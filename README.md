# Task 1: Data Cleaning and Preprocessing

## Objective
Clean and prepare a real-world dataset containing patient appointment records to make it ready for analysis and visualization.

---

## Dataset
**Source**: [Medical Appointment No Shows (Kaggle)](https://www.kaggle.com/datasets/joniarroba/noshowappointments)

**File**: `medical_appointment_no_shows.csv`  
**Columns**:
- `PatientId`
- `AppointmentID`
- `Gender`
- `Scheduledday`
- `Appointmentday`
- `Age`
- `Neighbourhood`
- `Scholarship`
- `Hipertension`
- `Diabetes`
- `Alcoholism`
- `Handcap`
- `SMS_received`
- `No_show`

---

## Tools Used
- Excel
- Python (Pandas)

---

## Cleaning Steps Performed

## Methode used:

| Task | Excel | Python |
|------|-------|--------|
| Handled Missing Values | `filter` |  `df.isnull().sum()` |
| Searching Duplicates | `Conditional Formatting` | `df.duplicated().sum` |
| Removed Duplicates | `Remove Dublicates` | `df.drop_duplicates()` |
| Standardized column value (e.g., `Neighbourhood`) | `LOWER()` and `UPPER()` |  `df[].str.title()` or `df[].str.lower()`|
| Converted Date Columns (`scheduledday`, `appointmentday`) | `Flash fill` and `LEFT()` formulas | `pd.to_datetime(df['ScheduledDay']).dt.strftime('%d-%m-%Y')` |
| Renamed Columns | `=LOWER()` and underscores used instead of spaces | `df.columns = [col.strip().lower().replace(" ", "_") for col in df.columns]` |
| Data Type Fixes | Age → `int`, Dates → `datetime` | Elaborated in `data_cleaning_README.md` |
| Filter Out Invalid Data | Age → `filter`, and row `removed` | `df[(df['age'] >= 0) & (df['age'] <= 100)]` |

---

## Cleaned Dataset Output
- File: `cleaned_medical_appointment_no_shows.csv`
- Original rows: `110527`
- Rows after removing rows with invalid ages: `106987`
- No. of invalid removed: `3540`
- Total rows: `106987` (no duplicated found)
- Column formats standardized and validated

---

## Repository Structure

| File/Folder | Description |
|-------------|-------------|
| `raw_data/medical_appointment_no_shows.csv` | Raw dataset |
| `excel/README.md` and `cleaned_medical_appointment_no_shows.csv` | `Excel version of the cleaning process` and cleaned CSV file by Excel |
| `notebooks/README.md`, `cleaned_medical_appointment_no_shows2.csv` and `data_cleaning.ipynb` | Python cleaning code and `Python version of cleaning process` |
| `README.md` | Summary of all cleaning actions |

---

## Insights Gained
- Initial data contained minor inconsistencies in text casing and date formats.
- No duplication records are found.
- A few records had invalid age entries, which were filtered for accurate analysis.

---

## Why Python over Excel?
While Excel is useful for quick visual checks, Python with Pandas is far more efficient, reproducible, and scalable for cleaning larger datasets. It allows automation of repetitive tasks, better handling of data types, and provides a clearer audit trail—making it the preferred tool for data professionals.

---

## Maintained by
**Damanti Murmu**  
Aspiring Business and Data Analyst |
[LinkedIn](https://www.linkedin.com/in/damantimurmu/)
