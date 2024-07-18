# Fetal-Monitoring-System
### Project Description: Non-Invasive Fetal Movement Monitoring System

This project aims to develop a non-invasive, cost-effective fetal movement monitoring system using the ESP32 microcontroller and MPU6050 accelerometers. The primary objective is to enable pregnant mothers to monitor fetal movements at home, thus ensuring continuous fetal health monitoring without frequent clinical visits. The system is designed to be reliable, low-cost, and user-friendly, providing timely alerts for any abnormal fetal movements.

### Components Used:
1. **ESP32 Microcontroller:** Serves as the main processing unit and handles Bluetooth communication.
2. **MPU6050 Accelerometers:** Three accelerometers are used to capture fetal movements.
3. **TCA9548A I2C Multiplexer:** Allows multiple I2C devices to communicate with the ESP32.
4. **Bluetooth Module:** Integrated within the ESP32 to transmit data to a mobile application.
5. **Buzzer:** Provides audible alerts for abnormal conditions.
6. **3.7V Batteries and BMS Board:** Power the system and manage battery health.
7. **MIT App Inventor:** Used to develop the mobile application that receives and displays fetal movement data.

### Step-by-Step Build Process:

1. **Component Integration:**
   - Connect the MPU6050 accelerometers to the TCA9548A I2C multiplexer, which is then connected to the ESP32's I2C pins (SCL and SDA).
   - Wire the buzzer to one of the GPIO pins of the ESP32.

2. **Power Management:**
   - Connect two 3.7V batteries in parallel to the BMS board to ensure stable power supply and battery protection.
   - Power the ESP32 and the connected components from the BMS board.

3. **Sensor Initialization:**
   - Initialize the I2C communication in the ESP32 code.
   - Configure and initialize each MPU6050 sensor via the I2C multiplexer.

4. **Data Processing:**
   - Continuously read acceleration data from each MPU6050 sensor.
   - Calculate the magnitude of movements and compare them against predefined thresholds for normal, stretching, and kicking movements.

5. **Bluetooth Communication:**
   - Establish a Bluetooth connection between the ESP32 and the mobile app.
   - Continuously send processed data to the mobile app.

6. **Alert Mechanism:**
   - Implement a function to check for abnormal conditions based on movement data.
   - Trigger the buzzer for an audible alert if abnormal movement is detected.

7. **Mobile Application:**
   - Develop a mobile app using MIT App Inventor to display real-time data and alerts.
   - The app provides an interface for users to monitor fetal movements and receive notifications.

### Final Integration:
   - Test the entire system to ensure reliable performance.
   - Optimize the system for power consumption and user-friendliness.

This comprehensive system offers an effective solution for at-home fetal movement monitoring, combining sensor technology with mobile app integration to enhance prenatal care.
