Using NodeJS create an application that will monitor a set of specific folders for new files, build an API link based on the folder location the file is in, post the file, and perform an one of two actions upon completion.

# Acquire the Source
* Visit our [GitHub Repository](https://github.com/Lab-Logistic-Services/CoderByte-Data-Sweep-Assessment) and clone the repository.

# Folder Structure
The following is the folder structure required for this application and is included in this repository.
* root_directory
  * application
  * log_files
  * 1000000
    * 1002
    * archive
    * exceptions
  * 1000001
    * 1007
    * archive
    * exceptions
  * 1000002
    * 1014
    * archive
    * exceptions  

# Requirements
* The system should utilize .env files for all custom configuration settings
* Only monitor the first sub directory for new files.
* The System should be able to process any type of file that hits the folder
* The system should be able to restrict file types based on settings in the .env file
* The system should be able to wait until the file is no longer open, or being written to before posting.
* The system should post to a route that is created using the file directory structure:
  * https://test-api.lablogserv.net/<parent_directory>/<sub_directory>/results
* The system should send the following with each API Post
  * File checksum with each post
* If status 200 is received:
  * The system should archive the file into a dynamically created archive folder by year and month
  * The system should Present a notification window that disappears after a customizable time period set in the .env file
* If a status other than 200 is received:
  * The system should move the file into a holding directory
  * The system should present a notification window, showing the error, that does not disappear and gives the user an option to submit a bug.
* The system should log the following events in a log file.
  * File detections
  * File Actions <Post & Response, Archive, Exceptions>
  * All Errors
* The log files should be rotated based on options settable from the .env file
  * Hourly
  * Daily
  * Weekly
  * Monthly
  * Size limit

# How to submit
Please upload the code for this project to GitHub, and post a link to your repository below.
