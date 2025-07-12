# 📊 SQL_Insights.Gemini.Activities

**SQL_Insights.Gemini.Activities** is a custom UiPath activity that connects to a SQL Server database and retrieves analytical insights using Google Gemini API.

---

## 📦 Overview

This activity enables UiPath developers to:

- Securely connect to SQL Server using a `SecureString` connection string.
- Automatically extract and analyze the database schema.
- Generate valid SELECT queries based on a natural language prompt.
- Execute the query and get results.
- Ask Gemini to summarize or explain the results in natural language.

---

## ✅ Features

- 🔐 Handles secrets using `SecureString` (no hardcoded values).
- 🧠 Automatically generates SQL Server SELECT statements using Gemini.
- 📊 Retrieves and summarizes query results.
- 📦 Built as a UiPath Custom Activity using .NET 6 and Visual Studio.

---

## 🧾 Inputs

| Name             | Type         | Description                                                              |
|------------------|--------------|--------------------------------------------------------------------------|
| ConnectionString | SecureString | SQL Server connection string (from Credential/Secret asset).            |
| GeminiApiKey     | SecureString | Gemini API key to call the Gemini model securely.                        |
| GeminiModel      | String       | Name of Gemini model to use (e.g., `gemini-pro`).                         |
| UserPrompt       | String       | The insight or question you want to ask about your database content.     |

---

## 📤 Outputs

| Name     | Type   | Description                                     |
|----------|--------|-------------------------------------------------|
| Response | String | Gemini's response with insight or summarized data.|

---

## ⚙️ Dependencies

- `System.Data.SqlClient`
- `Newtonsoft.Json`
- `System.Net.Http`
- .NET 6 Runtime
- UiPath Studio 2022.10+

> 🧱 **Native Dependency Note**: You must copy [SNI.dll](https://github.com/AmrEzzatAbdo/SQL_Insights.Gemini.Activities/blob/main/sni.dll) to this location:
> `C:\Users\<YOUR_USERNAME>\AppData\Local\Programs\UiPath\Studio`

---

## 💡 Use Cases

- Business analysts or users can ask questions about databases without writing SQL.
- Generate reports or summaries from live data with Gemini.
- Automate insight generation from structured data.

---

## 🔧 How to Install

1. Download the `.nupkg` file from the [Releases](https://github.com/YOUR_REPO/releases).
2. Add the local path in UiPath Studio: `Manage Packages > Settings > User-defined package sources`.
3. Go to `Manage Packages > Available > Your Feed`, and install the activity.

---

## 📜 License

This project is licensed under the [MIT License].

---

## 👨‍💻 Author

Developed by **Amr Ezzat**

- LinkedIn: [linkedin.com/in/amr-ezzat](https://www.linkedin.com/in/amrezzatabdal-al/)
- Email: `amrezzat289@gmail.com`

---

> Feel free to contribute or open issues for improvements!
