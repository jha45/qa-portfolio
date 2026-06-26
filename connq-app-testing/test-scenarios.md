# Test Scenarios — ConnQ v1.0.5

| # | Feature | Test Performed | Result | Notes |
|---|---------|---------------|--------|-------|
| 1 | Onboarding | Sign up with valid email and password | Pass | Account created successfully |
| 2 | Onboarding | Login with valid credentials | Pass | Logged in successfully |
| 3 | Onboarding | Login with incorrect password | Pass | Correct error handling |
| 4 | Onboarding | Forgot password flow | Pass | OTP sent and flow completed |
| 5 | Profile Creation | Fill all fields and save | Fail | Bug #2 — Field of Interest not persisted |
| 6 | Profile Creation | Upload a profile photo | Pass | Photo uploaded and displayed correctly |
| 7 | Profile Creation | Enter emoji in name field | Fail | Bug #7 — Save blocked entirely |
| 8 | Profile Creation | Exceed field character limit | Pass | 10-digit limit enforced correctly |
| 9 | QR Code | Generate QR code | Pass | QR displayed clearly |
| 10 | QR Code | Cross-device QR scan (iOS scanning Android) | Pass | Correct profile opened |
| 11 | Sharing | Share profile via WhatsApp | Pass | Link sent; Bug #6 — preview not personalized |
| 12 | Receiver Experience | Open link without app installed | Partial | Reachable; full rendering unconfirmed |
| 13 | Receiver Experience | Add to Phone contacts | Pass | Contact saved successfully |
| 14 | Multi-Profile | Create second (Business) card | Pass | Bug #8 — business name truncated |
| 15 | Multi-Profile | Switch between profiles | Pass | No data bleed between cards |
| 16 | Privacy | Mark a contact field private | Not Tested | Feature not found in UI |
| 17 | Privacy | Mark a contact field public | Not Tested | Feature not found in UI |
| 18 | Analytics | View Insights after profile activity | Partial | Bug #5 — no auto-refresh |
| 19 | Permissions | Review permissions on install | Pass | All permissions reasonably justified |
| 20 | Network | Use app offline | Pass | Cached cards viewable; correct error on save |
| 21 | Stability | Background app mid-edit, resume | Pass | Unsaved edit preserved |
| 22 | Cross-Platform | Same account on Android + iOS | Pass | Profile opened correctly on both |
| 23 | UI/UX | Rotate device / different screen sizes | Pass | Layout adapted correctly |
| 24 | Session | Log out and back in | Pass | Data persisted correctly |
| 25 | Theming | Switch dark mode; confirm persistence | Pass | Theme applied and persisted |
| 26 | Settings | Confirm version info and policy links | Pass | Version and links present |
| 27 | Analytics | Cross-check Top Actions counts | Fail | Bug #4 — Call and Save to Gallery not tracked |
| 28 | Sharing | Inspect shared link metadata | Fail | Bug #6 — generic Open Graph tags |
| 29 | Billing | Start PRO trial | Pass | No payment info required |
| 30 | Profile Creation | Business name display vs entered value | Fail | Bug #8 — only first word shown |
