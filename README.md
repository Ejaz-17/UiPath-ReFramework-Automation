# UiPath ReFramework Automation

An end-to-end automation built using UiPath’s **Robotic Enterprise Framework (ReFramework)**.  
This project reads input from Excel, uses Orchestrator Assets & Queues, processes transactions via a web portal, and writes back results to Excel. It includes robust error handling, retry logic, and Orchestrator integration.

---

## 🧰 Features

| Feature | Description |
|--------|-------------|
| ReFramework Architecture | Modular, scalable, and maintainable design |
| Excel Integration | Read input and write output back to Excel |
| Secure Credentials | Uses Orchestrator Assets to fetch credentials |
| Queue-based Processing | Handles multiple transactions through Orchestrator Queues |
| Web Portal Interaction | Logs in, submits data, retrieves generated number |
| Error Handling & Retry | Built-in exception handling and retry mechanism |
| Logging & Audit Trail | Logs detailed transaction info for debugging |

---

## 🎯 How It Works (Flow)

1. Read input data from Excel.  
2. Add transactions into an Orchestrator Queue (or process directly).  
3. For each queue item:
   - Fetch credentials from Orchestrator Assets  
   - Use web automation to login & submit data  
   - Retrieve generated number  
   - Update result in Excel  
4. Handle any failures using ReFramework’s built-in error states (Init, Get Transaction, Process, End).  
5. Log outcome of each transaction.

---

## 🧩 Setup & Configuration

1. Clone or download this repo.  
2. Open it in **UiPath Studio**.  
3. In Orchestrator:
   - Create **Assets** for credentials (username/password)  
   - Create a **Queue** for your transactions  
   - Provision a **Machine** and **Robot**, and assign permissions  
4. In the project `Config.xlsx`, update:
   - `OrchestratorQueueName`  
   - `AssetName`  
   - Excel input/output file paths  
5. Publish and run via UiPath Assistant or Orchestrator.

---



