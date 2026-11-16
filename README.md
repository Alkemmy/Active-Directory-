<img width="410" height="170" alt="Screenshot 2026-11-15 at 3 38 41 PM" src="https://github.com/user-attachments/assets/75c9243d-4ecb-467b-bef0-e5283f805ccf" />
<img width="1717" height="550" alt="Screenshot 2026-11-15 at 3 49 00 PM" src="https://github.com/user-attachments/assets/208da966-3ad7-4132-b4b2-9a5cfe72528c" />
<img width="1014" height="724" alt="Screenshot 2026-11-16 at 6 25 20 PM" src="https://github.com/user-attachments/assets/03b209dc-a85d-4943-850a-7966f5899ef1" />
<img width="708" height="469" alt="Screenshot 2026-11-15 at 3 41 28 PM" src="https://github.com/user-attachments/assets/5b6a9aee-7971-46df-b3ce-879ee1175953" />
Objective: Create a local domain environment to manage users and computers. Environment:
* Windows Server 2022 (Domain Controller)
* Windows 11 (Client)
* Virtualization: [UTM]
Configuration Steps:
- [ ] Installed Windows Server and Windows 11 in virtual machines.
- [ ] Configured static IPv4 addresses on the same subnet.
- [ ] Installed Active Directory Domain Services (AD DS) and promoted the server to a Domain Controller.
- [ ] Created a standard user account in AD.
- [ ] Joined the Windows 11 client to the domain.
Troubleshooting & Lessons Learned:
* Issue: Windows 11 could not find the domain during the initial join attempt.
* Cause: The client was prioritizing an IPv6 DNS address over the IPv4 Active Directory DNS server.
* Resolution: Disabled IPv6 on both the server and client network adapters, flushed the DNS cache, and successfully joined the domain.
