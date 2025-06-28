<!-- omit in toc -->
# thinking-in-chaos
Thinking in Chaos.

- [0. Overview前景](#0-overview前景)
  - [智能家居](#智能家居)
  - [智能建筑](#智能建筑)
  - [智慧制造](#智慧制造)
  - [智慧农业](#智慧农业)
  - [其它](#其它)
- [1. 感知层Downlink](#1-感知层downlink)
  - [1.1 Sensors](#11-sensors)
  - [1.2 Actuators](#12-actuators)
  - [1.3 Controllers](#13-controllers)
- [2. 传输层Uplink](#2-传输层uplink)
  - [Wireless](#wireless)
  - [Wire](#wire)
  - [Protocol](#protocol)
  - [速率](#速率)
- [3. 平台层Platform](#3-平台层platform)
- [4. 应用层Application](#4-应用层application)


## 0. Overview前景
### <font color="Green">智能家居</font>
将家庭内单品进行联网，通过语音实时控制，打造智能家居平台。
### <font color="Green">智能建筑</font>
利用传感器将建筑内的设备数字化、智能化，以节约能源。
### 智慧制造
对厂房的机械设备及室内环境等情况进行联网监控。
### 智慧农业
利用传感器实时监测作物及畜牧产品的生长情况。
### 其它
智能安防、车联网、公共服务、智慧物流、智能交通、智慧能源、智能医疗、智能零售......

## 1. 感知层Downlink
### 1.1 Sensors
* <font color="Green">Temperature温度</font>
* <font color="Green">Humidity湿度</font>
* Occupancy
* Contact
* Pressure
* Flow
* Air Quality Sensor
* Water Freeze Detecotr
* Water Leak Detector
* Rain
* ~~压力（重量）、气压（轮胎胎压）、光照强度、气体成分、指纹、面部识别、速度和位移...~~

### 1.2 Actuators
* <font color="Green">Relay</font>
* <font color="Green">Water Valve</font>
  * <font color="Green">On/Off Valve</font>
  * <font color="Green">Floating Valve</font>
  * <font color="Green">Modulating Valve</font>
  * <font color="Green">Six way valve</font>
* <font color="Green">Pump</font>
* ~~Light~~
* ~~Plug/Outlets~~
* ...

### 1.3 Controllers
* Switches and controls
  * Pump Controller

* HVAC
  * <font color="Green">Thermostat</font>
  * <font color="Green">Fan</font>
  * <font color="Green">Air Purifier</font>

* Energy
  * Water Heater
  * Solar Power
  * Heat Pump

* ~~Media~~

## 2. 传输层Uplink
### Wireless
* 短距离
  * <font color="Green">Wi-Fi</font>
  * <font color="Green">Thread</font>
  * Zigbee
  * BLE
* 长距离
  * LoRaWAN
  * NB-IoT/Cat.M
  * eMTC

### Wire
* <font color="Green">RS-485</font>
* Enthernet

### Protocol
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

### 速率
* 高速率业务主要使用3G、4G 及WiFi技术，可应用于视频监控、车载导航等场景；
* **中速率**业务主要使用蓝牙、eMTC等技术，可应用于智能家居、储物柜等高频使用场景；
* **低速率**业务，即LPWAN(低功耗广域网)，主要使用NB-IoT、LoRa、Sigfox及ZigBee等技术，可能应用于智慧停车、远程抄表等使用频次低的应用场景

## 3. 平台层Platform
* ThingsBoard
* HomeAssistant
* Tuya
* RainMaker
* AWS/AliYun/Google IoT
* ChipStack - LoRaWAN

## 4. 应用层Application
* Apple Home app
* Google Home app
* AWS
* ...