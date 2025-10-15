# Bulk Loader Test Cases

## Background
**Step 1:** The Bulk Loader form is open

---

## TestCase1: File is not opened and sheet does not contain percentage format
**Step 1:** A file is selected that is not open in Excel
**Step 2:** The user attempts to preview or process data
**Step 3:** The system should allow the operation to proceed
**Step 4:** No percentage format warning is shown

---

## TestCase2: File is not opened and sheet contains percentage format
**Step 1:** A file is selected that is not open in Excel
**Step 2:** The user attempts to preview or process data
**Step 3:** The system should allow the operation to proceed
**Step 4:** No percentage format warning is shown
**Step 5:** Percentage is correctly processed

---

## TestCase3: File is opened and sheet does not contain percentage format - small data set - up to 100 rows
**Step 1:** A file is open in Excel
**Step 2:** The selected sheet does not contain percentage formatting
**Step 3:** The user attempts to preview or process data
**Step 4:** The system should allow the operation to proceed
**Step 5:** No percentage format warning is shown

---

## TestCase4: File is opened and sheet does contain percentage format - small data set - up to 100 rows
**Step 1:** A file is open in Excel
**Step 2:** The selected sheet contains percentage formatting
**Step 3:** The user attempts to preview or process data
**Step 4:** The system should display an information message
**Step 5:** The operation is blocked until the file is closed

---

## TestCase5: File is opened and sheet does not contain percentage format - LARGE data set - at least 150k rows
**Step 1:** A file is open in Excel
**Step 2:** The selected sheet does not contain percentage formatting
**Step 3:** The user attempts to preview or process data
**Step 4:** The system should allow the operation to proceed
**Step 5:** No percentage format warning is shown

---

## TestCase6: File is opened and sheet does contain percentage format - LARGE data set - at least 150k rows
**Step 1:** A file is open in Excel
**Step 2:** The selected sheet contains percentage formatting
**Step 3:** The user attempts to preview or process data
**Step 4:** The system should display an information message
**Step 5:** The operation is blocked until the file is closed

---

## TestCase7: New file selected after first file was checked with a sheet containing percentage format without closing Bulk Loader
**Step 1:** A file was previously checked and found to have a sheet with percentage formatting
**Step 2:** A new file is opened and is selected with a sheet with percentage formatting
**Step 3:** The percentage format check is reset
**Step 4:** The system should display an information message
**Step 5:** The operation is blocked until the file is closed

---

## TestCase8: New file selected after first file was checked with a sheet not containing percentage format without closing Bulk Loader
**Step 1:** A file was previously checked and found to have no sheet with percentage formatting
**Step 2:** A new file is opened and is selected with a sheet with percentage formatting
**Step 3:** The system should display an information message
**Step 4:** The operation is blocked until the file is closed

---

## TestCase9: New sheet selected of a file already checked with a sheet containing percentage format without closing Bulk Loader
**Step 1:** A file was previously checked and found to have a sheet with percentage formatting
**Step 2:** A new sheet is selected in the same file without percentage formatting
**Step 3:** The percentage format check is reset
**Step 4:** The sheet is loaded without any issues

---

## TestCase10: New sheet selected of a file already checked with a sheet not containing percentage format without closing Bulk Loader
**Step 1:** A file was previously checked and found to have no sheet with percentage formatting
**Step 2:** A new sheet is selected in the same file with percentage formatting
**Step 3:** The percentage format check is reset
**Step 4:** The system should display an information message
**Step 5:** The operation is blocked until the file is closed

---

## TestCase11: File is opened, user closes the file, and retries
**Step 1:** A file is open in Excel and contains percentage formatting
**Step 2:** The user closes the file in Excel
**Step 3:** The user retries the operation
**Step 4:** The system should allow the operation to proceed

---

## TestCase12: Sheet name contains trailing '$'
**Step 1:** A sheet name contains a trailing '$'
**Step 2:** The system checks for percentage formatting
**Step 3:** The trailing '$' is ignored
**Step 4:** The correct sheet is validated

---

## TestCase13: Multiple sheets with similar names
**Step 1:** Multiple sheets exist with similar names (with and without '$')
**Step 2:** The user selects a sheet
**Step 3:** The correct sheet is validated and loaded