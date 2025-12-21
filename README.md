# 📡 Sonar: A Real-Time Anomaly Detection Tool

**Sonar** is a high-performance security monitoring tool designed to scan Windows event logs in real-time against an extensive **[Sigma](https://sigmahq.io/)** ruleset.

---

## Features

- **Real-Time:** Unlike traditional batch-processing tools, Sonar monitors event logs as they are generated, minimizing the "detection gap".
- **Extensive Ruleset:** Leverages the battle-tested [Hayabusa rules](https://github.com/Yamato-Security/hayabusa-rules) from Yamato Security.
- **Lightweight:** 7MB dependency-free executable.
- **Offline:** Designed to work with air-gapped environments.
- **Export Capabilities:** Query detections by rule name, severity, keywords, and export them into JSON files.

---

## Getting Started

### Prerequisites

- Windows 8.1+ or Windows Server 2012 R2+.
- (Optional/Recommended) Administrator privileges to read Security logs.

### Usage

1. Download Sonar [here](https://github.com/Saeros-Security/Sonar/releases).
2. Run Sonar.exe and choose which Sigma profile to use:
   - Core: High-quality rules that are unlikely to generate false positives.
   - Core+: Rules that may inadvertently match legitimate applications.
   - Core++: Rules that aim to detect threats as early as possible leading to a higher volume of false positives.

Each detection appears in the console and is stored in a local SQLite database located in `./Database/detections.db`.

<table>
  <tr>
    <td valign="top"><img src="https://github.com/user-attachments/assets/6f7fae8a-8b1c-4824-94c5-f1ce1fc9fbf4"/></td>
  </tr>
</table>

#### Export (Keystroke `E`)

Hit `E` to export detections based on:

- Rule name: Performs a search by Sigma rule.
- Severity: Performs a search by level (Informational, Low, Medium, High, Critical).
- Keyword: Performs a full-text search across event log properties.

#### Dashboard (Keystroke `S`)

Hit `S` to display detection statistics:

- Detection count by computer.
- Detection count over time.
- Top detection rules by severity.

<table>
  <tr>
    <td valign="top"><img src="https://github.com/user-attachments/assets/63d5ffc1-6cb9-4531-81a6-cdfe222a8058"/></td>
  </tr>
</table>

#### Help (Keystroke `H`)

Hit `H` to display help.

---

## License

Distributed under the GPLv3 License.
