<h1>Data Protection &amp; Encryption Implementation</h1>
<h3>AWS Enterprise Environment</h3>

<h2>Overview</h2>
<p>
  This repository documents the implementation of a data-protection strategy in AWS focused on preventing public exposure and
  enforcing encryption at rest across storage and database services. The work also includes continuous compliance monitoring and
  alerting to detect non-compliant configurations in real time.
</p>

<hr/>

<h2>Key Responsibilities</h2>
<ul>
  <li>Enabled S3 Block Public Access at the account level to prevent accidental public exposure</li>
  <li>Encrypted S3 buckets using SSE-KMS with customer-managed keys (CMKs) for stronger control and auditability</li>
  <li>Enabled EBS encryption by default to ensure all new volumes and snapshots are automatically encrypted</li>
  <li>Identified an unencrypted EBS volume and migrated it to an encrypted volume using snapshots (copy + encrypt + reattach) without data loss</li>
  <li>Validated RDS encryption posture and enforced encryption at creation time to meet compliance expectations</li>
  <li>Created a customer-managed symmetric KMS key and enabled automatic key rotation (365 days)</li>
  <li>Documented a safe manual rotation approach for keys that do not support automatic rotation (create new key, move new encryption, monitor, disable old key, retain for recovery)</li>
  <li>Configured AWS Config rules to monitor S3 public access and encryption compliance across S3, EBS, and RDS</li>
  <li>Implemented SNS alerts for non-compliance and validated notifications by intentionally triggering a policy violation</li>
</ul>

<hr/>

<h2>Tools &amp; Technologies</h2>
<ul>
  <li>Amazon S3 (Block Public Access, Default Encryption)</li>
  <li>AWS Key Management Service (KMS)</li>
  <li>Amazon EBS (Encryption by Default, Snapshots)</li>
  <li>Amazon RDS (Encryption at Rest)</li>
  <li>AWS Config (Rules, Compliance Tracking)</li>
  <li>Amazon SNS (Notifications)</li>
</ul>

<hr/>

<h2>Impact</h2>
<ul>
  <li>Reduced risk of data exposure by blocking public S3 access at the account level</li>
  <li>Enforced encryption at rest across storage and database services using KMS</li>
  <li>Improved compliance readiness through continuous configuration monitoring and alerting</li>
  <li>Established repeatable key-rotation practices to support long-term security operations</li>
</ul>

<hr/>

<h2>Author</h2>
<p>
  <strong>Adedayo</strong><br/>
  AWS Cloud Architect | Cloud Security Specialist
</p>

<hr/>

<h2>Disclaimer</h2>
<p>
  All documentation is anonymized and does not contain confidential or proprietary information.
</p>
