# PingIt - Network Monitor

A real-time network monitoring tool built with vanilla JavaScript that allows you to check website availability, latency, and response times with a clean, modern UI.

![PingIt Interface - 1](/assets/01.png)
![PingIt Interface - 2](/assets/02.png)


[Live Demo](https://pingit-xi.vercel.app)

## Features

- **Real-time Monitoring**: Continuously monitor website availability and performance
- **Latency Tracking**: Measure and track network latency over time
- **Response Time Analysis**: Monitor website response times with detailed metrics
- **Visual Analytics**: 
  - Interactive charts showing latency and response time history
  - Color-coded status indicators
  - Comprehensive history table
- **Error Handling**: Robust error detection and reporting with automatic retry capability
- **Cross-Origin Support**: Works with CORS-enabled and restricted sites
- **Responsive Design**: Clean, modern UI that works on all device sizes

## Technology Stack

- Vanilla JavaScript (ES6+)
- Chart.js for data visualization
- TailwindCSS for styling
- No backend required - runs entirely in the browser

## Installation

1. Clone the repository:
```bash
git clone https://github.com/jeffasante/pingit.git
cd pingit
```

2. Open with a local server:
```bash
# Using Python
python -m http.server 5500

# Or using Node.js http-server
npx http-server
```

3. Visit `http://localhost:5500` in your browser

## Usage

1. Enter a URL in the input field (e.g., "google.com" or "https://example.com")
2. Click "Check Status" or press Enter
3. Monitor real-time statistics:
   - Current latency
   - Site status
   - Response time
   - Historical data

## Key Components

### NetworkStatusChecker Class

The core functionality is handled by the `NetworkStatusChecker` class, which provides:

- Configurable ping intervals and timeouts
- Automatic retry attempts for failed checks
- Event-based status updates
- Error handling and reporting

### Features in Detail

1. **URL Validation and Formatting**
   - Automatic protocol (https://) addition if not specified
   - URL format validation

2. **Status Monitoring**
   - Site availability checking
   - Latency measurement
   - Response time tracking
   - Status code reporting

3. **Data Visualization**
   - Real-time chart updates
   - Historical data tracking
   - Performance trending

4. **Error Handling**
   - CORS compatibility
   - Network error detection
   - Timeout management
   - Automatic retries

## Configuration

Key constants that can be modified:

```javascript
const MAX_DATA_POINTS = 20;  // Maximum number of historical data points
const CHART_UPDATE_INTERVAL = 5000;  // Update interval in milliseconds

// NetworkStatusChecker options
{
  pingInterval: 5000,    // How often to check (ms)
  timeout: 5000,         // Request timeout (ms)
  retryAttempts: 2,      // Number of retry attempts
  retryDelay: 1000      // Delay between retries (ms)
}
```

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- Chart.js for the charting library
- TailwindCSS for the UI framework