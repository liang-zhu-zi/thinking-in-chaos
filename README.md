<!-- omit in toc -->
# thinking-in-chaos
Thinking in Chaos.

- [1. Applications](#1-applications)
- [2. Solutions](#2-solutions)
- [3. Products](#3-products)
  - [3.1 Hardware](#31-hardware)
    - [3.1.1 DevKits](#311-devkits)
    - [3.1.2 Equipment](#312-equipment)
      - [A. Sensors](#a-sensors)
      - [B. Actutors](#b-actutors)
      - [C. Controllers](#c-controllers)
      - [D. HMIs](#d-hmis)
      - [E. Misc](#e-misc)
  - [3.2 SDKs](#32-sdks)
  - [3.3 Cloud](#33-cloud)
- [4. Technology](#4-technology)
  - [4.1 感知层Downlink](#41-感知层downlink)
    - [4.1.1 Sensors](#411-sensors)
    - [4.1.2 Actuators](#412-actuators)
    - [4.1.3 Controllers](#413-controllers)
    - [4.1.3 HMIs](#413-hmis)
  - [4.2 传输层Uplink](#42-传输层uplink)
    - [4.2.1 Wireless](#421-wireless)
    - [4.2.2 Wire](#422-wire)
    - [4.2.3 Protocol](#423-protocol)
    - [4.2.4 速率](#424-速率)
  - [4.3 平台层Platform](#43-平台层platform)
  - [4.4 应用层Application](#44-应用层application)

## 1. Applications
* **<font color="Green">智能家居</font>**
  将家庭内单品进行联网，通过语音实时控制，打造智能家居平台。
* **<font color="Green">智能建筑</font>**
  利用传感器将建筑内的设备数字化、智能化，以节约能源。
* 智慧制造
  对厂房的机械设备及室内环境等情况进行联网监控。
* 智慧农业
  利用传感器实时监测作物及畜牧产品的生长情况。
* 其它
  智能安防、车联网、公共服务、智慧物流、智能交通、智慧能源、智能医疗、智能零售......

## 2. Solutions
* **<font color="Green">室内环境监测</font>**
  * **<font color="Green">环境监测</font>**
* **<font color="Green">HVAC应用</font>**
  * **<font color="Green">Thermostat</font>**
  * **<font color="Green">Fan</font>**
  * **<font color="Green">Water Valve</font>**
  * **<font color="Green">Heat Pump</font>**

## 3. Products
### 3.1 Hardware
#### 3.1.1 DevKits
#### 3.1.2 Equipment
##### A. Sensors
* <font color="Green">Temperature温度</font>
  * 负温度系数（NTC）热敏电阻
    * 接口类型：ADC
      * NTC10KTypeII
      * NTC10KTypeIII
      * NTC20K
  * SHT系列（SHT30/SHT31/SHT35）- SHTC3
* <font color="Green">Humidity湿度</font>
* Occupancy
  * PIR - PassiveInfrared
  * PHY - PhysicalContact
* Contact
* Air Quality Sensor
* Concentration 浓度
  * Carbon Monoxide Concentration 一氧化碳浓度
  * Carbon Dioxide Concentration 二氧化碳浓度
  * Formaldehyde Concentration 甲醛浓度
  * PM1 Concentration 
  * PM2.5 Concentration
  * PM10 Concentration
  * TVOC（Total Volatile Organic Compounds Concentration）总挥发性有机化合物浓度
* Pressure
* Flow
* Water Freeze Detecotr
* Water Leak Detector
* Rain
* ~~压力（重量）、气压（轮胎胎压）、光照强度、气体成分、指纹、面部识别、速度和位移...~~

##### B. Actutors
* <font color="Green">Relay</font>
* <font color="Green">Fan</font>
  * On/Off Fan
  * 3 Speed Fan
  * EC Fan
* <font color="Green">Water Valve</font>
  * <font color="Green">On/Off Valve</font>
  * <font color="Green">Floating Valve</font>
  * <font color="Green">Modulating Valve</font>
  * <font color="Green">Six way valve</font>
* <font color="Green">Pump</font>
* ~~Light~~
* ~~Plug/Outlets~~
* ...

##### C. Controllers
* Switches and controls
  * Pump Controller
* HVAC
  * <font color="Green">Thermostat</font>
  * <font color="Green">Air Purifier</font>
* Energy
  * Water Heater
  * Solar Power
  * Heat Pump

##### D. HMIs
* HVAC
  * <font color="Green">Thermostat</font>


##### E. Misc
| Power & Display            | Sensors | Actutors | Controllers |
|----------------------------|---------|----------|-------------|
| Low Power + No Display     | V       | V        | V           |
| Low Power + Mono LCD       | ?       | ?        | ?           |
| Low Power + E-Ink/E-Paper  | V       | V        | V           |
| Non-Low Power + No Display | ?       | V        | V           |
| Non-Low Power + Mono LCD   | ?       | ?        | ?           |
| Non-Low Power + B/W LCD    | V       | V        | V           |
| Non-Low Power + TFT LCD    |         |          | V           |

### 3.2 SDKs
* 开源社区版
* 闭源专业版

### 3.3 Cloud
* Integration
* Client App

## 4. Technology
### 4.1 感知层Downlink
#### 4.1.1 Sensors
* <font color="Green">Temperature温度</font>
  * 负温度系数（NTC）热敏电阻
    * 接口类型：ADC
      * NTC10KTypeII
      * NTC10KTypeIII
      * NTC20K
  * SHT系列（SHT30/SHT31/SHT35）
    * 类型：数字输出（I²C或UART）
    * 测量范围：湿度0-100%RH（±1.5%），温度-40-125℃（±0.2℃）
    * 特点：高精度、低功耗，工业级应用（如冷链、实验室）。
    * 厂商：Sensirion（瑞士盛思锐）
  * DHT系列（DHT11/DHT22/AM2302）
    * 类型：数字输出（单总线协议）
    * 测量范围：
      * DHT11：湿度20-80%RH（±5%），温度0-50℃（±2℃）
      * DHT22：湿度0-100%RH（±2%），温度-40-80℃（±0.5℃）
    * 特点：成本低、响应慢，适合一般民用场景（如家用温湿度计）。
    * 厂商：Aosong（广州奥松）
  * BME280
    * 类型：数字输出（I²C/SPI）
    * 功能：温湿度+气压三合一传感器
    * 特点：集成度高，适合气象站、无人机等。
    * 厂商：Bosch（博世）
  * BME680
    * 温度、湿度、气压、气体
    * 温度±0.5°C；湿度±3%RH
    * 四合一传感器
    * 适合空气质量检测
    * 厂商：Bosch（博世）
  * HDC2080
    * 温度：-40~125°C；
    * 湿度：0100%RH
    * 温度±0.2°C；湿度±2%RH
    * 高精度，低功耗，适合便携设备
  * 选型建议
    * 精度要求高：选择SHT3x、BME280、HDC2080等。
    * 预算有限：DHT11或DHT22是不错的入门选择。
    * 集成功能：需要气压检测时选BME280。
    * 需要多功能集成：BME680可同时测温、湿、压和气体。
    * 环境适应性：高温高湿环境优先选SHT31或HTU21D。
    * 成本敏感：DHT11或DS18B20（仅温度）+HR202组合。
  * 常见厂商品牌
    * Sensirion（瑞士）：SHT系列、SCD30（CO2+温湿度）。
    * Texas Instruments（美国）：HDC1080。
    * Omron（日本）：2JCIE系列（环境传感器）。
    * 国产替代：乐鑫（ESP32集成）、炜盛科技（温湿度模块）。

#### 4.1.2 Actuators
TODO:...

#### 4.1.3 Controllers
* ~~Media~~

#### 4.1.3 HMIs
TODO:...

### 4.2 传输层Uplink
#### 4.2.1 Wireless
* 短距离
  * <font color="Green">Wi-Fi</font>
  * <font color="Green">Thread</font>
  * Zigbee
  * BLE
* 长距离
  * LoRaWAN
  * NB-IoT/Cat.M
  * eMTC

#### 4.2.2 Wire
* <font color="Green">RS-485</font>
* Enthernet

#### 4.2.3 Protocol
* <font color="Green">Matter</font>
  * <font color="Green">Wi-Fi & BLE</font>
  * <font color="Green">Thread</font>
  * Enthernet
* <font color="Green">BACnet</font>
  * <font color="Green">BACnet MS/TP Slave</font>
  * BACnet IP Slave
* <font color="Green">Modbus</font>
  * Modbus RTU
  * Modbus IP

#### 4.2.4 速率
* 高速率业务主要使用3G、4G 及WiFi技术，可应用于视频监控、车载导航等场景；
* **中速率**业务主要使用蓝牙、eMTC等技术，可应用于智能家居、储物柜等高频使用场景；
* **低速率**业务，即LPWAN(低功耗广域网)，主要使用NB-IoT、LoRa、Sigfox及ZigBee等技术，可能应用于智慧停车、远程抄表等使用频次低的应用场景

### 4.3 平台层Platform
* ThingsBoard
* HomeAssistant
* Tuya
* RainMaker
* AWS/AliYun/Google IoT
* ChipStack - LoRaWAN

### 4.4 应用层Application
* Apple Home app
* Google Home app
* AWS
* ...
