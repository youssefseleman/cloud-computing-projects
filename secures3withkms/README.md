SecureS3 with KMS
This project provides step-by-step instructions for securely storing data in an Amazon S3 bucket using AWS Key Management Service (KMS) for encryption. All actions are performed via the AWS Management Console.

Prerequisites
An AWS account with necessary permissions to create:
S3 buckets
KMS customer managed keys
IAM policies
Internet access and browser to open AWS Console
Objective
Create a secure S3 bucket that uses server-side encryption with a KMS key (SSE-KMS) for all uploaded objects, ensuring data-at-rest protection.

Steps
1. Create a Customer Managed Key (CMK) in KMS
Go to the AWS KMS Console.
Click Create key.
Choose:
Symmetric key type
Encrypt and decrypt key usage
Enter an alias (e.g., secureS3Key)
Optionally add a description and tags.
Set key administrative and usage permissions (allow necessary IAM users or roles).
Click Finish.
2. Create an S3 Bucket with Encryption
Go to the Amazon S3 Console.
Click Create bucket.
Set a unique bucket name (e.g., my-secure-bucket-kms).
Choose region.
Under Default encryption, select:
Enable
AWS Key Management Service key (SSE-KMS)
Choose your CMK (e.g., secureS3Key)
Click Create bucket.
3. Upload Objects to the Encrypted Bucket
Go to your bucket in the S3 Console.
Click Upload, then select files.
In the Properties section, verify:
Encryption is set to AWS-KMS
AWS KMS key is your customer-managed key
Click Upload.
