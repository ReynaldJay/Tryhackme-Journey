# Tryhackme-Journey
Documenting my cybersecurity journey through TryHackMe. Includes detailed write-ups, notes, and proof of completion for each room, focusing on blue team skills and SOC operations. A portfolio to track progress, reinforce learning, and showcase commitment to the field.

pre_security_path = '/mnt/data/tryhackme-pre-security'

# Example rooms in the Pre Security Path (as of current THM curriculum)
rooms = [
    "Cyber Security Introduction",
    "How The Web Works",
    "DNS in Detail",
    "Packets and Protocols",
    "HTTP in Detail",
    "OSI Model",
    "Intro to LAN",
    "Physical Layer",
    "Network Services",
    "Windows Fundamentals Part 1",
    "Windows Fundamentals Part 2",
    "Windows Fundamentals Part 3",
    "Linux Fundamentals Part 1",
    "Linux Fundamentals Part 2",
    "Linux Fundamentals Part 3"
]

for room in rooms:
    room_folder = os.path.join(pre_security_path, 'rooms', room.replace(" ", "_"))
    screenshot_folder = os.path.join(pre_security_path, 'screenshots', room.replace(" ", "_"))
    os.makedirs(room_folder, exist_ok=True)
    os.makedirs(screenshot_folder, exist_ok=True)
    
## Objective
Brief summary of the goal of this room.

## Key Skills Learned
- Skill 1
- Skill 2
- Skill 3

## Tools Used
- Tool 1
- Tool 2

## Notes
- Key insights or commands to remember

## Proof of Completion
![Screenshot](../../screenshots/{room.replace(" ", "_")}/proof.png)
"""
    with open(os.path.join(room_folder, 'README.md'), 'w') as f:
        f.write(md_content)

# Create README for the whole Pre Security Path
main_readme = """# TryHackMe – Pre Security Path

This folder documents my progress through the TryHackMe Pre Security Path.
Each room contains:
- Objectives
- Skills learned
- Tools used
- Notes
- Proof of completion (screenshots)

Screenshots are stored in the matching folder under `screenshots/`.

---
[![TryHackMe Badge](https://tryhackme-badges.s3.amazonaws.com/YourUsername.png)](https://tryhackme.com/p/YourUsername)
"""
os.makedirs(pre_security_path, exist_ok=True)
with open(os.path.join(pre_security_path, 'README.md'), 'w') as f:
    f.write(main_readme)

pre_security_path
