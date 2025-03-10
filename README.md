# easun-icharger-mppt4880
ESPHome configuration for the EASUN Icharger MPPT-4880
![easun_icharger_mppt4880](https://github.com/user-attachments/assets/ecd4db7a-c9f6-4ccf-938b-e0895486b408)

Got this charger and was unable to find a proper configuration setup for controlling it via ESPHome. Everything was either half-assed or partially worked.

**EDIT:: Died after 5 days of use. Unless I am able to reset the device or get another, I will no longer update this!**

The yaml file here should hopefully work properly for anyone. The only part skipped was the battery equalization features which are not needed for lithium batteries.

This setup was done using an M5 Stack Atom Lite 2020 (not the S3 variant!) and an M5 Stack Tail485 to communicate with the Easun using the COM port:
 - Pins 1 and 2 from the COM port of the EASUN Charger must be used.   
 - Pin 3 (ground) is not necessary. If you get invalid data when resetting the MPPT controller and not rebooting the ESPHome device, try bridging Pin 3 to the ESPHome device negative/ground!   
  
M5 Stack Atom Lite: https://shop.m5stack.com/products/atom-lite-esp32-development-kit  
M5 Stack Tail485: https://shop.m5stack.com/products/atom-tail485  

2 YAML files are available:
 - The full configuration file if you want to replicate my setup (M5Stack Atom Lite + Tail485).
 - The configurattion section for the charger controller including the web_server block for the structured look


![easun_esphome](https://github.com/user-attachments/assets/fdc6698f-1499-40d9-b64b-b0e46d7df201)

