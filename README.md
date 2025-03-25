# Cloud File Encryption and Storage

## Project Overview
This project enables secure file storage by implementing an encryption process before storing files in AWS S3. The workflow includes:
- Uploading a raw file, which is stored in Azure.
- Encrypting the file locally.
- Saving the encrypted file locally and uploading it to AWS S3.
- Logging all events in Azure Application Insights and AWS CloudWatch.
- Storing log data in CloudSyncDB.
- Implementing a backup mechanism: If a file is deleted from either Azure or AWS S3, it can be retrieved from the other.

## Features
- Secure file encryption before cloud storage.
- Integration with Azure for initial raw file storage.
- Encrypted file storage in AWS S3.
- Centralized logging with Azure Application Insights and AWS CloudWatch.
- Database storage for log records in CloudSyncDB.
- Backup retrieval from the alternate storage location if deleted.

## Technology Stack
- **Cloud Services:** Azure, AWS S3
- **Monitoring & Logging:** Azure Application Insights, AWS CloudWatch
- **Database:** CloudSyncDB
- **Encryption:** AES-258
- **Backend:** JavaScript

## Workflow
1. **File Upload:** User uploads a raw file which is stored in Azure.
2. **Encryption Process:**
   - The uploaded file is encrypted using (encryption algorithm).
   - The encrypted file is stored locally.
3. **Storage in AWS:** The encrypted file is uploaded to AWS S3.
4. **Backup Mechanism:** If a file is deleted from one storage location (Azure or AWS S3), it can be restored from the other.
5. **Logging:**
   - Azure Application Insights logs file uploads and encryption details.
   - AWS CloudWatch tracks file storage activities.
6. **Database Sync:** CloudSyncDB stores relevant log data for tracking and auditing.
