# Microsoft 365 Defend the Tenant

Hardening of a Microsoft 365 lab tenant against ten Microsoft Secure Score
recommendations, with a security brief explaining the decisions, trade-offs
and recommendations.

## Controls implemented

1. MFA for administrative roles (phishing-resistant)
2. MFA for all users
3. Block legacy authentication
4. MFA for medium and high sign-in risk
5. Remediation for high user risk
6. Prevent user application consent
7. Invited-only Teams lobby bypass
8. Organizer-only Teams presenters
9. Block anonymous Teams meeting join
10. Self-service password reset for all users

All Conditional Access policies are enforced, with one role-assignable
break-glass group as the only exclusion.

## Key finding

Mid-way through, every policy excluded the Global Administrator role. The
assessment reported "implemented" while the most powerful accounts were
unprotected. The exclusion was removed after an admin passkey and the
emergency accounts were tested. A passing score is not the same as protection.

## Screenshots

| Image | Shows |
| --- | --- |
| `images/01-ca-policy-list.png` | Conditional Access policies CA001-CA005, all On |
| `images/02-ca001-grant.png` | Phishing-resistant authentication strength for admins |
| `images/03-ca003-client-apps.png` | Legacy auth block: Exchange ActiveSync + Other clients |
| `images/04-ca005-grant.png` | Risk remediation + MFA strength, Every time |
| `images/05-user-consent.png` | Do not allow user consent |
| `images/06-teams-meeting-policy.png` | Lobby, presenters and anonymous join settings |
| `images/07-sspr-all.png` | Self service password reset enabled = All |
| `images/08-assessment-results.png` | Final assessment: 10 implemented |

## Author

Name: KANISHAK GADHAVI
