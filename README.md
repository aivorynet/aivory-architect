# AIVory Architect

**Visual Cloud Infrastructure Design for Your IDE**

AIVory Architect is a multi-platform tool that lets you design cloud infrastructure visually and deploy with one click. Drag-and-drop VMs, databases, and load balancers onto a canvas, auto-generate
Terraform, and deploy to 6 cloud providers.

## Features

- **Visual Infrastructure Designer** - Drag-and-drop canvas with grid snapping and zoom/pan
- **6 Cloud Providers** - AWS, Azure, GCP, Hetzner Cloud, RunPod, DeepInfra
- **Terraform Code Generation** - One-click generation of production-ready `.tf` files
- **Integrated Deployment** - Execute `terraform init`, `plan`, `apply` directly from IDE
- **Kubernetes Management** - Deploy manifests and monitor pods in real-time
- **Secure Vault** - Credential storage and environment variable management

## Quick Start

### Prerequisites

- IntelliJ IDEA 2023.3+ (Community or Ultimate)
- Java 17+ (JetBrains Runtime recommended)
- Terraform 1.6+ (for deployment features)
- kubectl (for Kubernetes features)

### Installation

**JetBrains Marketplace:**
1. Open IntelliJ IDEA
2. Go to `Settings → Plugins → Marketplace`
3. Search for "AIVory Architect"
4. Click Install and restart IDE

**Manual Installation:**
```bash
# Clone and build
git clone https://github.com/aivorynet/aivory-architect.git
cd aivory-architect/architect-jetbrains
./gradlew buildPlugin

# Install from disk
# Settings → Plugins → ⚙️ → Install from Disk
# Select build/distributions/architect-jetbrains-*.zip

```
### Configuration

1. Open the AIVory Architect tool window (right sidebar)
2. Add cloud provider credentials via the Vault panel
3. Start designing your infrastructure

## Usage

Once installed, design and deploy infrastructure visually:

1. Open AIVory Architect tool window
2. Drag a VM node onto the canvas
3. Configure provider, size, and region in the properties panel
4. Connect to a database node
5. Click "Generate Terraform" → creates main.tf, variables.tf, outputs.tf
6. Click "Deploy" → runs terraform apply

### Cloud Providers

| Provider| Status | Resources Supported |
|---------------|----------------|-------------------------------------------------------|
| Hetzner Cloud | ✓ Full Support | Servers, Volumes, Networks, Load Balancers, Firewalls |
| AWS | ✓ Available| EC2, RDS, ELB, VPC, EBS, S3 |
| Azure | ✓ Available| VMs, SQL Database, Load Balancer, VNet, Managed Disks |
| GCP | ✓ Available| Compute Engine, Cloud SQL, Load Balancing, VPC|
| RunPod| ✓ Available| GPU Instances, Serverless Endpoints |
| DeepInfra | ✓ Available| AI Model Endpoints, Inference APIs|

### Resource Types

AIVory Architect supports these infrastructure components:

- Virtual Machines - Cloud VMs with SSH key management
- Databases - Managed SQL and NoSQL databases
- Load Balancers - Traffic distribution with health checks
- Networks - VPCs, subnets, and security groups
- Storage - Block volumes and object storage
- GPU Instances - AI/ML workloads on RunPod and DeepInfra
- Kubernetes - Pod deployment and monitoring

### Backend Integration

AIVory Architect integrates with the AIVory backend for cloud sync and team features:

- Cloud Sync - Save designs to the cloud
- Team Collaboration - Share infrastructure templates
- Authentication - OAuth2 PKCE with single sign-on

Free tier available - Get started immediately with local-only features.

For cloud sync and team features, subscribe at https://app.aivory.net/register/plans.

### Support

- Issues: https://github.com/aivorynet/aivory-architect/issues
- Email: support@aivory.net
- Website: https://aivory.net

---
Made with ❤️ by https://aivory.net
