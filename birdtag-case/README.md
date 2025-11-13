# BirdTag — Serverless Bird Recognition (AWS)

BirdTag is a serverless system for media tagging and retrieval. It processes images/audio, applies ML models to detect bird species, and notifies users about updates on specific tags.

## My Role & Contributions
- **AWS IAM** setup and permissions hardening
- **API Gateway** design & deployment
- **User authentication** via **Amazon Cognito**
- Implemented **`update_tags` Lambda (Python)** to modify bird tags for image/video/audio assets
- **SNS-based notifications**: topic & subscription flow to inform users about updates by tag

## Architecture (high-level)
- **S3**: media storage
- **Lambda**: ML inference & business logic (YOLOv8, BirdNET; `update_tags`, queries)
- **API Gateway**: unified entry point
- **DynamoDB**: tags/metadata
- **SNS**: notifications
- **Cognito**: user pools & auth
- **CloudWatch**: logs/metrics

(Front-end was a local **Vue** client under `/client`, not deployed per assignment constraints.)

## Key Features (selected)
- Serverless tagging & retrieval workflow
- Tag-based notifications via SNS subscriptions
- Authenticated API access with Cognito JWT

## Diagrams & Screenshots
- ![Architecture](./images/architecture.png)

## Notes & Improvements
- Proposed: CloudWatch Alarms, input validation, caching, batch processing, and distribution via CloudFront for global latencies

## Attribution
- Group assignment at Monash University.  
- **Original repository (team)**: https://github.com/dijia1124/cc-a3-group  
- This case study contains **write-up and diagrams/screenshots only**; code remains with the team.
