<img src="https://img.shields.io/badge/Android%2B-3DDC84?style=for-the-badge&logo=android&logoColor=white"/>
<img src="https://img.shields.io/badge/Kotlin-7F52FF?style=for-the-badge&logo=kotlin&logoColor=white"/>

<img width="1651" height="1969" alt="imagee" src="https://github.com/user-attachments/assets/a334ab3a-34b3-4803-a83d-084865a9868d" />

> ⚠️ **FOR EDUCATIONAL AND AUTHORIZED SECURITY TESTING ONLY** ⚠️

## 🎯 About The Project

**BLEDroid** is a powerful Android application designed for network security
to evaluate Bluetooth environment resilience through controlled,
high-frequency scan cycles. Built with **Kotlin** and leveraging Android's official
`BluetoothLeScanner` and `BluetoothAdapter` APIs, this tool stress-tests Bluetooth
infrastructure to identify potential vulnerabilities — no root required.

Similar project of **WifiDroid**, sharing the same Tailwind-inspired dark UI, MVVM
architecture, coroutine-based engine, and legal safeguards — now in **deep blue**.

## 🔑 Key Differentiators

| Feature | Details |
|---|---|
| ✅ **No Root Required** | Operates entirely within Android's security framework |
| ⚡ **Three Scan Modes** | BLE only / Classic only / Dual (simultaneous) |
| 🔵 **BLE + Classic** | Covers both `BluetoothLeScanner` and `BluetoothAdapter.startDiscovery()` |
| 🎯 **Smart BLE Filters** | Filter by ALL devices, device name prefix, or MAC address |
| 🛡️ **Permission Safe** | Runtime permission checks + `SecurityException` handling on every call |
| 📊 **Live Analytics** | Cycles, devices found, unique devices, cycles/s, failures |
| 🎨 **Tailwind Blue Dark Theme** | Material Design 3 with Tailwind CSS blue/slate palette |
| 🔒 **Privacy Focused** | Zero data collection, no external connections |

## ✨ Features

### Core Functionality

- 🔄 **Automated Stress Testing** — Configurable iteration counts (1–1000+)
- ⏱️ **Adjustable Scan Window** — 100ms to 5000ms per cycle
- 📈 **Real-time Monitoring** — Live progress bar, cycles/s, elapsed time
- 📝 **Colored Terminal Log** — Timestamped entries with color-coded levels (success/error/warning/debug)
- 🎯 **BLE Device Filtering** — ALL / By name prefix / By MAC address
- 🚀 **Coroutine Architecture** — Non-blocking engine with `Dispatchers.IO` + `StateFlow` / `SharedFlow`

### 📡 Scan Modes

| Mode | API Used | Best For |
|---|---|---|
| 🔵 **BLE Only** | `BluetoothLeScanner.startScan()` | IoT devices, wearables, beacons |
| 🟣 **Classic Only** | `BluetoothAdapter.startDiscovery()` | Phones, headsets, speakers |
| 🔀 **Dual** | Both simultaneously | Full environment coverage |

### 📊 Live Metrics

- Total scan cycles completed
- Total devices found (cumulative)
- Unique devices discovered (by MAC address)
- Scan cycles per second (real-time)
- Total elapsed time
- Failure count with error categorization

### 🛡️ Safety Mechanisms

- Emergency stop button (mid-test abort)
- Permission validation before **every** scan call
- Graceful `SecurityException` handling — no crashes on permission loss
- Auto-abort if permission revoked mid-test

### 🎨 User Interface

- Tailwind CSS blue dark theme
- Material Design 3 components (Cards, TextInput, SeekBar, ProgressBar)
- Scan Mode + BLE Filter spinners
- Filter value input for name/MAC filtering
- Configurable iterations (1–1000) and scan window (100ms–5s)
- Scrollable colored terminal-style activity log
- Live 2×3 metrics grid

### Permissions Required

| Permission | API Level | Purpose |
|---|---|---|
| `BLUETOOTH` | ≤ API 30 | Basic Bluetooth access |
| `BLUETOOTH_ADMIN` | ≤ API 30 | Start/stop discovery |
| `ACCESS_FINE_LOCATION` | ≤ API 30 | Required for BLE scanning |
| `BLUETOOTH_SCAN` | API 31+ | BLE and Classic scanning |
| `BLUETOOTH_CONNECT` | API 31+ | Read device name/address |
| `BLUETOOTH_ADVERTISE` | API 31+ | Future advertising support |
