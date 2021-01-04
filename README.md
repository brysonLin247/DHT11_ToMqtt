# DHT11_ToMqtt

**简介：** ESP8266通过MQTT协议将温湿度数据传输至OnenNet云平台

#### 1. 具体功能：

1.  DHT11采集环境温湿度数据，ESP8266模块通过MQTT协议将温湿度数据传输至OnenNet云平台
2.  OneNET可以通过云平台远程控制LED灯的亮灭
3.  串口显示相关数据信息

#### 2. 硬件环境：

1. 正点原子STM32F103RCT6（正点原子MiniSTM32）
2. DHT11温湿度传感器
3. ESP8266-01S无线模块

#### 3. 云平台环境配置：

1. **云平台配置：**
- OneNET控制台—全部产品服务（多协议接入，选MQTT旧版）—添加产品—进入产品（记住产品ID）—设备列表—添加设备（记住鉴权信息）—创建完成（记住设备ID）
  
2. **云平台应用设置：**
- 添加应用—编辑应用—组件库中添加折线图和开关
  
- 折线图（数据上传成功后进行配置）: 选择数据流 — 选择设备—数据流选择要显示的数据（这里选择温度，temperature）
   - 开关（数据上传成功后进行配置）: 选择数据流 — 选择设备—数据流选择要显示的数据（这里选择温度，ledFlag）—开关开值（LEDON）—开关关值（LEDOFF）——EDP不填

#### 4. 接线：

1. ESP8266-01S（5根线）

   - PA2     RX
   - PA3     TX
   - PA4     复位
   - 3V3     VCC
   - GND   GND

2. DHT11（3根线）

   - PA6    DATA

   - 3V3     VCC

   - GND   GND

3. LED
   - PD2    LED1