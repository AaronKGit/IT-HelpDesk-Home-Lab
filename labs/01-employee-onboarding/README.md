# Lab 001 — New Employee Workstation Deployment

**Scenario:** Provision a Windows 11 Enterprise workstation for Sarah Miller, a fictional Accounting employee.

**Environment:** VirtualBox 7.2 · DC01 (Windows Server 2025) · Active Directory `corp.test` · PC02 (Windows 11 Enterprise) · DNS `10.10.10.10`

## Work completed
- Installed Windows 11 Enterprise on PC02 and configured its virtual networking.
- Pointed PC02 to the domain controller for DNS and confirmed name resolution using `nslookup corp.test`.
- Joined PC02 to the `corp.test` domain.
- Created domain account `CORP\smiller` and added it to the **Accounting** security group.
- Signed into PC02 as Sarah and verified identity and group membership using `whoami` and `whoami /groups`.

## Verification
| Check | Result |
| --- | --- |
| PC02 shows domain `corp.test` | Passed |
| Sarah appears in Accounting group members | Passed |
| `whoami` returns `corp\smiller` | Passed |
| `whoami /groups` contains `CORP\Accounting` | Passed |
| An administrator action prompted for elevated credentials | Observed |

**Outcome:** PC02 was joined to Active Directory, and Sarah's domain login and group membership were verified. Accounting file-share permissions were **not** configured or tested.

**Evidence:** Three screenshots were captured: PC02's domain membership, Sarah's Accounting group membership, and the `whoami` / `whoami /groups` output. A two-page PDF containing those images was produced separately.

*Personal training environment; fictional user and organization.*
