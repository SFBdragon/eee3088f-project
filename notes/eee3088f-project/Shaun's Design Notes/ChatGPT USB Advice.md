
Designing a PCB to negotiate 9V power delivery over USB-C, especially with at least 600mA or 200mA, requires understanding the USB Power Delivery (USB PD) protocol and the components that can handle this negotiation without requiring a full microcontroller. Here's a guide to help you get started:

### 1. **Understanding USB PD Protocol:**
   - **USB PD Specification**: To negotiate 9V, you'll need to follow the USB PD specification, which defines how devices can communicate over USB-C to negotiate power requirements. The USB PD protocol allows for multiple voltage levels (5V, 9V, 15V, 20V, etc.), and it uses communication over the CC (Configuration Channel) lines to establish voltage and current capabilities.
   - **Resources for Learning**:
     - **USB Power Delivery Specification**: The official USB Power Delivery specification (available from the [USB Implementers Forum](https://www.usb.org/)) is the most comprehensive resource.
     - **"USB Power Delivery – A Technical Overview"** by Texas Instruments: This document explains the PD protocol in-depth.
     - **USB Power Delivery Wiki**: Some communities maintain open-source wikis on USB PD, which can be a helpful resource.
     - **Webinars/Tutorials**: Look for tutorials by semiconductor companies like Texas Instruments, Analog Devices, and STMicroelectronics. They provide webinars and whitepapers explaining USB PD and its implementation.

### 2. **Achieving 9V Negotiation:**
   - **Power Delivery ICs**: For your application, you'll need an IC that can handle the USB PD negotiation process and support 9V as one of the voltage levels. Fortunately, there are several options that don’t require a full microcontroller. These chips can take care of the protocol communication and voltage selection for you.
   
     **Recommended ICs**:
     - **Texas Instruments TUSB320**: This is a popular USB Type-C controller that supports USB PD. It is capable of negotiating 5V, 9V, 15V, and 20V, and comes in a small package for integration into your design.
     - **STMicroelectronics STUSB4500**: This IC supports USB PD 3.0 and can negotiate various voltages, including 9V. It can work with minimal external components.
     - **NXP PTN5150**: Another USB PD sink controller, capable of negotiating various voltages and provides a reliable solution for USB PD 2.0/3.0 devices.

   These ICs typically come with a low-power mode and are designed to operate without the need for an external microcontroller, making them suitable for your design requirements.

### 3. **Component Recommendations for 9V Power Delivery**:
   To design the PCB, you'll need a few additional components:
   - **Buck-Boost Converter**: Depending on the voltage supplied by the USB host, you might need a buck-boost converter to regulate the voltage to 9V. Components like **Texas Instruments LM2623** or **Analog Devices LTC3535** are good options.
   - **USB Type-C Receptacle**: Make sure to choose a USB Type-C connector that can handle the required current (at least 600mA) and provide proper connections to the CC lines.
   - **Power MOSFETs**: If you are controlling power switching, make sure to choose low Rds(on) MOSFETs to minimize power losses.

### 4. **Designing with JLCPCB:**
   - **JLCPCB Parts Library**: JLCPCB has a variety of components available in their library, including common USB-C components. You can use their [component search](https://jlcpcb.com/parts) to check for USB PD ICs and other components compatible with your design.
   - **Check Availability**: You’ll want to verify if your chosen ICs and other components are available in JLCPCB’s parts list to avoid sourcing issues.
   
   - **Schematic & Layout Tools**: JLCPCB provides support for importing designs made in popular tools like KiCad, Altium, and Eagle. If you haven’t already, consider using these tools to design your PCB, as they have built-in libraries for USB-C components and power delivery circuits.

### 5. **Additional Notes**:
   - **Testing USB PD**: After designing the PCB, you'll need to test the USB PD functionality. USB PD testers like the **Total Phase USB Power Delivery Analyzer** can help you verify that your design properly negotiates with a USB PD host.
   - **Thermal Considerations**: High current through the USB Type-C connector can generate heat, so ensure your layout accounts for proper thermal dissipation, especially near the power delivery components.

### Conclusion:
To achieve 9V power delivery with a USB-C interface on your PCB, you can use a USB PD controller IC (such as the TI TUSB320 or STUSB4500), along with additional components like a buck-boost converter and MOSFETs for power switching. By leveraging available resources and libraries (such as JLCPCB's parts catalog), you can design an efficient and functional PCB that negotiates 9V delivery without requiring a full microcontroller.