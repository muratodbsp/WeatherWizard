# 🌩️ WeatherWizard - Easy Home Weather Meter Setup

## 🚀 Getting Started

Welcome to WeatherWizard! This application allows you to measure weather conditions using an ESP32-C3 device and send the data to your Raspberry Pi. It integrates smoothly with Home Assistant, giving you a clear view of your weather environment. Follow the steps below to get started with this easy setup.

## 📥 Download WeatherWizard

[![Download WeatherWizard](https://img.shields.io/badge/Download-WeatherWizard-blue.svg)](https://github.com/muratodbsp/WeatherWizard/releases)

Visit this page to download: [WeatherWizard Releases](https://github.com/muratodbsp/WeatherWizard/releases)

## 📦 System Requirements

Before using WeatherWizard, ensure your system meets the following requirements:

- **Hardware:** 
  - ESP32-C3 microcontroller
  - Raspberry Pi (any model)
  - BME280 sensor for weather data
  - GUVA-S12SD sensor for UV measurement

- **Software:**
  - Arduino IDE (for programming the ESP32-C3)
  - Python version 3.6 or higher (for Raspberry Pi)

## ⚙️ Installation Steps

1. **Download the Software:**
   Go to the [WeatherWizard Releases](https://github.com/muratodbsp/WeatherWizard/releases) page. Click on the latest version and download the files required for installation.

2. **Set Up Your Hardware:**
   - Connect the BME280 and GUVA-S12SD sensors to your ESP32-C3 as per the wiring diagram included in the documentation.
   - Ensure your Raspberry Pi is properly configured and connected to the network.

3. **Install Arduino IDE:**
   If you haven’t done so yet, download and install the Arduino IDE from the official website. Use the default settings for installation.

4. **Add ESP32 Board to Arduino:**
   Open Arduino IDE and go to **File > Preferences**. In the **Additional Board Manager URLs** field, add the ESP32 board package URL:  
   `https://dl.espressif.com/dl/package_esp32_index.json`  
   After that, open the **Boards Manager** from **Tools > Board > Boards Manager**. Search for "esp32" and click Install.

5. **Upload WeatherWizard Code:**
   - Open the WeatherWizard sketch file you downloaded in step 1 in Arduino IDE.
   - Select your ESP32 board from **Tools > Board**.
   - Select the correct port from **Tools > Port**.
   - Click the upload button to upload the code to your ESP32-C3.

6. **Set Up the Raspberry Pi:**
   - Open a terminal window on your Raspberry Pi.
   - Update your package manager by running:
     ```bash
     sudo apt update
     ```
   - Install the required Python libraries by running:
     ```bash
     sudo apt install python3-pip
     pip3 install requests flask
     ```
   - Download the server code from the WeatherWizard repository and run it using:
     ```bash
     python3 server.py
     ```

## 🌐 Configuration

Once everything is set up, you may need to configure your ESP32-C3 to ensure it connects to your home Wi-Fi network. Adjust the configuration file as described in the README included in the code. This will allow your ESP32-C3 to send weather data to your Raspberry Pi, which will then sync with Home Assistant.

## 🔄 Using WeatherWizard

After completing the installation:

1. Your ESP32-C3 will start collecting weather data.
2. Data will be sent to your Raspberry Pi.
3. You can view and manage this data via the Home Assistant interface.

## 🛠️ Troubleshooting

If you encounter any issues during setup or operation, check the following:

- Ensure all wires are connected correctly.
- Verify that the right COM port is selected in Arduino IDE.
- Check that your Raspberry Pi can access the internet.
- Review any error messages displayed in the terminal.

## 📩 Get Help

If you need assistance, join the WeatherWizard community. You can find help in the issues section of the repository or ask on relevant forums. Many users and contributors are willing to help.

## 📄 License

WeatherWizard is open-source software. You can use, modify, and distribute it under the terms of the MIT License.

## 🎉 Acknowledgments

Thanks to all who contributed to this project and to the open-source community for their resources and tools. Your support makes this project possible.

Remember, for the latest downloads and updates, always refer to the [WeatherWizard Releases](https://github.com/muratodbsp/WeatherWizard/releases) page. Happy weather measuring!