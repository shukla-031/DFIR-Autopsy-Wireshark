# DFIR Investigation Workflow

## Step 1: Network Analysis (Wireshark)
- Opened an offline PCAP file
- Applied filters such as:
  - http
  - dns
- Identified suspicious domains via DNS queries
- Detected HTTP GET requests indicating file downloads
- Followed TCP streams to confirm download activity

## Step 2: Disk Analysis (Autopsy)
- Created a new case in Autopsy
- Added a sample disk image as a data source
- Enabled ingest modules:
  - Web History
  - Recent Activity
  - File Type Identification
- Reviewed browser history and download artifacts

## Step 3: Correlation
- Network traffic revealed a suspicious file download
- Disk artifacts demonstrated how such activity is stored on disk
- Learned how investigators correlate evidence from multiple sources
