# Pulse

This is a node.js based resource monitor that utilises the native 'os' module in node.js to access system resource usage i.e. RAM, CPU etc. It provides real-time hardware performace, averaging and automated alerting.

# Overview

Pulse implements a reactive monitoring loop. Pulse polls the OS for memory and CPU usage, maintains a historical buffer to calculate performance trends and triggers async file-system events when hardware thresholds are exceeded.

# Key Features

- Real-time Telemetry: live tracking of RAM usage and CPU load average
- Trend analysis: implements a rolling history buffer to calculate the moving averages(stateful)
- Non-blocking logging: uses node's asyn 'fs' to log critical alerts without interrupting the monitoring cycle.

# Technical Stack

- Runtime: Node.js
- Core Modules: os (hardware interfacing), fs(asyn I/O), process(stdout control)
- Logic: Event-loop scheduling, data buffering and performace threshold.

# Usage

1. clone repo
2. npm install
3. run npx tsc
4. run npm run dev
