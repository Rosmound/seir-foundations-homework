# Spotter Verification File

## Part 1: My Spotter
- **Spotter Name:** Brandon (the person who spots YOU)

### 5 Things My Spotter Learned:
1. Provisioned EC2 instances manually in `us-east-1` with `t3.small` sizing.
2. Understood how package management with `dnf` and the `-y` flag automates non-interactive installations.
3. Learned that return code `4` in GnuCOBOL means account not found without crashing the application.
4. Learned how to launch Uvicorn FastAPI servers to expose backend legacy COBOL programs via modern APIs.
5. Learned how to create Golden AMIs to capture disk state and launch pre-configured environments fast.

---

## Part 2: Person I Spot
- **Spotted Student:** Darian (the person YOU spot)

### 5 Things I Learned That I Shared With Them:
1. **Provisioning and managing fresh EC2 instances from scratch:** I learned how to deploy brand-new instances running Amazon Linux 2023 in AWS (`us-east-1`), manage local instance lifecycles manually, and avoid relying on automated templates.
2. **Mastering package managers and command line flags:** I learned how AWS package management works using `dnf` (Danified Yum), understanding that it installs pre-approved software from trusted vendors, and using the `-y` flag to automatically answer "yes" to installation prompts.
3. **Understanding superuser permissions and root access:** I learned how `sudo` stands for "superuser do" and why it is necessary to temporarily elevate permissions to install system packages and modify protected directories.
4. **Understanding instance classes, families, sizes, and generations:** I learned how AWS hardware is categorized into instance types and generations, specifically focusing on selecting the right instance size to meet specific memory requirements like having 2 GB of RAM.
5. **SQL and NoSQL database use cases and scaling logic:** I learned how SQL's strict structure fits reliable financial transactions (like banking ledgers), while NoSQL is better suited
for unstructured media catalogs (like Spotify) to eliminate the heavy CPU costs and complex `JOIN` queries required to link artists, tracks, videos, and albums.

