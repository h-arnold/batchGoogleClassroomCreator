# Batch Google Classroom Management Script

This Google Apps Script automates the creation and management of Google Classrooms based on data from a Google Sheet. It allows you to create classrooms, add teachers, and update classrooms using a custom menu in the Google Sheets interface.

## Setup Instructions

### Prerequisites

- A Google account with access to Google Sheets and Google Classroom.
- Basic understanding of Google Apps Script.

### Steps to Set Up

1. **Create a Google Sheet:**

   - Open Google Sheets.
   - Create a new spreadsheet.
   - Add the following headers to the first row (A1 to G1):

     ```
     Course ID | Name | Teacher 1 | Teacher 2 | Teacher 3 | Teacher 4 | Enrollment Code
     ```

2. **Add Your Data:**

   - Enter the course names and teacher email addresses under the respective columns.
   - The `Course ID` and `Enrollment Code` columns will be populated by the script.

3. **Open Apps Script Editor:**

   - In your Google Sheet, go to `Extensions` > `Apps Script`.

4. **Copy and Paste the Script:**

   -  Copy the script in code.gs and paste it over the exisiting `myFunction` code.
5. **Enable Google Classroom API:**

   - In the script editor, go to `Resources` > `Advanced Google Services`.
   - Enable the "Google Classroom API".
   - Click on the "Google Cloud Platform API Dashboard" link at the bottom.
   - In the GCP console, enable the "Google Classroom API".

6. **Authorize the Script:**

   - Run the `onOpen` function once to prompt authorization.
   - Follow the prompts to authorize the script.
  
  ## Usage

1. **Open the Google Sheet:**

   - Your custom menu should now appear in the Google Sheets interface under `Classroom Management`.

2. **Create Google Classrooms:**

   - Click on `Classroom Management` > `Create Google Classrooms` to create classrooms based on your sheet data.

3. **Update Google Classrooms:**

   - Click on `Classroom Management` > `Update Google Classrooms` to update existing classrooms and ensure the teachers are correctly assigned.

## Logging

- Check the execution log for any errors or messages by going to `View` > `Logs` in the script editor.

## Notes

- Ensure that the teacher email addresses in the spreadsheet are valid and have the necessary permissions to be invited to Google Classroom.
- The first teacher in the list (Teacher 1) is set as the owner of the classroom, and the others are invited.
