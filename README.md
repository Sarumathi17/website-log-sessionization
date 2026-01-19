# Website Log Data Cleaning and Sessionization

## Objective
The objective of this project is to clean raw web server log data and identify
user sessions based on a 30-minute inactivity threshold. Bot and crawler traffic
is filtered to ensure analysis reflects genuine user behavior.

## Dataset
Public Apache web server access log dataset obtained from a publicly available
GitHub repository. The dataset contains real website traffic including both
human users and bot traffic.

## Tools & Technologies
- Python
- Pandas
- Jupyter Notebook

## Approach
1. Parsed raw Apache access logs into structured columns such as IP address,
   timestamp, URL, and user agent.
2. Converted timestamps to datetime format and sorted records by IP and time.
3. Identified user sessions using a 30-minute inactivity rule.
4. Detected and removed bot and crawler traffic based on user-agent patterns.
5. Generated session-level summaries including session duration and page views.

## Output
- Cleaned, sessionized dataset at the session level
- CSV file containing final session summaries

## Repository Structure
- `notebooks/log_sessionization.ipynb` – Main analysis notebook
- `data/access.txt` – Raw web server logs
- `data/sessionized_logs.csv` – Final sessionized output
