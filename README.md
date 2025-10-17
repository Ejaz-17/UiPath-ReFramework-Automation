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
   - Excel input/output file paths  <p align="center">
  <img src="https://uipath.com/hubfs/ui-path-logo.svg" width="120"/>
</p>

<h2 align="center">🤖 UiPath ReFramework Automation</h2>

<p align="center">
  A complete end-to-end automation built using UiPath’s <b>Robotic Enterprise Framework (ReFramework)</b>.  
  This project integrates Excel data, Orchestrator Assets & Queues, and web portal automation — all wrapped with  
  robust exception handling, retry logic, and logging for enterprise-grade reliability.
</p>

---

## 🧰 Features

| Feature | Description |
|----------|--------------|
| ⚙️ **ReFramework Architecture** | Modular, scalable, and maintainable design |
| 📊 **Excel Integration** | Reads input and writes results back to Excel |
| 🔐 **Secure Credentials** | Uses Orchestrator Assets to fetch credentials securely |
| 📦 **Queue-based Processing** | Manages transactions efficiently through Orchestrator Queues |
| 🌐 **Web Portal Interaction** | Automates login, data submission, and number retrieval |
| 🧱 **Error Handling & Retry** | Built-in exception handling and retry mechanism |
| 📝 **Logging & Audit Trail** | Tracks transaction logs for monitoring and debugging |

---

## 🎯 How It Works

1. **Read Input:** Load data from an Excel file.  
2. **Queue Setup:** Add each record as a transaction item in Orchestrator Queue.  
3. **Process Transaction:**  
   - Fetch credentials from Orchestrator Assets  
   - Log into the web portal  
   - Submit form data and retrieve the generated number  
   - Write results back to Excel  
4. **Error Recovery:**  
   - Handled automatically through ReFramework’s `Init`, `Get Transaction`, `Process`, and `End` states  
5. **Log Results:** Every step is logged in detail for transparency.

---

## ⚙️ Setup & Configuration

1. **Clone or Download** this repository.  
2. Open the project in **UiPath Studio**.  
3. Configure Orchestrator:  
   - Create **Assets** for credentials (Username/Password)  
   - Create a **Queue** for transactions  
   - Provision a **Machine** and **Robot**, and assign appropriate permissions  
4. Update the following in `Config.xlsx`:  
   - `OrchestratorQueueName`  
   - `AssetName`  
   - Excel input/output file paths  
5. **Publish & Run:** Execute via UiPath Assistant or directly from Orchestrator.

---

## 📂 Folder Structure

Project/
├── Config.xlsx
├── Data/
│ ├── Input.xlsx
│ └── Output.xlsx
├── Framework/
│ ├── InitAllSettings.xaml
│ ├── GetTransactionData.xaml
│ ├── Process.xaml
│ └── EndProcess.xaml
├── Main.xaml
└── README.md

---

## 🎥 Demo / Screenshot

*(Optional – Add your workflow image or demo video here)*  
Example:
```md
![Workflow Screenshot](assets/demo.png)
🧠 Built With
UiPath Studio

UiPath Orchestrator

Robotic Enterprise Framework (REFramework)

Excel Activities

Selenium Web Automation

📜 License
This project is open-source under the MIT License.

<p align="center"> Developed with ❤️ by <b>Ejaz Ahmed</b> <br> <a href="https://github.com/Ejaz-17">GitHub Profile</a> </p> ```
5. Publish and run via UiPath Assistant or Orchestrator.

---




