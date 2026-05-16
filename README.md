# Proxy Checker Pro

![Version](https://img.shields.io/badge/version-3.0-brightgreen)
![Python](https://img.shields.io/badge/python-3.6+-blue)
![License](https://img.shields.io/badge/license-MIT-orange)
![Platform](https://img.shields.io/badge/platform-Windows%20%7C%20Linux%20%7C%20macOS-lightgrey)
[![oosmetrics](https://api.oosmetrics.com/api/v1/badge/achievement/7b52afc2-c81d-4434-ab23-c384d137db05.svg)](https://oosmetrics.com/repo/NotAnyoneMe/ProxyChecker)
[![oosmetrics](https://api.oosmetrics.com/api/v1/badge/achievement/33fe5944-fb54-4302-b11c-17d6ecfd27fc.svg)](https://oosmetrics.com/repo/NotAnyoneMe/ProxyChecker)

A professional, feature-rich proxy checker application with a modern dark-themed GUI. Test HTTP, HTTPS, SOCKS4, and SOCKS5 proxies with real-time speed testing, country detection, and advanced verification methods.

<img width="1280" alt="Proxy Checker Pro Interface" src="https://github.com/user-attachments/assets/dcb0edd9-9033-4683-929d-3186965f7cf9" />

## 🏆 Achievements

> Ranked by [oosmetrics](https://oosmetrics.com/repo/NotAnyoneMe/ProxyChecker) based on repository growth acceleration.

| Badge | Achievement |
|-------|-------------|
| [![oosmetrics](https://api.oosmetrics.com/api/v1/badge/achievement/7b52afc2-c81d-4434-ab23-c384d137db05.svg)](https://oosmetrics.com/repo/NotAnyoneMe/ProxyChecker) | 🖥️ Top 10 in **Desktop** by acceleration — 2026-05-14 |
| [![oosmetrics](https://api.oosmetrics.com/api/v1/badge/achievement/33fe5944-fb54-4302-b11c-17d6ecfd27fc.svg)](https://oosmetrics.com/repo/NotAnyoneMe/ProxyChecker) | 🌐 Top 6 in **Network** by acceleration — 2026-05-14 |

## Features

### Core Functionality
- **Multiple Proxy Types**: HTTP, HTTPS, SOCKS4, SOCKS5
- **Flexible Input Formats**: 
  - `IP:PORT`
  - `IP:PORT:USER:PASS`
  - `USER:PASS:IP:PORT`
  - `IP PORT`
  - `HOST:PORT`
- **Authentication Support**: Full support for proxies with username/password
- **Real-time Testing**: HTTP request verification with custom test URLs
- **Speed Testing**: Measure proxy download speed in KB/s
- **Country Detection**: Automatic IP geolocation via API
- **Duplicate Removal**: Automatically filter duplicate proxies

### Advanced Features
- **Verification Methods**: 
  - HTTP Request (full functionality test)
  - Socket Connection (basic connectivity test)
- **Sorting Options**: Sort by IP, Port, Country, Speed, or Status
- **Export Options**: Save results as CSV or TXT
- **Customizable Settings**: 
  - Adjustable timeout values
  - Custom test URLs
  - Configurable verification methods
  - Speed check toggle
- **Modern Dark Theme**: Professional, eye-friendly interface with color-coded status

## Requirements

### Python Version
- Python 3.6 or higher

### Required Libraries
All required libraries are part of Python's standard library:
- `tkinter` - GUI framework (included with Python)
- `threading` - Concurrent proxy checking
- `socket` - Network connections
- `csv` - Export to CSV format
- `datetime` - Timestamp handling
- `re` - Regular expressions for parsing
- `urllib` - HTTP requests and proxy handling
- `json` - API response parsing

### System Requirements
- **Operating System**: Windows, Linux, or macOS
- **Memory**: 512 MB minimum
- **Display**: 1200x700 minimum resolution recommended
- **Internet Connection**: Required for country detection and proxy testing

## Installation

### Step 1: Clone the Repository
```bash
git clone https://github.com/NotAnyoneMe/ProxyChecker.git
cd ProxyChecker
```

### Step 2: Verify Python Installation
```bash
python --version
# or
python3 --version
```

Ensure you have Python 3.6 or higher installed.

### Step 3: Run the Application
```bash
python app.py
# or
python3 app.py
```

**Note**: No additional dependencies need to be installed. All required libraries are included with Python's standard library.

## Usage Guide

### Basic Workflow

**1. Load Proxies**
   - Click "Load Proxies" button in the Checker tab
   - Select your proxy list file (.txt format)
   - Choose the appropriate input format from the dropdown menu
   - Enable "Remove Duplicates" if needed

**2. Configure Settings**
   - Select proxy type: HTTP, HTTPS, SOCKS4, or SOCKS5
   - Set timeout value in seconds (default: 10)
   - Enable/disable "Check Speed" option
   - Choose output format for exports
   - Select sorting preference

**3. Start Checking**
   - Click "Start Check" to begin verification
   - Monitor real-time progress in the status bar
   - View results in the table with color-coded status:
     - Green = Working proxy
     - Red = Failed proxy
   - Use "Stop Check" to halt the process if needed

**4. Export Results**
   - Click "Save as CSV" for detailed reports with all columns
   - Click "Save as TXT" for a simple list of working proxies only

### Input File Format

Create a text file with your proxies, one per line. The application supports multiple formats:

```text
192.168.1.1:8080
10.0.0.1:3128:username:password
username:password:proxy.example.com:8080
203.0.113.5 8080
```

### Settings Configuration

Navigate to the **Settings** tab to customize:

- **Test URL**: Website used to verify proxy connectivity (default: https://www.google.com)
- **Speed Test URL**: File URL for download speed measurement (default: 100KB test file)
- **Default Timeout**: Maximum wait time per proxy in seconds
- **Concurrent Checks**: Thread count for parallel checking (display only in current version)
- **Verification Method**: 
  - HTTP Request: Full functionality test with actual web request
  - Socket Connection: Basic port connectivity test

## Use Cases

- **Web Scraping**: Find and validate reliable proxies for data collection projects
- **Privacy Testing**: Test proxy anonymity levels and connection speeds
- **Proxy Management**: Maintain and validate large proxy lists efficiently
- **Network Administration**: Verify proxy server functionality and performance
- **Security Research**: Test proxy configurations and security settings
- **Bot Development**: Source working proxies for automation tasks

## Advanced Configuration

### Custom Test URLs

You can specify custom URLs in the Settings tab to test proxies against specific websites or services:
- Social media platforms (Twitter, Facebook, Instagram)
- E-commerce sites (Amazon, eBay)
- API endpoints
- Geo-restricted content services
- Corporate intranets

### Speed Test Customization

Modify the speed test URL to use different file sizes based on your needs:
- **Small files (100KB)**: Quick speed checks, suitable for large proxy lists
- **Medium files (1-5MB)**: Balanced testing for moderate accuracy
- **Large files (10MB+)**: Accurate speed measurement, takes longer per proxy

### Output Format Options

Choose from multiple output formats:
- **IP:PORT** - Standard format
- **IP PORT** - Space-separated
- **IP,PORT** - Comma-separated (CSV compatible)

## Output Details

### CSV Export Format

The CSV export includes comprehensive information:

| Column | Description |
|--------|-------------|
| IP | IP address of the proxy (with auth username if applicable) |
| Port | Port number |
| Type | Proxy type (HTTP/HTTPS/SOCKS4/SOCKS5) |
| Country | Detected country via geolocation |
| Speed (KB/s) | Download speed measurement |
| Response Time | Time to establish connection |
| Status | Working or Failed with error details |

### TXT Export Format

Simple text file containing only working proxies in the selected output format:
```text
192.168.1.1:8080
10.0.0.1:3128
203.0.113.5:8080
```

## Troubleshooting

### Common Issues and Solutions

**Issue**: Proxies showing as "Failed" even though they are known to work
- **Solution 1**: Increase timeout value in settings (try 15-30 seconds)
- **Solution 2**: Switch verification method from HTTP Request to Socket Connection
- **Solution 3**: Check if the test URL is accessible from your location
- **Solution 4**: Some proxies may require specific authentication formats

**Issue**: Country shows as "Unknown" for all proxies
- **Solution 1**: Verify your internet connection is active
- **Solution 2**: Check if ip-api.com is accessible from your network
- **Solution 3**: Some private IP addresses won't have geolocation data
- **Solution 4**: API rate limiting may occur with very large proxy lists

**Issue**: Speed test shows "N/A" for all proxies
- **Solution 1**: Ensure the speed test URL is accessible and returns data
- **Solution 2**: Increase timeout value as slow proxies may timeout
- **Solution 3**: Disable speed checking if not needed to speed up verification
- **Solution 4**: Some proxies block file downloads

**Issue**: Application window not displaying correctly
- **Solution 1**: Verify minimum screen resolution (1200x700)
- **Solution 2**: Check display scaling settings in your OS
- **Solution 3**: Try maximizing the window

**Issue**: Application not starting or crashes on launch
- **Solution 1**: Verify Python 3.6+ is installed: `python --version`
- **Solution 2**: Check tkinter availability: `python -m tkinter`
- **Solution 3**: On Linux, install tkinter: `sudo apt-get install python3-tk`
- **Solution 4**: Check console for error messages

**Issue**: Checking process is very slow
- **Solution 1**: Reduce timeout value for faster checking
- **Solution 2**: Disable speed checking if not needed
- **Solution 3**: Use Socket Connection method instead of HTTP Request
- **Solution 4**: Check proxy list for invalid entries

## Contributing

Contributions are welcome and appreciated! Here's how you can help improve Proxy Checker Pro:

### How to Contribute

1. **Fork the repository** on GitHub
2. **Clone your fork** locally: `git clone https://github.com/YOUR-USERNAME/ProxyChecker.git`
3. **Create a feature branch**: `git checkout -b feature/AmazingFeature`
4. **Make your changes** and test thoroughly
5. **Commit your changes**: `git commit -m 'Add some AmazingFeature'`
6. **Push to your branch**: `git push origin feature/AmazingFeature`
7. **Open a Pull Request** with a clear description of changes

### Areas for Contribution

- **Additional proxy types**: SOCKS4A support, HTTP/2 proxies
- **Enhanced speed testing**: More accurate algorithms, multiple test files
- **Improved country detection**: Alternative APIs, local database support
- **GUI improvements**: Themes, translations, accessibility features
- **Performance optimizations**: Multi-threading implementation, memory efficiency
- **Export formats**: JSON, XML, database export options
- **Proxy chain support**: Test multiple proxy hops
- **Scheduling**: Automated periodic checking
- **Statistics**: Charts and graphs for results analysis
- **Bug fixes**: Report and fix issues
- **Documentation**: Improve guides and examples

### Code Style Guidelines

- Follow PEP 8 style guidelines
- Add comments for complex logic
- Update documentation for new features
- Test changes before submitting
- Keep commits focused and atomic

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for full details.

### MIT License Summary

You are free to:
- Use the software for any purpose
- Modify the source code
- Distribute copies
- Use the software commercially

The software is provided "as is", without warranty of any kind.

## Developer

**Developed by MLBOR**

- **Telegram**: [@MLBOR](https://t.me/MLBOR)
- **GitHub**: [github.com/NotAnyOneMe](https://github.com/NotAnyOneMe)

For questions, suggestions, or support, feel free to reach out via Telegram or GitHub.

## Support Development

If you find this tool useful and would like to support its continued development, cryptocurrency donations are greatly appreciated:

### Cryptocurrency Addresses

**TON (The Open Network)**
```
UQD-XUfoicqCzV-RCI6RkEzTO0iNi92ahMUSQ8l27s42LcVf
```

**LTC (Litecoin)**
```
ltc1qtl2tjdacrwk3r2qutl408quqwzeejv29jrvnnl
```

**BTC (Bitcoin)**
```
bc1q6y0qx6xhla2w9utlqusyzpskn0mdvfgzwchg50
```

**ETH (Ethereum)**
```
0xe3C42C6AF102fFDf6856DC2df3Ec7D009F4Eb31B
```

Your support helps maintain and improve this project. Thank you!

## Star This Repository

If you find Proxy Checker Pro useful, please consider giving it a star on GitHub. It helps others discover the tool and motivates continued development.

## Contact & Support

- **Bug Reports**: Submit via [GitHub Issues](https://github.com/NotAnyoneMe/ProxyChecker/issues)
- **Feature Requests**: Open an issue with the "enhancement" label
- **Direct Support**: Contact via Telegram [@MLBOR](https://t.me/MLBOR)
- **Discussions**: Join conversations in [GitHub Discussions](https://github.com/NotAnyoneMe/ProxyChecker/discussions)

## Changelog

### Version 3.0 - Ultimate Edition (Current)
- Multiple proxy type support (HTTP, HTTPS, SOCKS4, SOCKS5)
- Authentication support with flexible input formats
- Real-time speed testing with configurable URLs
- Automatic country detection via geolocation API
- Modern dark theme with professional styling
- Multiple input and output format options
- Color-coded status indicators (green/red)
- Real-time progress tracking
- Dual verification methods (HTTP/Socket)
- Export to CSV and TXT formats
- Sorting by multiple criteria
- Duplicate removal functionality

### Future Roadmap
- Multi-threading for faster checking
- Proxy chain testing
- Export to additional formats (JSON, XML)
- Statistics and analytics dashboard
- Scheduled checking
- Proxy rotation testing
- Advanced filtering options

---

<div align="center">

**Made with care by MLBOR**

**Give this project a star if you find it useful!**

[Report Bug](https://github.com/NotAnyoneMe/ProxyChecker/issues) · [Request Feature](https://github.com/NotAnyoneMe/ProxyChecker/issues) · [Contribute](https://github.com/NotAnyoneMe/ProxyChecker/pulls)

</div>