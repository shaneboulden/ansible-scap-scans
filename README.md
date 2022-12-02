## Ansible SCAP scanning

This is an example of how to orchestrate SCAP scans from an Ansible bastion host.

The `scan.yml` playbook:
- installs required OpenSCAP libraries and utilities on the target server
- copies across an example SCAP tailoring file to the target server
- performs a scan of the target server collecting ARF results, and creates a HTML report
- copies the ARF results and HTML report back to the bastion host, and
- cleans up the target server, removing the OpenSCAP libraries and any files
