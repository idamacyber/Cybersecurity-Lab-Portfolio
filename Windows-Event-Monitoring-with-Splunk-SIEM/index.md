# 📌 Windows Event Monitoring & Threat Detection Using Splunk SIEM

Splunk Enterprise was installed and configured locally on a Windows machine.

The following tasks were completed during deployment:

- Installed Splunk Enterprise
- Configured administrator account
- Accessed Splunk Web Interface
- Added Windows Event Logs as data sources
- Configured log ingestion settings
- Verified successful event ingestion
- Performed event analysis using SPL queries

Windows Event Logs were configured using:

```text
Settings → Add Data → Monitor → Local Event Logs

# 📊 Log Ingestion Verification

After configuring the data source, log ingestion was verified using the following SPL query:

```spl
index=windows
```

This confirmed that Windows logs were successfully indexed and searchable within Splunk.

The ingested telemetry included:

- Authentication events
- Security-related activity
- System events
- Host information
- Event timestamps

---

# 🚨 Detection Engineering & Security Monitoring

Several SPL queries were created to identify potentially suspicious authentication-related activity within the Windows environment.

## ❌ Failed Login Detection

```spl
index=windows EventCode=4625
```

### Purpose

Detects failed authentication attempts that may indicate:

- Brute-force attacks
- Password spraying attempts
- Unauthorized access attempts
- Invalid credential usage

---

## ✅ Successful Login Detection

```spl
index=windows EventCode=4624
```

### Purpose

Identifies successful user logins and helps analysts:

- Track user activity
- Verify account access
- Investigate suspicious login patterns
- Correlate successful access after failed attempts

---

## 🔒 Account Lockout Detection

```spl
index=windows EventCode=4740
```

### Purpose

Detects locked user accounts that may indicate:

- Password brute-force activity
- Repeated invalid login attempts
- Misconfigured services using outdated credentials

---

## 👤 New User Account Creation

```spl
index=windows EventCode=4720
```

### Purpose

Identifies newly created user accounts which may indicate:

- Unauthorized account creation
- Privilege escalation attempts
- Persistence mechanisms
- Administrative misuse


This project demonstrated how SIEM platforms provide visibility into endpoint activity and support security investigations through centralized log analysis.


# 🛠️ Skills Demonstrated

- SIEM deployment and configuration
- Windows Event Log ingestion
- SPL query development
- Security event analysis
- Threat detection fundamentals
- Authentication monitoring
- Log analysis and investigation
- SOC monitoring workflow


### 📊 Evidence & Documentation

All screenshots and explanations for this project are documented here:

🔗 [Google Slides ](https://docs.google.com/presentation/d/1dA2qaCVj_mEvSgb1v2BjULstgeQHIxDoC130sKnJhPk/edit?usp=sharing)


# ✅ Conclusion

This project successfully demonstrated the deployment and configuration of Splunk Enterprise for centralized Windows Event Log monitoring in a SOC-style lab environment.

By ingesting and analyzing Windows Security and System logs, the lab provided hands-on experience with SIEM operations, authentication monitoring, and basic threat detection workflows commonly used in real-world Security Operations Centers (SOCs).
