Spotter = Brandon   (the person who spots YOU)
5 things my spotter learned while working on the lab / homework:
1. Assigning the improper inbound rules may allow the SSH instance to load, but not the webpage and vice versa.
2. Installs on EC2 SSH instances can retain memory between instances that share a private IP for a short period of time.
3. The proper file path for displaying pngs and jpgs is ![alt text](path) in .md files.
4. Instances launched from templates can be renamed through the "Name" tag.
5. Unique "Instance IDs" are what give instances uniqueness and not their "Name" tag.

I am the spotter for = Brandon   (the person YOU spot)
5 things I learned that I shared with them:
1. Provisioning and managing fresh EC2 instances from scratch: I learned how to deploy brand-new instances running Amazon Linux 2023 in AWS (us-east-1), manage local instance lifecycles manually, and avoid relying on automated templates.
2. Mastering package managers and command line flags: I learned how AWS package management works using dnf (Danified Yum), understanding that it installs pre-approved software from trusted vendors, and using the -y flag to automatically answer "yes" to installation prompts.
3. Understanding superuser permissions and root access: I learned how sudo stands for "superuser do" and why it is necessary to temporarily elevate permissions to install system packages and modify protected directories.
4. Understanding instance classes, families, sizes, and generations: I learned how AWS hardware is categorized into instance types and generations, specifically focusing on selecting the right instance size to meet specific memory requirements like having 2 GB of RAM.
5. SQL and NoSQL database use cases and scaling logic: I learned how SQL's strict structure fits reliable financial transactions (like banking ledgers), while NoSQL is better suited for unstructured media catalogs (like Spotify) to eliminate the heavy CPU costs and complex JOIN queries required to link artists, tracks, videos, and albums.

