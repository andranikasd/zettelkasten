

This guide provides instructions for developers on how to implement validation for input fields required for creating PostgreSQL clusters using the CNPG PostgreSQL Operator. The validated data will be used to generate manifests in JSON format that will be pushed to GitLab, triggering ArgoCD to deploy the cluster. All custom fields should be included in labels or annotations.

## 1. Name and Namespace Validation Guide

### Name Validation

- **Allowed Characters**: Lowercase alphanumeric characters, `-` (dash), and `.` (dot).
- **Start and End Characters**: Must start and end with an alphanumeric character.
- **Length**: Minimum 1 character, maximum 253 characters.
- **Pattern**: Regular Expression - `^[a-z0-9]([-a-z0-9]*[a-z0-9])?$`

#### Examples

- **Valid**: `pg-cluster-1`, `mydatabase`, `postgres.cluster`
- **Invalid**: `PgCluster`, `my_database`, `-pgcluster`, `pgcluster-`

### Namespace Validation

- **Allowed Characters**: Lowercase alphanumeric characters, `-` (dash), and `.` (dot).
- **Start and End Characters**: Must start and end with an alphanumeric character.
- **Length**: Minimum 1 character, maximum 253 characters.
- **Pattern**: Regular Expression - `^[a-z0-9]([-a-z0-9]*[a-z0-9])?$`

#### Examples

- **Valid**: `default`, `kube-system`, `namespace1`
- **Invalid**: `NameSpace`, `my_namespace`, `.namespace`, `namespace-`

## 2. Storage Size Validation Guide

### General Guidelines

- **Format**: Storage size must be specified as a positive integer followed by a unit of measure (e.g., Mi, Gi, Ti).
- **Units**: Supported units are Mi (Mebibytes), Gi (Gibibytes), Ti (Tebibytes).
- **Minimum Value**: 500 Mi
- **Pattern**: Regular Expression - `^[1-9][0-9]*[MGiTi]{1,2}$`

#### Examples

- **Valid**: `10Gi`, `512Mi`, `1Ti`
- **Invalid**: `0Gi`, `100`, `10g`, `100MB`

## 3. Instances Count Validation Guide

### General Guidelines

- **Type**: Positive integer
- **Minimum Value**: 1
- **Maximum Value**: 100 (or any other reasonable upper limit based on your system's constraints)
- **Pattern**: Regular Expression - `^[1-9][0-9]{0,1}$`

#### Examples

- **Valid**: `1`, `10`, `25`
- **Invalid**: `0`, `-5`, `101`, `1.5`, `ten`


#### Example 

```json
{
  "apiVersion": "postgresql.cnpg.io/v1",
  "kind": "Cluster",
  "metadata": {
    "annotations": {
      "version": "1",
      "resourceType": "postgres"
    },
    "labels": {
      "app.kubernetes.io/instance": "postgresql-databases"
    },
    "name": "some-pgsql-db"
  },
  "spec": {
    "imageName": "ghcr.io/cloudnative-pg/postgresql:16.1",
    "instances": 1,
    "storage": {
      "size": "500Mi",
      "storageClass": "directpv-min-io"
    }
  }
}
```