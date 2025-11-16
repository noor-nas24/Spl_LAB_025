
# Lab Title: Splunk – DNS Log Analysis

---

## Objective

In this lab, you will:
- Learn how to ingest and analyze DNS logs in Splunk.
- Understand how to extract useful information such as DNS query types, source hosts, and common destinations.
- Practice building basic SPL (Search Processing Language) queries to investigate DNS activity.

---

## Lab Setup

1.**Splunk**: Already installed and accessible.

2.**Data Source**: JSON-formatted Zeek DNS logs.

3.**Log File**: Download the file below and place it in a directory accessible to Splunk for ingestion.
**[Download sample dns file](https://raw.githubusercontent.com/0xrajneesh/30-Days-SOC-Challenge-Beginner/refs/heads/main/dns_logs.json)**

---

## Steps to Upload DNS Log into Splunk

1. Go to Splunk Web → **Settings > Add Data**.
2. Choose **Upload** and select the file `dns.log`.
3. Set Source type: `json` or create a custom source type `dns`.
4. Index: Choose `main` or create a new index like `dns_lab`.
5. Finish the upload and confirm indexing.
6. you can start search `source="" host=" sourcetype="_json" `.
---

## Lab Tasks

Use SPL queries to answer the following:

### Task 1: Identify the most frequently queried domain names
```spl
index="*" | stats count by query | sort -count
```

### Task 2: Find the most active user IPs generating DNS traffic
```spl
 index="*" | stats count by "id.orig_h" | sort -count
```
### Task 3: Breakdown of DNS query types (A, AAAA, CNAME, PTR)
```spl
index="*" | stats count by qtype
```
## Submission
Submit a screenshot of each of the following:
- Your SPL query and result for Task 1.
 ![image alt](https://github.com/noor-nas24/Spl_LAB_025/blob/591b4f264f85823415171b54627def3b2f6e9a08/Task3.png)
  
- SPL query and result for Task 2.
   ![image alt](https://github.com/noor-nas24/Spl_LAB_025/blob/591b4f264f85823415171b54627def3b2f6e9a08/task2.png)
  
- SPL query and result for Task 3.
 ![image alt](https://github.com/noor-nas24/Spl_LAB_025/blob/591b4f264f85823415171b54627def3b2f6e9a08/Task3.png)
