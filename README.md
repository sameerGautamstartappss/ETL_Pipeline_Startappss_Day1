# ETL_Pipeline_Startappss_Day1
Absolutely! Here's your **cleaned-up `README.md` without License and Developer info**, ready to use:

---

```markdown
# 🚀 ETL Project — JSON & CSV Validation Pipeline

An ETL pipeline for validating and processing JSON metadata and CSV data files using Python.

---

---

## 🔄 ETL Pipeline Flow (Visualized with Mermaid)

```mermaid
flowchart LR
    A[📥 Input Files<br>JSON & CSV arrive in Input Folder] --> B[✅ Validate<br>Check JSON Metadata & CSV Data Integrity]
    B -->|Validation Passed| C[📊 Process<br>Transform & Clean Data]
    C --> D[📤 Move to Output<br>Store in Output Folder]
    B -->|Validation Failed| E[🚫 Move to Issue<br>Log & Move Files to Issue Folder]
````

---

## 💻 Code Components

| Module           | Purpose                                  |
| ---------------- | ---------------------------------------- |
| `main.py`        | Orchestrates the ETL workflow            |
| `validator.py`   | Contains validation logic for JSON & CSV |
| `filehandler.py` | Handles file movement (Issue/Output)     |
| `logger.py`      | Logs pipeline activities                 |
| `config/*.json`  | Holds validation rules & settings        |

---

## ⚙️ Processing Logic

1️⃣ **Input**
JSON metadata and CSV data files are placed inside the `input/` folder.

2️⃣ **Validation**

* `validate_json_metadata()` checks if required fields exist and formats are correct.
* `validate_csv_data()` checks for required columns, datatypes, and missing values.

3️⃣ **Processing**

* If validation passes, files are moved to `output/`
* If validation fails, files are moved to `Issue/` with a reason file

---

## 📝 Validation Flow (Mermaid Diagram)

```mermaid
graph TD
    Start[📁 New Files Detected] --> CheckJSON[🔍 Validate JSON Metadata]
    CheckJSON -->|Valid| CheckCSV[🔍 Validate CSV Data]
    CheckJSON -->|Invalid| MoveJSONIssue[🚫 Move JSON to Issue Folder]
    CheckCSV -->|Valid| MoveOutput[✅ Move JSON & CSV to Output]
    CheckCSV -->|Invalid| MoveCSVIssue[🚫 Move CSV & JSON to Issue Folder]
```

---

## 📜 Logs and Error Handling

* Logs are maintained in `logs/pipeline.log`
* Detailed error reasons are saved alongside moved files in `Issue/`

---

## ✅ How to Run the Pipeline

```bash
cd etl_project_16July/src/main
python main.py
```

---

## ✅ Dependencies

* Python 3.8+
* pandas

Install via:

```bash
pip install pandas
```

---

## 📊 Sample Output Screenshot

<img width="848" height="891" alt="image" src="https://github.com/user-attachments/assets/dc773e42-be9c-4e33-8e92-6397a5a7f213" />
<img width="869" height="602" alt="image" src="https://github.com/user-attachments/assets/e1dbb771-d40a-4b16-8201-4622761d2774" />
<img width="817" height="145" alt="image" src="https://github.com/user-attachments/assets/2115ec32-86c3-4275-9615-9b2741ac5553" />

---

```

---

Let me know if you want:
- Sample config JSON content  
- Mermaid diagram for folder structure  
- Badge icons for build/pipeline status
```

