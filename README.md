# 🚨 ESP32-Based Fire & Gas Monitoring System — RTOS-Driven Embedded Design 🚨

A standalone embedded fire and gas monitoring system emphasizing **power integrity**, **RF-aware PCB layout**, and **deterministic real-time behavior** using **FreeRTOS**.  

The system integrates **sensing, processing, and cellular communication** on a single expansion PCB, enabling reliable operation **without external network dependency**.  

---

## ⚡ MCU & RTOS
- **ESP32 dual-core** running FreeRTOS  
- Tasks separated for **deterministic response** and **fault isolation**:  
  - Sensor acquisition  
  - Event evaluation / threshold logic  
  - GSM communication (AT command handling)  
  - Alert & retry management  
- **RTOS queues and semaphores** synchronize sensor events and communication states  
- **Watchdog supervision** ensures task-level fault recovery  

---

## 📡 Cellular Communication
- **GSM800L quad-band module (2G)**  
- UART interface controlled via RTOS task  
- Power design accommodates **~2A peak TX current** during GSM bursts  
- Local **bulk and low-ESR decoupling** reduces voltage sag  
- Enables **SMS-based alerting independent of Wi-Fi or cloud services**  

---

## 🔥 Sensor Subsystem
- Flame sensor for **fast IR fire detection**  
- MQ-2 gas/smoke sensor for **combustible gas detection**  
- DHT11 for **temperature & humidity context**, helping reduce false alarms  

---

## 🔋 Power & Reliability
- On-board **18650 Li-ion battery** for autonomous operation  
- Power domains partitioned between:  
  - RF load (GSM)  
  - Digital logic (ESP32)  
  - Analog sensing  
- Ensures **MCU stability during RF current spikes**  
- System remains operational during mains power failure  

---

## 🛠 PCB & Integration
- Modular expansion-board layout  
- **Wide, low-impedance power traces** for RF paths  
- Continuous ground reference for **noise control**  
- Reduced wiring and connector failure points  

---

## 🎯 Engineering Objective
Deliver a **deployable, real-world embedded safety system** with:  
- RTOS-based **task determinism**  
- Reliable **alert delivery**  
- **Power-aware hardware design**  
- Clean **firmware–hardware co-design**  

---

## 📂 Repository Contents
- `hardware/` — PCB schematics, Gerber files, and BOM  
- `firmware/` — FreeRTOS-based ESP32 firmware  
- `docs/` — RTOS task diagrams, scheduler priorities, and system design notes  
- `README.md` — Project overview and documentation  

---

## 🔗 Resources
- Open-source schematics, PCB, and RTOS firmware: [GitHub Repository](https://github.com/iarpan1/fire_detector)  

---

## 🏷 Tags
`EmbeddedSystems` `RTOS` `FreeRTOS` `ESP32` `HardwareDesign` `GSM` `PCBDesign` `PowerIntegrity` `FireSafety` `ElectronicsEngineering` `OpenSource`
