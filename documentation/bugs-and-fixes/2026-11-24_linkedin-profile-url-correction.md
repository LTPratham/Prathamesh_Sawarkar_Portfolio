# Bug Fix: LinkedIn Profile URL Correction

- **Date**: 2026-11-24
- **Author**: Antigravity Assistant & Prathamesh Sawarkar
- **Severity**: Low (Contact / External Navigation)

---

## 1. Description
The LinkedIn contact link in the portfolio contact section and documentation pointed to an generic handle (`/in/prathamesh-sawarkar`) which redirected to someone else's LinkedIn profile instead of Prathamesh Sawarkar's personal profile.

## 2. Steps to Reproduce
1. Scroll down to the `#contact` section on the portfolio page.
2. Click on the **LinkedIn** contact card.
3. Observe that LinkedIn opens an unrelated profile instead of Prathamesh's actual account (`prathamesh-sawarkar-43b497319`).

## 3. Root Cause
The URL was previously configured with placeholder vanity slug `https://www.linkedin.com/in/prathamesh-sawarkar` rather than the exact public profile link `https://www.linkedin.com/in/prathamesh-sawarkar-43b497319/`.

## 4. Fix Applied
- Updated `index.html` to point to `https://www.linkedin.com/in/prathamesh-sawarkar-43b497319/` and updated displayed slug to `/in/prathamesh-sawarkar-43b497319`.
- Updated `README.md` contact section link to `https://www.linkedin.com/in/prathamesh-sawarkar-43b497319/`.

## 5. Files Modified
- `index.html` (Line 1722-1725)
- `README.md` (Line 146)

## 6. Verification
- Verified link target and displayed slug match `https://www.linkedin.com/in/prathamesh-sawarkar-43b497319/`.
- Validated target attributes (`target="_blank" rel="noopener"`).
