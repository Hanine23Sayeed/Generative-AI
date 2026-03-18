# 🔍 AI-Powered Network Security Agent

> A conversational AI agent that performs network scanning using natural language — powered by LangChain, OpenAI GPT-4o, and Nmap.

---

## 📌 Overview

This project removes the complexity of network security scanning by wrapping **Nmap** — the industry-standard network scanning tool — inside an AI agent. Instead of memorizing technical commands, users simply describe what they want in plain English and the agent handles everything automatically.

**Example:**
```
User: "Show me all devices connected to my network"
Agent: Automatically selects the right tool, runs the scan, and returns a clean human-readable summary.
```

---

## ✨ Features

- 🗣️ **Conversational interface** — interact in plain English, no commands needed
- 🔎 **8 specialized scanning tools** — from quick scans to full vulnerability assessments
- 🧠 **AI-powered reasoning** — GPT-4o decides which scan to run based on your request
- ✅ **Input validation** — Pydantic ensures safe and clean inputs before any scan executes
- 🔄 **Tool calling architecture** — AI reasons, tools execute, results explained back to you

---

## 🛠️ Tech Stack

| Technology | Role |
|---|---|
| [LangChain](https://langchain.com) | Agent framework and tool orchestration |
| [OpenAI GPT-4o](https://openai.com) | Natural language understanding and reasoning |
| [Nmap](https://nmap.org) | Network discovery and security auditing |
| [Pydantic](https://docs.pydantic.dev) | Input validation and schema enforcement |
| Python | Core programming language |

---

## 🔧 Available Tools

| Tool | Description |
|---|---|
| `get_local_network_info` | Detects your local network, IP addresses, and scan ranges automatically |
| `nmap_scan` | General scan with full flexibility and custom options |
| `nmap_quick_scan` | Fast scan of the most common ports |
| `nmap_port_scan` | Targeted scan on specific ports |
| `nmap_service_detection` | Identifies software and services running on open ports |
| `nmap_os_detection` | Detects the operating system of a target device |
| `nmap_ping_scan` | Discovers all live hosts on a network without port scanning |
| `nmap_script_scan` | Runs advanced Nmap scripts for vulnerability detection |

---

## ⚙️ Installation

### 1. Clone the repository
```bash
git clone https://github.com/your-username/ai-network-security-agent.git
cd ai-network-security-agent
```

### 2. Install Python dependencies
```bash
pip install langchain langchain-openai pydantic
```

### 3. Install Nmap

**Windows:**
Download and install from [https://nmap.org/download.html](https://nmap.org/download.html)

**Linux:**
```bash
sudo apt install nmap
```

**macOS:**
```bash
brew install nmap
```

### 4. Set your OpenAI API key

Open the main file and replace:
```python
os.environ["OPENAI_API_KEY"] = "sk-your-api-key-here"
```

### 5. Set your Nmap path (Windows only)

If you are on Windows, find where Nmap is installed and set the path:
```python
NMAP_PATH = r"C:\Program Files (x86)\Nmap\nmap.exe"
```

To find the path automatically, run:
```python
import shutil
print(shutil.which("nmap"))
```

---

## 🚀 Usage

Run the agent:
```bash
python main.py
```

Or invoke it directly in your code:
```python
result = agent_executor.invoke({"input": "What devices are connected to my network?"})
print(result["output"])
```

### Example Queries

```
"What is my local network info?"
"Do a quick scan on 192.168.1.1"
"Scan ports 80, 443, and 8080 on 192.168.1.1"
"Detect what services are running on 192.168.1.1"
"What operating system is 192.168.1.1 running?"
"Run a vulnerability scan on 192.168.1.1"
"Run the http-title script on 192.168.1.1"
"Show all live devices on my network"
```

---

## 🏗️ Architecture

```
User (plain English)
        ↓
   GPT-4o (reasons about the request)
        ↓
   Selects the right tool
        ↓
   Tool executes Nmap scan
        ↓
   Raw output returned to GPT-4o
        ↓
   GPT-4o explains results to user
```

The AI is responsible for **reasoning and communication**.
The tools are responsible for **execution**.

---

## ⚠️ Disclaimer

This tool is intended for **authorized network scanning only**. Only scan networks and devices that you own or have explicit permission to scan. Unauthorized network scanning may be illegal in your country.

---

## 📄 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## 🤝 Contributing

Contributions are welcome! Feel free to open an issue or submit a pull request.

---

## 📬 Contact

If you have any questions or would like to discuss the project, feel free to reach out via LinkedIn or open an issue on GitHub.
