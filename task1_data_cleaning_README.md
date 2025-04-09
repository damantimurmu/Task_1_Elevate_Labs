# Task 1: Data Cleaning and Preprocessing

## Objective
Clean and prepare a real-world dataset containing patient appointment records to make it ready for analysis and visualization.

---

## Dataset
**Source**: [Medical Appointment No Shows (Kaggle)](https://www.kaggle.com/datasets/joniarroba/noshowappointments)

**File**: `medical_appointment_no_shows.csv`  
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

## Tools Used
- Excel
- Python (Pandas)

---

## Cleaning Steps Performed

### Methode used in Excel:

| Task | Method Used |
|------|-------------|
| Handled Missing Values | `- Use the filter feature on each column.`
`-Identify blank cells in columns like age, neighbourhood, or others.`
`- Fill them if possible, or remove rows where data is critical.` |
| Removed Duplicates | `.drop_duplicates()` |
| Standardized Text (e.g., `gender`) | `.str.lower()` |
| Converted Date Columns (`scheduledday`, `appointmentday`) | `pd.to_datetime()` |
| Renamed Columns | Lowercase, underscores used instead of spaces |
| Data Type Fixes | Age → `int`, Dates → `datetime64[ns]` |

### Method used in Python:

| Task | Method Used |
|------|-------------|
| Handled Missing Values | `.isnull().sum()` |
| Removed Duplicates | `.drop_duplicates()` |
| Standardized Text (e.g., `gender`) | `.str.lower()` |
| Converted Date Columns (`scheduledday`, `appointmentday`) | `pd.to_datetime()` |
| Renamed Columns | Lowercase, underscores used instead of spaces |
| Data Type Fixes | Age → `int`, Dates → `datetime64[ns]` |

---

## Cleaned Dataset Output
- File: `cleaned_medical_appointment_no_shows.csv`
- Total rows: `110528` (no duplicated found)
- Column formats standardized and validated

---

## Notes
- `no_show` was kept as-is but might be re-encoded (Yes/No → 1/0) in further analysis
- Checked and corrected unusual ages (e.g., negative or very high)

---

## Repository Structure

| File/Folder | Description |
|-------------|-------------|
| `raw_data/medical_appointment_no_shows.csv` | Raw dataset |
| `cleaned_data/cleaned_medical_appointment_no_shows.csv` | Cleaned dataset |
| `notebooks/data_cleaning.ipynb` | Python cleaning code |
| `excel/cleaning_steps.xlsx` | Excel version of cleaning process |
| `summary.md` | Summary of all cleaning actions |

---

## Maintained by
**Damanti Murmu**  
Aspiring Business and Data Analyst |
[LinkedIn](https://www.linkedin.com/in/damantimurmu/)
