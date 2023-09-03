# Underground Cyber Fight

![](https://www.canva.com/design/DAFsfTkwAEM/_jirTJoIWcJIGL_z9trE2Q/watch?utm_content=DAFsfTkwAEM&utm_campaign=designshare&utm_medium=link&utm_source=publishsharelink)

[https://github.com/cmndcntrlcyber/undergroundcyberfight](https://github.com/cmndcntrlcyber/undergroundcyberfight)

24-hour red v blue hackathon, watch from each sides perspective or both, then team challenges on the weekend

A shared DetectionLab environment

A signup page with timeslots as buttons, upon pressing the button, you're prompted to pay for the timeslot, you're provided a one-time, once generated token. (so if it's lost they know the risks going into it)

You can choose blue or red when the user supplies the token

Starts an Ansible/Terraform deployment to an Ubuntu or Kali RDP session via HTTPS

# Gamification Objectives

## Red Objectives

Distribute red-token-id at necessary points

## Blue Objectives

Distribute blue-token-id at necessary points

## Score Calculation

- 51 flags planted throughout the environment
    
    (1 flag per 24 hrs day * two teams = 48 flags rounded up to 51 so there are no ties) 
    

Bot sweeps through directories to find the flags of users engaged

end of session

score is passed via api, posts to database that serves to an overlay our video render 

- [ ]  does youtube have something built in for custom overlays?
    - [ ]  Custom Workspaces
        - [ ]  OBS
        - [ ]  VM Version
        - [ ]  Browser
        - [ ]  App emulation
        - [ ]  Zoom function Trigger

## Viewership Methods

![](https://github.com/cmndcntrlcyber/undergroundcyberfight/blob/main/Untitled.png)


### Streaming

A participant can choose to stream their session while they hack or defend

A youtube window is broken into 7 parts, a top middle timer, middle topology minimap, one player in each outer-top corner, a view of their monitor in the outer-bottom corner, in the bottom middle is the scorecard over a 24-hour period (at midnight it resets)

### Topology tracking

A small Topological overlay shows where the flags are and where the participant is in relation to them

as the user gets closer to a flag on the topological map the view of the computer display zooms closer to the users’ active terminal until they plant their x-token-id

## Player Interaction

Process from Web App to Console

1. White screen, in the middle it reads `Enter Username:` 
2. User enters Username 
3. User selects a single Red or Blue Timeslot 
4. hit a paywall(?), use paypal or crypto(?)
5. after payment they receive the red-token
    1. same token is what bot scans for
    2. same token will be used for a API granted curl request to payloads staged at an upload server (payload.attck.community/red-token/)

# Infrastructure Objectives

# Version 1

# Version 2

### Network Segmentation and Isolation within Proxmox:

- Use Terraform to define and provision virtual networks (VLANs) within Proxmox.
- Configure firewall rules and network interfaces in Proxmox using Ansible playbooks to control the traffic flow between different segments.
- Leverage Proxmox's network bridge functionality and Ansible to automate the setup and management of virtual switches and network interfaces.

### For user activity monitoring and logging:

- Configure centralized logging using Ansible and tools like the ELK (Elasticsearch, Logstash, Kibana) stack or Splunk to collect and analyze logs from VMs within the cyber range.
- Set up monitoring and intrusion detection systems (IDS) using Ansible to detect and alert on suspicious activities within the range.

### When incorporating cybersecurity tools and technologies:

- Utilize Ansible to automate the installation and configuration of security tools (e.g., intrusion detection systems, vulnerability scanners) within the VMs.
    - **For Red Team:** Debian WebTop with Kali Packages and Default Desktop
        - `echo "deb http://http.kali.org/kali kali-rolling main contrib non-free non-free-firmware" | sudo tee /etc/apt/sources.list`
        - Second Ubuntu Server for C2
<<<<<<< HEAD
    - **For Red Team:** Ubuntu 20.04 WebTop with SecOnion
        - ![SecOnion](https://github.com/Security-Onion-Solutions/securityonion)
=======
    - **For Blue Team:** Ubuntu 20.04 WebTop with SecOnion
>>>>>>> 274efc805c3ad9e6166acd222f0c9c7ca4bc6ee0
    - **Target Env:** DetectionLab 
- Leverage Packer to create custom VM images with pre-installed security tools, ensuring consistent deployments.
    - **RT WebTop**
    - **BT WebTop**

