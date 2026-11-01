# ChronoFence

**ChronoFence** is a zero-dependency, client-side browser application designed for local environmental diagnostics, timing measurements, hardware profiling, and performance benchmarking. 

It runs entirely in the browser using local workers, WebAssembly, and native web APIs with strict privacy guarantees—no data or telemetry is stored or transmitted externally.

---

## Features

- **Local Timing & CPU Diagnostics**: Measures minimum positive positive clock resolution (`performance.now()`), floating-point workload sample means, standard deviations, and animation-frame interval consistency.
- **WebGL & Hardware Profiling**: Queries unmasked WebGL vendors/renderers, checks graphics pipeline markers (e.g., software rasterizers, virtual machines), and reads browser-reported hardware concurrency and memory hints.
- **Consent-Based Screen Share & Frame Monitoring**: Observes local browser-reported display stream metadata and tracks presented-frame timing via `requestVideoFrameCallback` without recording or saving pixel/audio content.
- **Cryptographic Benchmarks**: Multi-threaded synthetic performance tests running **AES-GCM** via Web Crypto and **ChaCha20** blocks via embedded **WebAssembly** in background workers.
- **Media Device Audit**: Lists browser-exposed audio/video inputs and outputs without requesting immediate capture permission.
- **Optional Loopback Probes**: Real local HTTP (`no-cors`) and WebSocket connections targeting `127.0.0.1` on user-specified ports.

---

## Getting Started

Because ChronoFence is built as a single standalone HTML file containing embedded styles, scripts, and WebAssembly payloads, no complex build steps or Node.js toolchains are strictly required.

### Running Locally
1. Clone the repository:
   ```bash
   git clone [https://github.com/username/ChronoFence.git](https://github.com/username/ChronoFence.git)
   cd ChronoFence
