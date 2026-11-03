Run 1
Instance ID: i-099a7c064e4c9cb04
Summary:
For my initial manual lab run, I provisioned a fresh Amazon Linux 2023 t3.small instance in us-east-1 and executed the standard setup sequence from scratch. During the setup, I encountered an initial path error because I accidentally included a trailing space and period in my git clone command, which I resolved by clearing the hidden .git folder and re-cloning correctly. This run helped me truly understand how AWS provisions brand-new metadata and ephemeral local storage for every independent virtual machine.
Exact Output Line:
INFO:     Uvicorn running on http://0.0.0.0:8000 (Press CTRL+C to quit)

Run 2
Instance ID: i-093cdb12d1824172
Summary:
In this second run, I focused on improving my muscle memory by executing Steps 0 through 4 entirely by hand on a new instance. I hit a minor syntax hiccup when typing the mandatory ID line because I accidentally put a space after the TZ= equals sign, which caused Bash to throw a "no such file or directory" error that I quickly corrected. Through this repetition, I gained a much deeper appreciation for why tracking unique boot timestamps and instance IDs is vital for validating individual cloud deployments.
Exact Output Line:
Sat Oct 31 01:59:43 GMT 2026

Run 3
Instance ID: i-0761579b3aa9d7b8e
Summary:
Building further repetition for my third manual sequence, I spun up another fresh EC2 instance and systematically ran through package installation, repository cloning, and environment activation. No major syntax blockers occurred this time around, allowing me to focus heavily on verifying the API endpoints and Swagger documentation layout. I now fully understand how isolating dependencies inside the virtual environment protects the system architecture from global package conflicts.
Exact Output Line:
i-0761579b3aa9d7b8e

Run 4
Instance ID: i-0135beacedb51c0b7
Summary:
For my fourth run, I successfully executed the full lab sequence while carefully verifying my London timezone formatting and metadata queries before launching Uvicorn. I encountered zero unexpected errors during this run because the command sequence has become much more familiar through consistent practice. This run solidified my understanding of how AWS assigns distinct private and public IPs to each separate instance lifecycle.
Exact Output Line:
2026-10-31 17:31:50

Run 5
Instance ID: i-0b1e7ce10d4b9c3eb
Summary:
For my fifth run, I completed the full installation and server setup sequence on a fresh EC2 instance before performing the mandatory COBOL practice tasks. I experienced an issue when running custom transactions without semicolon separators, which caused exit code checks to fail when commands threw errors. After correcting the syntax to use semicolons, I successfully executed and verified all four COBOL exit codes (0, 4, 8, 12).
Exact Output Line:
boot-time: 2026-11-02 00:25:18

Run 6
Instance ID: i-006774b3d6bd4f8f6
Summary:
During my sixth run, I executed the full automation and verification sequence while focusing on executing manual fixed-width ledger slicing using Linux cut commands. I initially ran into an issue where the SSH terminal session froze during execution, which I resolved by establishing a fresh SSH connection back into /opt/balerica-bank. This run reinforced how fixed-width records store account data deterministically across legacy file systems.
Exact Output Line:
100001Alice Johnson             ACTIVE  000005000000USD

Run 7
Instance ID: i-00985bd8e86aa9fd0
Summary:
For my final lab run, I executed the end-to-end setup sequence for the seventh time to solidify complete muscle memory for EC2 provisioning and application deployment. The installation and initialization executed cleanly with zero pathing or permission errors. Completing this final iteration cemented my understanding of how cloud infrastructure lifecycle management integrates with application runtime execution.
Exact Output Line:
INFO:     Application startup complete.


