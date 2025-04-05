# daisy-serverless-lesson2.13
CE9 Lesson 2.13 Homework

1. What Type of Infrastructure and Application Deployments Are Each Tool Best Suited For?

- Terraform

Designed for provisioning and managing cloud infrastructure across multiple providers (AWS, Azure, Google Cloud, etc.).

Best suited for traditional cloud deployments involving networking, storage, databases, VMs, Kubernetes clusters, and other infrastructure components.

Ideal for long-lived environments where infrastructure resources persist beyond specific application functions.

- Serverless Framework

Focused on deploying serverless applications, mainly on AWS Lambda, Google Cloud Functions, and Azure Functions.

Best suited for event-driven workloads, microservices, and applications that scale dynamically without provisioning or managing servers.

Optimized for short-lived function executions, API-based applications, and automation use cases.

2. How Do Their Primary Objectives Differ?
- Terraform → Infrastructure-as-Code (IaC)

Provides declarative configuration for creating and managing infrastructure at scale.

Ensures repeatability, consistency, and automation of cloud resource provisioning.

Focused on infrastructure longevity and stability.

- Serverless Framework → Application Deployment & Management

Focuses on deploying serverless applications and event-driven architectures.

Simplifies function deployments with predefined configurations for APIs, databases, and cloud events.

Optimized for reducing infrastructure management overhead.

3. Learning Curve and Ease of Use for Developers or DevOps Teams
- Terraform

Steeper learning curve because it requires an understanding of cloud infrastructure, HCL (HashiCorp Configuration Language), and state management.

More complex state tracking and dependency resolution, requiring careful planning.

Provides fine-grained control over resources, which adds complexity but also flexibility.

- Serverless Framework

Easier to learn for developers since it's centered around deploying serverless applications.

Uses YAML configuration files, making it simpler to manage functions and events.

Abstracts much of the infrastructure complexity, allowing developers to focus on code rather than cloud resources.

4. Differences in State Tracking and Deployment Changes
- Terraform (State-Based Management)

Maintains a state file (terraform.tfstate), which records all deployed resources.

Allows for incremental changes, making modifications to infrastructure without re-deploying everything.

Uses plan & apply mechanisms to preview and execute changes safely.

- Serverless Framework (Stateless Deployments)

Deploys functions without maintaining a central state file.

Changes are typically re-deployed from scratch, meaning deployments often overwrite existing configurations.

Uses provider-specific tracking (e.g., AWS CloudFormation) for managing resources indirectly.

5. When to Use Serverless Framework Over Terraform (and Vice Versa)?
- Use Serverless Framework When:

Building an event-driven application that relies on AWS Lambda or other cloud functions.

Want quick deployments with minimal infrastructure overhead.

The application does not require persistent infrastructure, like VMs, Kubernetes clusters, or complex networking.

- Use Terraform When:

Need complete control over cloud infrastructure, including networking, storage, compute, and databases.

Managing a hybrid cloud environment or multi-cloud strategy.

Infrastructure should be long-lived and needs robust state tracking.

6. Are There Scenarios Where Using Both Together Might Be Beneficial?
Yes. Terraform and Serverless Framework can complement each other effectively in hybrid architectures, such as:

Example Use Case: Combining Terraform & Serverless Framework

Terraform provisions core cloud infrastructure (VPCs, IAM roles, databases, S3 buckets, etc.).

Serverless Framework deploys application logic (Lambda functions, API Gateway routes, event-driven triggers).

Terraform manages long-lived infrastructure, while Serverless handles ephemeral compute workloads.

Best Practice: Use Terraform to provision foundational resources, then Serverless Framework to deploy and manage serverless applications on top of that infrastructure.

