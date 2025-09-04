# SQL-Based Security Investigation

## Overview
This repository documents a SQL-based investigation of security issues in a large organization’s employee and login data. As a cybersecurity professional, I analyzed the `employees` and `log_in_attempts` tables using SQL filters (`AND`, `OR`, `NOT`) to identify unauthorized access and suspicious login patterns. The project showcases my SQL skills, problem-solving, and commitment to securing organizational systems, supported by lab screenshots.

## Objectives
- Examine login attempts and employee data to detect security issues.
- Use SQL queries with `AND`, `OR`, `NOT` to identify risks like brute force attacks or unauthorized logins.
- Support findings with lab screenshots.

## Tools Used
- **Database**: SQL (e.g., MySQL, SQLite) in a lab environment.
- **Documentation**: PDF (audit report), Markdown, lab screenshots.

## Repository Structure
- [sql-audit-report.pdf](https://github.com/Usman-emtee/SQL-Security-Investigation/blob/main/sql-audit-report.pdf): Portfolio document with SQL queries, findings, and screenshots.

## Key Findings
- **Brute Force Risk**: User `alice` had 5 failed login attempts, suggesting a potential attack.
- **Unauthorized Access**: User `charlie` logged in at 2:00 AM, outside business hours.
- **Non-Employee Attempts**: Unknown usernames attempted access, indicating intrusion attempts.
- **Recommendations**: Implement MFA, restrict login hours, block external IPs, and set up monitoring.

## Usage
1. Clone the repository: `git clone https://github.com/Usman-emtee/SQL-Security-Investigation.git`
2. Review the report in `sql-audit-report.pdf`.


## Example Query
```sql
SELECT username, COUNT(*) as failed_attempts
FROM log_in_attempts
WHERE success = 0
GROUP BY username
HAVING failed_attempts > 3;
```

## Disclaimer
This investigation was conducted in a lab environment with hypothetical data. Always obtain explicit permission before analyzing real systems to ensure compliance with legal and ethical standards.

## Contact
- GitHub: [usman-emtee](https://github.com/usman-emtee)
- LinkedIn: [usman-mt](https://linkedin.com/in/usman-mt)
- Email: usmanemtee@gmail.com
