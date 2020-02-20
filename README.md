# Role Name:
- ansible-role-compliance-windows-password-policy-2019

# Description:
This Password Policy Role was based off the CIS specs for 2019 servers.   This
role covers the "Password Policy" section only. The checks and remediation
commands are for local settings only. Group Policy settings may override these
settings. When the "remediate" variable is set to "YES", the role will try to
remediate the server's setting(s) accoridng to the CIS standards.  The
defaults/main.yml file can be used to disable specific CIS items (i.e.
"execute_<cis task #>") from executing. The default value in the
defaults/main.yml for these CIS item variables (i.e. "execute_<cis task #>")
is set to "YES". The value "YES" means that the CIS item will execute at run
time. Set the value to "NO" if you want to skip this CIS item in question
from executing.

# Requirements:
Windows Ansible related pre-requisites

# Defaults file for ansible-role-compliance-windows-password-policy-2019:
# Variables

Parameter | Choices/Defaults|Comments
----------|-----------------|--------
__remediate__ |"NO"| variable used to determine whether or not to remediate.
__minPWage_cis__ |1| CIS Value.
__maxPWage_cis__ |60| CIS Value.
__minPWlgth_cis__ |14| CIS Value.
__lngth_pw_history_cis__ |24| CIS Value.
__LT_cis__ |10| CIS Value.
__lckt_drtn_cis__ |15| CIS Value.
__LOW_cis__ |15| CIS Value.
__approved_windows_ver__ |2019| approved windows version for this role.


# Example Playbook:
---
 - hosts: [win]
   roles:
   - ansible-role-compliance-windows-password-policy-2019


# Author Information:
Richard M. Williams

rmwill@us.ibm.com
