
### 1. Introduction

This document provides a comprehensive guide for setting up a portable computing system housed in a case. The system includes a mini-PC, battery, L3 switch, and router. This setup is designed to be portable, durable, and suitable for various environments, meeting IP65 standards for dust and water resistance.

### 2. Requirements

#### Mini-PCs

- **Fanless Design**
- **RAM**: Minimum 32GB
- **CPU**: 8+ core processor
- **Storage**: Non-SD card storage of at least 512 GB (e.g., SSD or NVMe drive)

### List of Products: Mini PCs

| **Product**                               | **Specifications**                                     | **Default TDP** | **Price** | **Link to Product**                                                                                                                                                                                                                                                                                                                                                                                                           | **Status**  | **Reason**                   |
| ----------------------------------------- | ------------------------------------------------------ | --------------- | --------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------- | ---------------------------- |
| **XCY Ryzen 5 5625U**                     | AMD Ryzen 5 5625U(8 cores), 32GB RAM, 1TB SSD, Fanless | 15W             | $500      | [XCY Ryzen 5 5625U](https://aliexpress.ru/item/1005006416028795.html?sku_id=12000037087594429&spm=a2g2w.productlist.search_results.16.1aeb51436GvBZW)                                                                                                                                                                                                                                                                         | Order       | Suitable specs               |
| **Промышленный мини-компьютер**           | Core i5-3317U, 8GB RAM, 256GB SSD, Fanless             | 17W             | $150.36   | [Промышленный мини-компьютер](https://aliexpress.ru/item/32885585650.html?srcSns=sns_Copy&businessType=ProductDetail&spreadType=socialShare&tt=MG&utm_medium=sharing&sku_id=12000022677387826)                                                                                                                                                                                                                                | Denied      | Low RAM                      |
| **BEBEPC**                                | Core i5-7560U(2 cores), 32GB RAM                       | 15W             | $500      | [BEBEPC](https://aliexpress.ru/item/1005003660853253.html?sku_id=12000033256372676&spm=a2g2w.productlist.search_results.15.4ad2daf9oZZMZP)                                                                                                                                                                                                                                                                                    | Review      | Low cores count              |
| **безвентиляторный промышленный мини-ПК** | Core i7-1255U(10 cores), 16GB RAM, 512GB SSD, Fanless  | 15W             | $378      | [безвентиляторный промышленный мини-ПК](https://aliexpress.ru/item/1005006595778880.html?spm=a2g2w.detail.similar_rcmd.5.3fae4985XSTUG1&mixer_rcmd_bucket_id=aerabtestalgoRecommendAbV26_testVectorSearchDefaultAndClickStream&pdp_trigger_item_id=0_4000169727654&ru_algo_pv_id=4777df-61b690-8423cd-a8adfa-1716040800&scenario=aerSimilarItemPdpRcmd&sku_id=12000037764962258&traffic_source=recommendation&type_rcmd=core) | Alternative | Test needed, TDP,<br>Low RAM |
| **EGLOBAL**                               | Core i5-8260U(4 cores), 32GB RAM, 1TB SSD, Fanless     | 25W             | $440      | [EGLOBAL](https://aliexpress.ru/item/1005006889985959.html?sku_id=12000038631036942&spm=a2g2w.productlist.search_results.10.4ad2daf9oZZMZP)                                                                                                                                                                                                                                                                                   | Review      | Low cores count              |
| **Мини-ПК промышленный без кулера**       | Core i7-1255U(10 cores), 32GB RAM, 1TB SSD, Fanless    | 15W             | $580      | [Мини-ПК промышленный без кулера](https://aliexpress.ru/item/1005006606120955.html?sku_id=12000037822247273&spm=a2g2w.productlist.search_results.14.4ad2daf9oZZMZP)                                                                                                                                                                                                                                                           | Review      | Price, TDP                   |
| **Beelink SER6 Mini**                     | AMD Ryzen 5 5625U(8 cores), 32GB RAM, 1TB SSD          | 45W             | $580      | [Beelink SER6 Mini](https://www.amazon.com/dp/B0CJF7ZX3W?tag=track-ecv-usa-777407-20&linkCode=osi&th=1)                                                                                                                                                                                                                                                                                                                       | Denied      | Fanless non-approved         |
| **Topton**                                | AMD Ryzen 7 7730U(8 cores), 32GB RAM, 1TB SSD, Fanless | 15W             | $665      | [Topton](https://aliexpress.ru/item/1005005253862425.html?sku_id=12000032372076826&spm=a2g2w.productlist.search_results.11.6b1d104drD0Z7Q)                                                                                                                                                                                                                                                                                    | Alternative | Price                        |

#### Switches

- **Layer 3 (L3) Switch**: Capable of handling VLANs, QoS, and other L3 functionalities.

### List of Products: Switches

|**Product**|**Specifications**|**Default TDP**|**Price**|**Link to Product**|**Status**|**Reason**|
|---|---|---|---|---|---|---|
|**MikroTik CRS328-24P-4S+RM**|24 Gigabit Ethernet, 4 SFP+, Layer 3, PoE, 512MB RAM|44W|$463|[MikroTik CRS328-24P-4S+RM](https://www.amazon.com/Mikrotik-CRS328-24P-4S-RM-Ethernet-rackmount/dp/B07C657P7Q)|On Review|Price, TDP|
|**MikroTik CRS328-24P-2S+RM**|24 Gigabit Ethernet, 2 SFP+, Layer 3, 512MB RAM|24W|$150|[MikroTik CRS328-24P-2S+RM](https://www.amazon.com/Mikrotik-CSS326-24G-2S-RM-Gigabit-Ethernet/dp/B0723DT6MN)|Choose for Order|Suitable specs, price|
|**TP-Link TL-SG3428**|24 Gigabit Ethernet, 4 SFP, Layer 3, 512MB RAM|18W|$170|[TP-Link TL-SG3428](https://www.amazon.com/TP-Link-TL-SG3428-Integrated-Lifetime-Protection/dp/B0916BP6J5)|Alternative|Good specs, affordable price|
|**Huawei S5720-28X-SI-AC**|24 Gigabit Ethernet, 4 SFP+, Layer 3, 512MB RAM|35W|$450|[Huawei S5720-28X-SI-AC](https://www.huawei-networks.ru/catalog/switches_huawei_s5720-sl/s5720-28x-si-ac)|On Review|High price, good specs|

#### Routers

- **Integrated VPN Solutions**: The router should support multiple VPN protocols (e.g., OpenVPN, IPSec) and provide robust security features.

### List of Products: Routers

| **Product**               | **Specifications**                                                | **Default TDP** | **Price** | **Link to Product**                                                                               | **Status**       | **Reason**                     |
| ------------------------- | ----------------------------------------------------------------- | --------------- | --------- | ------------------------------------------------------------------------------------------------- | ---------------- | ------------------------------ |
| **MikroTik hEX S**        | 5 Gigabit Ethernet, 1 SFP, IPsec HW Acceleration, Passive Cooling | 6W              | $70       | [MikroTik hEX S](https://www.amazon.com/MikroTik-Gigabit-Ethernet-Router-RB760iGS/dp/B07F7HDRKX)  | Choose for Order | Low TDP, suitable specs        |
| **Ubiquiti EdgeRouter 4** | 3 Gigabit Ethernet, 1 SFP, VPN Support (OpenVPN, IPSec)           | 25W             | $200      | [Ubiquiti EdgeRouter 4](https://www.amazon.com/Ubiquiti-Networks-ER-4-EdgeRouter-4/dp/B078PGCGN2) | Alternative      | High TDP, higher price         |
| **Tenda G3**              | 5 Gigabit Ethernet, Dual-WAN, VPN Support (OpenVPN, IPSec)        | 15W             | $80       | [Tenda G3](https://www.tendacn.com/product/g3.html)                                               | Alternative      | Moderate TDP, good specs       |
| **TP-Link TL-R605**       | 5 Gigabit Ethernet, Dual-WAN, VPN Support (OpenVPN, IPSec)        | 10W             | $60       | TP-Link TL-R605                                                                                   | Alternative      | Low TDP, very affordable price |

#### Cases

- **Mobility**: Case should have wheels for easy transportation
- **IP Standard**: At least IP67 to ensure complete protection against dust and prolonged immersion in water

### List of Products: Cases

|**Product**|**Specifications**|**IP Standard**|**Price**|**Link to Product**|**Status**|**Reason**|
|---|---|---|---|---|---|---|
|**Pelican 1650 Protector Case**|28.57 x 17.52 x 10.65 in, wheels, waterproof, crushproof, dustproof|IP67|$380|[Pelican 1650 Protector Case](https://www.pelican.com/us/en/product/cases/protector/1650)|Alternative|Price|
|**Nanuk 945 Case**|25.4 x 19.3 x 8.6 in, wheels, waterproof, dustproof, crushproof|IP67|$240|[Nanuk 945 Case](https://www.amazon.com/Nanuk-Waterproof-Hard-Case-Insert/dp/B003JH7ZWC)|Alternative|Price|
|**B&W International Type 6700**|24.0 x 17.3 x 9.4 in, wheels, waterproof, dustproof, crushproof|IP67|$197|[B&W International Type 6700](https://www.amazon.com/B-W-International-Type-6700-Outdoor/dp/B00BFZ18V4)|Alternative|Price|
|**HPRC 2700W**|25.6 x 19.7 x 10.8 in, wheels, waterproof, dustproof, crushproof|IP67|$290-370|[HPRC 2700W](https://www.amazon.com/HPRC-2700W-Wheeled-Hard-Case/dp/B08H7MNDS5)|Alternative|Price|
|**SKB 3I-2918-10BC iSeries**|29" x 18" x 10" - Cubed Foam w/Wheels, waterproof, dustproof, crushproof|IP67|$380|[SKB 3I-2918-10BC iSeries](https://www.amazon.com/SKB-3I-2918-10BC-29in-10-85in-wheels/dp/B004IBP8LS)|Alternative|Price|
|**Bootech Suggested**|?|IP68|$100|?|Choose for Order|IP68 rating|

#### Connectors

- **IP Standard**: At least IP67 to ensure complete protection against dust and prolonged immersion in water

### List of Products: Connectors

|**Product**|**Specifications**|**IP Standard**|**Price**|**Link to Product**|
|---|---|---|---|---|
|**RJ45 Bulkhead Connector**|RJ45, panel mount, shielded|IP67|~$20|RJ45 Bulkhead Connector|
|**Power Connector**|DC power input/output, panel mount|IP67|~$15|Power Connector|
|**USB Bulkhead Connector**|USB Connector, panel mount|IP67|~$25|USB Bulkhead Connector|
|**HDMI Bulkhead Connector**|HDMI, panel mount|IP67|~$30|HDMI Bulkhead Connector|
|**Circular Connector**|Multipin, panel mount|IP67|~$40|Circular Connector|

### 3. Setup and Integration

#### Component Placement

- **Case**: Contains foam padding and space for cable management.
- **Components**:
    - **Mini-PC**: Placed on one side of the main compartment, connected to the battery for power and the switch for networking.
    - **Battery**: Centrally located for easy power distribution to all components.
    - **L3 Switch**: Positioned on the opposite side from the Mini-PC, connected to the router and other network devices.
    - **Router**: Near the switch for efficient networking connections.

#### Connections

- **Power**:
    - The Mini-PC, switch, and router are connected to the battery for power.
    - The battery supports charging while providing power (pass-through charging).
- **Network**:
    - The Mini-PC connects to the switch.
    - The switch connects to the router and other network devices.
- **Output Ports**:
    - Install IP67-rated RJ45 bulkhead connectors for Ethernet ports.
    - Install IP67-rated power connectors for power input/output ports.
    - Install IP67-rated USB bulkhead connectors for data transfer ports.
    - Use waterproof grommets and seals to ensure no water can enter through the drilled holes.

### 4. Power Consumption Calculation

#### Power Consumption Breakdown

|**Component**|**Power Consumption**|
|---|---|
|**Mini-PC**|45W|
|**L3 Switch**|44W|
|**Router**|6W|
|**Total**|45W + 44W + 6W = 95W|

#### Required Battery Capacity

To calculate the required battery capacity for 6 hours of operation:

Required Capacity=Total Power Consumption×Hours of OperationRequired Capacity=Total Power Consumption×Hours of Operation Required Capacity=95�×6 hours=570�ℎRequired Capacity=95W×6 hours=570Wh

Using two ALLPOWERS Portable Power Stations (288Wh each), the total capacity would be 576Wh, which is sufficient for 6 hours of operation.

### List of Products: Batteries

| **Product**                          | **Specifications**                              | **IP Standard** | **Price** | **Link to Product**              |
| ------------------------------------ | ----------------------------------------------- | --------------- | --------- | -------------------------------- |
| **ALLPOWERS Portable Power Station** | 288Wh, AC Outlets, USB Ports, 12V Outputs, IP65 | IP65            | $300      | ALLPOWERS Portable Power Station |
| **Jackery Explorer 500**             | 518Wh, AC Outlets, USB Ports, 12V Outputs, IP65 | IP65            | $499      | Jackery Explorer 500             |
| **Goal Zero Yeti 400**               | 396Wh, AC Outlets, USB Ports, 12V Outputs, IP65 | IP65            | $450      | Goal Zero Yeti 400               |
| Bootech Suggested                    | ?                                               | ?               | ?         | ?                                |
|                                      |                                                 |                 |           |                                  |


### 6. Price Calculation with Selected Products (Delivery Price not included)

| **Component**  | **Product**                                                                     | **Price**       |
| -------------- | ------------------------------------------------------------------------------- | --------------- |
| **Case**       | Bootech Suggested                                                               | $100            |
| **Mini-PC**    | XCY Ryzen 5 5625U                                                               | $500            |
| **L3 Switch**  | MikroTik CRS328-24P-2S+RM                                                       | $150            |
| **Router**     | MikroTik hEX S                                                                  | $70             |
| **Battery**    | ALLPOWERS Portable Power Station (x2) OR Bootech Suggested                      | $300 x 2 = $600 |
| **Connectors** | RJ45 Bulkhead Connector (2x), Power Connector (2x), USB Bulkhead Connector (2x) | $120            |

**Total Cost**: $100 + $500 + $150 + $70 + $600 + $120 = **$1,540** (595.000 AMD)

This configuration meets all requirements, maintains the IP67 standard, and fits within the budget constraints while ensuring a minimum of 6 hours of operation without being connected to a power source.