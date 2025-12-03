# Nanoka

> **Note:** This project is primarily targeted at users in Greater China (Mainland, Hong Kong, Macau, and Taiwan). This README provides a basic English overview; for detailed usage, please utilize translation tools.

## Compatibility
**Android 8 – Android 16**

## Prerequisites
A functional **Zygisk environment** (Zygisk Driver) is mandatory for this module to operate. You may refer to the following implementations:

*   **ZygiskNext**: [https://github.com/Dr-TSNG/ZygiskNext](https://github.com/Dr-TSNG/ZygiskNext.git)
*   **NeoZygisk**: [https://github.com/JingMatrix/NeoZygisk](https://github.com/JingMatrix/NeoZygisk.git)
*   **ReZygisk**: [https://github.com/PerformanC/ReZygisk](https://github.com/PerformanC/ReZygisk.git)

## Features
1.  **System Property Modification**: Universal application for mainstream Android devices.
2.  **Root Authorization Modes**: Provides two optional whitelist-based root modes on Magisk.
3.  **Mount Corrections**: Fixes and adjustments for non-compliant mount points.

## Configuration
To ensure system stability and prevent complex issues, **manual user-defined configuration files are not supported**. All configurations must be managed exclusively through the **KsuWebUI** interface.

*   **KsuWebUI Download**: [GitHub Releases](https://github.com/5ec1cff/KsuWebUIStandalone/releases)

### Authorization Modes
In the KsuWebUI dashboard, the Root authorization feature is labeled as **[SuList]**. The operation mode can be adjusted using the three-segment toggle in the upper right corner.

**[false]** (Default)
*   **Status**: Disabled.
*   **Description**: The SuList mode is inactive.

**[Std]**
*   **Status**: Standard Isolation.
*   **Mechanism**: Uses the native `FORCE_DENYLIST_UNMOUNT` command from the Zygisk API.

**[Plus]**
*   **Status**: Enhanced Isolation.
*   **Mechanism**: Utilizes `unshare` + `umount` to achieve a more robust isolation environment.

## Usage Notes
1.  **Non-Magisk Environments**
    If you are using a non-Magisk environment (e.g., KernelSU or APatch), please maintain the default **[SuList]** setting. Any modifications to this mode will strictly not take effect on these platforms.

2.  **Magisk DenyList Configuration**
    Before use, ensure that the **Enforce DenyList** option is **disabled** in Magisk settings. Additionally, verify that the DenyList itself is empty and that no applications are manually configured or checked within it.

## License & Contact

**Project Status: Closed Source**
This project is not distributed under any open-source license, and the developer is under no obligation to release the source code.

*   If you have strict security concerns or trust issues regarding closed-source software, strictly allow yourself to utilize other open-source Root hiding modules.
*   If you choose to place your trust in this project, we hope you enjoy the experience.

**Feedback & Support**
For feedback, bug reports, or inquiries, please reach out via Telegram:
**[@YukiFlowerOP](https://t.me/YukiFlowerOP)**
