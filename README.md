For this problem statement, I am proposing a new solution to remove the manual intervention and directly automate the complete process. I have developed a UI dashboard which has parameters to select the client name, select the time duration for which the records are needed, start date and end date, select the file combinations from the drop-down mentioned, and hit the submit button. The background scripts will run and finally generate the IR link and send a success email to the PS Team. I want to add this in the proposed solution section of my slide. Please give me text as your output of this slide in the bullet points format in a crisp, brief, formal language.




Process flow 

The process flow for the current implementation goes as follows. First step, the client requests the data, sharing the time duration and the required file combinations format. The files has to be in the pairs, that is the requirement from the business side. Now, there is an automated script which runs in the backend. The script steps are as follows. It goes to the S3 database, it accesses the database, then it extracts the documents for that time duration and it gets downloaded to the local system of the team mate. Now, if the file combination required is in HTML plus XML format, then the teammate has to check if all the HTML files for that time duration are being downloaded from the database.There is a new script which has the following steps. The script picks the file, for example, XML file, it takes the file name and then goes to the S3 database and matches the name with the HTML format. In this fashion, all the HTMLs corresponding to the XML files are downloaded into another folder on the local system. If the HTML file is not found, then there is an issue.The txt file corresponding to the html files that are missing that have to be downloaded manually from the database.Once this is done, the next step comes to zip the files into folders. But here is a problem of the file size restriction. The zipped folder size has to be less than 1.5 GB. For example, if the file combination pairs are HTML and XML, then each quarter duration folders are around 1.5 gb after zipping. Hencoe for 1 year, we need 4 zipped folders. If eg. txt + xml file combination, then 1 year data are zipping is approx 1.2 Gb. 

Now the final step, We have tools to generate the IR links for each corresponding zipped folder that is created manually. And these IR links are then uploaded to the Akamai server and finally the links are given to the client as per requirement. After a specific duration, the links are purged i.e. destroyed once the client has downloaded all the data. These are all the steps that are mentioned in the process flow. I want to add this in a new slide for the presentation. Please give me crisp, clear, brief, and short data in the bullet points format in formal language. Your output should be in the text format.





Process flow OUTPUT

Client Request: Client shares time duration and required file format combinations (e.g., HTML + XML).

Data Extraction: Backend script fetches documents from S3 for the given duration and downloads them locally.

File Pairing Check:

Team manually verifies availability of required file pairs (e.g., HTML with XML).

If HTML is missing, a secondary script matches filenames and downloads corresponding HTML files.

Missing files (e.g., TXT) are downloaded manually from S3.

File Packaging:

Files are zipped into folders with a strict size limit of 1.5 GB.

E.g., HTML + XML for 1 year → 4 zipped folders (quarterly), TXT + XML → ~1.2 GB per year.

IR Link Generation & Delivery:

IR links are generated for each zipped folder and uploaded to the Akamai server.

Links are shared with the client and purged after the download window expires.


Proposed solution OUTPUT

A UI dashboard allows selection of:

Client Name, Start & End Dates, Time Duration, and File Combinations

On submission, backend automation performs the following:

Retrieves all required files and valid pairs directly from S3

Automatically detects and downloads missing HTML files to ensure complete pairing

Eliminates manual file size checks by:

Splitting data into 3-month intervals per folder

Ensuring each zipped folder remains under the 1.5 GB size limit

Packages files, generates IR links, uploads to Akamai

Sends a success email notification to the Production Support Team



Advantages of the New Solution Implemented
End-to-end automation eliminates manual intervention in file retrieval and processing.

Significant reduction in turnaround time for fulfilling client historical data requests.

Improved accuracy and consistency in file pairing and packaging.

Automated folder size management ensures zipped files comply with the 1.5 GB limit.

Scalable and reusable solution for onboarding multiple clients with varying requirements.

User-friendly UI dashboard enables easy parameter selection without technical expertise.

Automated email notifications improve communication and tracking for the Production Support Team.

Enhanced reliability in IR link generation and delivery through streamlined backend processes.
