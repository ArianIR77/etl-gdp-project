# ETL GDP Project

This project is part of a hands-on lab to demonstrate the implementation of a complete ETL (Extract, Transform, Load) pipeline using Python. The goal is to extract GDP data for all countries from a web archive of a Wikipedia page, transform it into the desired format, and load it into both a CSV file and a SQLite database.

---

## 📊 Project Objective

An international firm looking to expand its operations worldwide wants access to up-to-date GDP data. As a Junior Data Engineer, you are tasked with building an automated ETL pipeline to:
- Extract GDP data from a specified webpage.
- Convert the GDP figures from **millions to billions** of USD.
- Save the processed data into a **CSV file** and a **SQLite database**.
- Run a query to retrieve countries with **GDP greater than 100 billion USD**.
- Log each step of the ETL process with timestamps.

---

## 🔧 Technologies Used

- **Python 3**
- `requests`
- `beautifulsoup4`
- `pandas`
- `numpy`
- `sqlite3`
- `datetime`

---

## 🛠️ Project Structure

- `etl_project_gdp.py` – Main Python script that performs the full ETL process.
- `Countries_by_GDP.csv` – Output CSV file with country and GDP data in billions.
- `World_Economies.db` – SQLite database file containing the table `Countries_by_GDP`.
- `etl_project_log.txt` – Log file capturing the progress of the ETL process.

---

## 🚀 How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/<your-username>/etl-gdp-project.git
   cd etl-gdp-project
````

2. Install required packages:

   ```bash
   pip install -r requirements.txt
   ```

3. Run the script:

   ```bash
   python etl_project_gdp.py
   ```

---

## 📌 Output Example

Query output for countries with **GDP > 100 billion USD**:

```
        Country       GDP_USD_billions
1         China                19373.59
2         Japan                 4409.74
3       Germany                 4308.85
...         ...                     ...
66       Oman                   104.90
67  Guatemala                   102.31
68   Bulgaria                   100.64
```

---

## 📝 Notes

* The script uses a snapshot of the Wikipedia GDP page from September 2023, accessed via the [Wayback Machine](https://web.archive.org/web/20230902185326/https://en.wikipedia.org/wiki/List_of_countries_by_GDP_%28nominal%29).
* Logging is implemented at each major step of the ETL process to `etl_project_log.txt`.

---

## 📂 Sample Log Entry

```
2025-05-01-14:00:01:Preliminaries complete. Initiating ETL process.
2025-05-01-14:00:05:Data extraction complete. Initiating Transformation process.
...
2025-05-01-14:00:30:Process Complete.
```
