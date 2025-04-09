# 🧼 Task 1: Data Cleaning and Preprocessing

## 🎯 Objective
Clean and prepare a real-world dataset containing patient appointment records to make it ready for analysis and visualization.

---

## 📁 Dataset
**Source**: [Medical Appointment No Shows (Kaggle)](https://www.kaggle.com/datasets/joniarroba/noshowappointments)

**File**: `medical_appointments.csv`  
**Columns**:
- `patientid`
- `appointmentid`
- `gender`
- `scheduledday`
- `appointmentday`
- `age`
- `neighbourhood`
- `scholarship`
- `hipertension`
- `diabetes`
- `alcoholism`
- `handcap`
- `sms_received`
- `no_show`

---

## 🛠️ Tools Used
- Excel
- Python (Pandas)

---

## 🧪 Cleaning Steps Performed

| Task | Method Used | Tools |
|------|-------------|-------|
| Handled Missing Values | `.isnull().sum()` | Python |
| Removed Duplicates | `.drop_duplicates()` | Python & Excel |
| Standardized Text (e.g., `gender`) | `.str.lower()` | Python |
| Converted Date Columns (`scheduledday`, `appointmentday`) | `pd.to_datetime()` | Python |
| Renamed Columns | Lowercase, underscores used instead of spaces | Python |
| Data Type Fixes | Age → `int`, Dates → `datetime64[ns]` | Python |

---

## ✅ Cleaned Dataset Output
- File: `cleaned_medical_appointments.csv`
- Total rows: `XXXX` (after removing duplicates/nulls)
- Column formats standardized and validated

---

## 📌 Notes
- `no_show` was kept as-is but might be re-encoded (Yes/No → 1/0) in further analysis
- Checked and corrected unusual ages (e.g., negative or very high)

---

## 📥 Repository Structure

| File/Folder | Description |
|-------------|-------------|
| `data/medical_appointments.csv` | Raw dataset |
| `data/cleaned_medical_appointments.csv` | Cleaned dataset |
| `notebooks/data_cleaning.ipynb` | Python cleaning code |
| `excel/cleaning_steps.xlsx` | Excel version of cleaning process |
| `summary.md` | Summary of all cleaning actions |

---

## 👩‍💻 Maintained by
**Ayushi Gupta**  
Raja Jwala Prasad Postdoctoral Fellow  
[LinkedIn](https://linkedin.com/in/Dr-Ayushi-Gupta) | [ResearchGate](https://www.researchgate.net/profile/Ayushi-Gupta-15)
