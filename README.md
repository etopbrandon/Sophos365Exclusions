<!-- ABOUT THE PROJECT -->
## About The Project

This project is a collection of Sophos XG/XGS Firewall web policy exclusions for common Microsoft 365 services. The most common issue this solves is errors when attempting to download Office updates or install new software with the C2R client. Update/Install files are sent as .CABs, which Sophos will block in the default protection rules as "System Files" under the "Risky Downloads" policy. These exclusions also ensure other common 365 resources are allowed. 

Sophos has published an import, but they had broken the rules up into *145 individual exclusion entries*, all disabled, which not only polluted the list of exclusions but was also time consuming to individually enable. This edited import file has trimmed out legacy/retired/uncommon services, and consolidated all excluded Regex URL patterns to a total of four top level entries. 




<!-- GETTING STARTED -->
## Getting Started

To import this file to your Sophos XG/XGS firewall, follow this guide. This guide was created with information current with SFOS v19.5

### Prerequisites

You must have a Sophos XG firewall with licensing for Web Protection. It is recommended to take a backup of your existing configuration before making changes

### Installation

1. Download the `SophosFixed365Exclusions.tar` file. Do not extract it
2. Launch the SFOS console as an administrator
3. Navigate to `Backup & Firmware` in the left nav bar under "SYSTEM"
4. Select the `Import Export` tab
5. Click  **Choose** **File** and browse for the `SophosFixed365Exclusions.tar`  file
6. Select and Import the file

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- USAGE EXAMPLES -->
## Usage

The import will add four exclusions containing many Regex URL matching entries. These imported rules will be imported as **Disabled**. You *must* complete the following steps to enable them:

1. In SFOS, navigate to `Web` in the left navbar under "PROTECT"
2. Select the `Exceptions` tab
3. Enable the following exceptions by toggling the On/Off switch on the right:
	- O365 - 1 (Exchange)
	- O365 - 2 (Collaboration - Allow)
	- O365 - 3 (Azure/Microsoft365 General - Allow)
	- O365 - 4 (Storage)

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- CONTRIBUTING -->
## Contributing

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

If you have a suggestion that would make this better, please fork the repo and create a pull request. 
Don't forget to give the project a star! Thanks again!

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- LICENSE -->
## License

Distributed under the GNU GPLv3 License. See `LICENSE` for more information.

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- CONTACT -->
## Contact

Brandon Martinez - eTop Technology
brandon@etoptechnology.com
Giga#4634

Project Link: [https://github.com/etopbrandon/Sophos365Exclusions](https://github.com/etopbrandon/Sophos365Exclusions)

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- ACKNOWLEDGMENTS -->
## Acknowledgments

* [Sophos](https://www.sophos.com/)
* [MSPGeek Community](https://discord.gg/mspgeek)

<p align="right">(<a href="#readme-top">back to top</a>)</p>
