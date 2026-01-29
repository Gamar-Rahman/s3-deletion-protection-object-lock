# s3-deletion-protection-object-lock
Hands-on lab demonstrating how to protect Amazon S3 buckets and objects from deletion using resource-based policies and S3 Object Lock with retention.

# Enable Deletion Protection for Amazon S3 Using Resource-Based Policy and Object Lock

## Lab Overview

This lab demonstrates how to protect an Amazon S3 bucket and its objects from accidental or unauthorized deletion using:

- **S3 Resource-Based (Bucket) Policies**
- **Amazon S3 Object Lock**

By the end of this lab, you will:
- Prevent deletion of an S3 bucket
- Prevent deletion of objects inside the bucket
- Enable Object Lock with a **1-day retention period**

---

## Concepts Covered

### What is a Resource-Based Policy?
A resource-based policy is directly attached to an AWS resource (such as an S3 bucket or KMS key).  
It controls:
- **Who** can access the resource
- **What actions** they can perform

In this lab, we use a bucket policy to explicitly **deny delete operations**.

---

### What is Amazon S3 Object Lock?
Amazon S3 Object Lock prevents objects from being:
- Deleted
- Overwritten

for a fixed retention period or indefinitely (WORM – Write Once Read Many).


# Configure Amazon S3 Object Lock (1 Day Retention)

## Steps

1. Upload an object to the S3 bucket
2. Select the object → Actions → Edit retention
3. Enable retention
4. Choose:
   - Retention mode: Governance
   - Retention period: 1 Day
5. Save changes

---

## Validation

Attempt to:
- Delete object ❌
- Overwrite object ❌

You should receive an **Access Denied** error.


#### Object Lock Modes:
- **Retention Period** – Locks objects for a defined time
- **Legal Hold** – Locks objects indefinitely until removed



