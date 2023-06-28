# undergroundcyberfight
Pick your side in a 24-Hour hack battle powered by The Cloud Underground

A shared Vulnerable AD environment & DetectionLab config in the same environment

A signup page with timeslots as buttons, upon pressing the button, you're prompted to pay for the timeslot, you're provided a one-time, once generated token. (so if it's lost they know the risks going into it)

You can choose blue or red when the user supplies the token

starts an ansible/terraform deployment to an ubuntu or kali rdp session via https

### Network Segmentation and Isolation within Proxmox:

- Use Terraform to define and provision virtual networks (VLANs) within Proxmox.
- Configure firewall rules and network interfaces in Proxmox using Ansible playbooks to control the traffic flow between different segments.
- Leverage Proxmox's network bridge functionality and Ansible to automate the setup and management of virtual switches and network interfaces.

### For user activity monitoring and logging:

- Configure centralized logging using Ansible and tools like the ELK (Elasticsearch, Logstash, Kibana) stack or Splunk to collect and analyze logs from VMs within the cyber range.
- Set up monitoring and intrusion detection systems (IDS) using Ansible to detect and alert on suspicious activities within the range.

### When incorporating cybersecurity tools and technologies:

- Utilize Ansible to automate the installation and configuration of security tools (e.g., intrusion detection systems, vulnerability scanners) within the VMs.
- Leverage Packer to create custom VM images with pre-installed security tools, ensuring consistent deployments.
