# COMP 4350 Proposal (Team Co-App)

### Project Summary and vision 

<u>**Summary**</u>

CoApp is a co-op application management platform, a comprehensive web application designed to streamline the student experience of the co-op job search. This platform uses React, Spring Boot, and MongoDB to address the most common challenges faced by students throughout their co-op job searches and provides an all-in-one space to manage job applications, interview preparations, and researching potential employers. 

This application takes all the essential co-op organizational tools and puts them in one user-friendly interface. Students can track their job applications from the start to their outcome, maintain interview schedules for these applications with a calendar view, and access a communal “rate my co-op” review board to see what others think about their work terms. This app gets rid of the need for multiple scattered spreadsheets, tracking apps, or unorganized notes.

<u>**Vision**</u>

Our vision with CoApp is to turn the co-op job search from a stressful, disorganized experience into something supportive and structured. As co-op students, we know very well that students juggle dozens of applications at once, trying to balance academic and personal responsibilities along the way. With all of this in mind, it's easy to feel overwhelmed or even miss deadlines and opportunities because of how daunting the job search itself can be. CoApp will hopefully help support students as they take more control over their careers by giving them the tools they need to stay organized throughout this process and ease the stress of keeping track of everything co-op related. 

Beyond just organization, we envision building a communal aspect into this app where students can share knowledge and experiences they gained throughout their work terms, and give their opinions on employers as they navigate their co-op journey. Together, students will be able to make more informed decisions about their co-op terms and applications by using the opinions and experiences of their peers. Usually, this information for students is limited to their immediate network. Now, they can see the thoughts of all the co-op students before them.


<u>**Stakeholders**</u>

Co-op Students:
Students can prepare for their upcoming work term by creating an account to track all their job applications. They can also log their interviews, application status, and see everything in one calendar view to avoid scheduling conflicts. After interviews, they can save their questions and practice them later on for future opportunities with other companies. They can also read reviews on companies to prepare themselves for how they will strategize their applications. 

Co-op Alumnus:
Once graduated, alumni can create an account to share their own experiences with current students by writing reviews for companies they worked at, providing insight into the interview process, work culture, compensation, and tech stack. These stakeholders can help build a knowledge base that guides future students and helps them make more informed decisions about their applications.

Co-op Coordinators:
A coordinator can benefit from students using this platform. Their students will be more organized and prepared throughout the job search process. When students come for advising or review sessions, they will have more organized data about their applications or related documents to reference. Coordinators can recommend this app as a platform for the best organizational practices while managing their applications, resulting in less student stress and better application outcomes, which reflects better on the coordinator and their program. 


### Core Functional Features/User Stories

Below we have our functional features and user stories. We have
1. User Authentication

- Co-op students need a way to manage their career data and interview notes. So, they should be able to create an account on the platform and manage their login information.
- Priority: High
- Cost: 3 Days

- Create Account: As a co-op student, I want to create an account using my email so I can save my application history and information.

    - <u> Acceptance criteria: </u>

	    - Given that I’m on the log-in screen and want to make a new account, when I click the “create new account” button, then I am greeted with a new interface to submit an email and password.
	    - Given that I’m looking at the interface to submit an email and password, when I submit a valid email that is not already associated with an account and a “valid” password, then an email will be sent to the email address I submitted that contains a verification code and I’m greeted with a new interface prompting me for that code.
	         - “Valid” password criteria: Must not be empty (must contain at least one non-whitespace character). Cannot start with a whitespace character. Cannot end with a whitespace character
	    - Given that I’m looking at the interface to submit an email and password, when I submit an invalid email then I will be shown a message saying that the email I submitted was invalid.
	    - Given that I’m looking at the interface to submit an email and password, when I submit an email already associated with an account then I will be shown a message saying that I must choose a different email.
	    - Given that I’m looking at the interface to submit an email and password, when I submit an invalid password, then I will be shown a message saying that the password I submitted was invalid.
	        - “Valid” password criteria: Must not be empty (must contain at least one non-whitespace character). Cannot start with a whitespace character. Cannot end with a whitespace character
	    - Given that I have access to that email address and see the email containing the verification code, when I take that code and input it into the new interface, then I will have successfully made an account and can log-in using the email/password combination that I put in.
	    - Given that I have access to that email address and don’t see the email containing the verification code, when I want to receive a new code because I didn’t receive it, then I can press a “re-send code” button on the screen to receive a new code.

- Login: As a co-op student who already has an account on the platform, I want to log in so I can access my data.

    - <u> Acceptance criteria: </u> 
	    - Given that I’m logged-out, have an account created, and on the log-in screen, when I type in my email and password correctly, then I will be logged-in, be able to access my data, and perform actions on the application.
	    - Given that I’m logged-out, have an account created, and on the log-in screen, when I type my email/password incorrectly, then I will be prompted to try again, my data will be inaccessible, and I will not be able to any actions on the application

- Log Out: As a student who’s already logged in, I want to log out because I’m using a library computer and I don’t want anyone else to be able access my private information.
   - <u> Acceptance criteria: </u> 
	   - Given that I’m logged-in and want to log-out, when I click the “log-out” button then I will lose access to my data and will be unable to perform the app’s functionalities

- Change Password: As a co-op student, I have made an account, but I forgot my password, and I would like to access the platform again, so I want a way to change my password securely.
   - <u> Acceptance criteria: </u> 
	   - Given that I am logged in and want to change my password, when I click the “edit profile” button at the top of the screen, then I will see a page that contains a “change password” button.
	   - Given that I’m on the “edit profile” screen, when I click on the “change password” button, then I will see an interface with fields to input my current password and my new password
	   - Given that I see the “change password” interface, when I input my current password correctly with a new, valid password, then the password I use to log into this account changes to the new password that I sent.
	        - “Valid” password criteria: Must not be empty (must contain atleast one non-whitespace character). Cannot start with a whitespace character. Cannot end with a whitespace character
	    - Given that I see the “change password” interface, when I input my current password incorrectly, then I will see a message saying that I put in an incorrect password
	    - Given that I see the “change password” interface, when I input my current password correctly but input an invalid password as my new password, then I will see a message saying that my new password is invalid
	    - Given that I see the “change password” interface, when I input my current password correctly but put in that same password as my new password, then I will see a message saying that my new password can not be my old password
	    - Given that I’ve successfully changed my password, when I log-in with my new password then I will be granted access to my account and be logged-in
	    - Given that I’ve successfully changed my password, when I log-in with my old password then I will be denied access and see a message saying “wrong password”

2. Log Job Applications

- Students want a place to record every job that they plan to apply for in order to replace their messy spreadsheets. They should be able to enter company names, job titles, links to postings, and track the application status so they can keep everything in order.
- Priority: High
- Cost: 5 Days

- Log New Application: As a co-op student, I want to create a new application entry with a company’s name, job title, deadline date, and link to the source so I have a record of my job hunt.
    - <u>Acceptance criteria:</u>
	    - Given that I’m on a page for showing all the applications I’ve logged, when I click on a button that says “add new application”, then I will see a new interface that will allow me to input a company name, job title, deadline date, and a link
	    - Given that I see the interface for submitting the new application, when I input these fields and click a submit button, then a new application will be added to my list with these details
	    - Given that I see the interface for submitting the new application, when I input an empty company name or job title (“empty” as in I leave it blank or input a name/job title that is only empty characters) then I will be shown a message saying that I the name/job title is invalid and I will not be allowed to press submit
	    - Given that I see the interface for submitting the new application, when I don’t select a deadline date then I will see a message saying to select a date and will not be allowed to press the submit button
	    - Given that I successfully added a new application, when I return to the page showing the applications I’ve logged, then I can see the new application within the list.

- Delete Entry: As a co-op student, I want to delete an application entry because I sometimes make duplicates or mistakes and want to keep my list clean.
    - <u>Acceptance criteria:</u>
	    - Given that I’m on the page for showing all the applications I’ve logged and I want to delete an application, when I click on a “trash” button next to the application I want to delete, then I will be prompted with a confirmation for deleting the application
	    - Given that I see the confirmation prompt, when I click on the “confirm delete” button then the application will be deleted and I will be returned to the page showing my my applications, where I will no longer see the deleted application
	    - Given that I see the confirmation prompt, when I click “cancel” then the application will not be deleted and I will be returned to my list of applications, where I will be able to see the application that I canceled the deletion for.

- Update Status: As a job seeker, I want to change the status of an application ("Not Applied", "Applied", "Interview Scheduled", etc.) so I know which applications require my attention.
    - <u>Acceptance criteria:</u>
	    - Given that I’m on the page showing all the applications I’ve logged, when I press on an “update status” button next to an application whose status I want to change, then I will see a way to select from different statuses to set as well as a cancel button.
	    - Given that I see this means of setting a status to the application, when I press on one of these statuses then I am returned to the list of applications and the status will be changed to the one I selected
	    - Given that I see this means of setting a status to the application, when I press the cancel button then I am returned to the list of applications and the status remains unchanged to what it was previously

- Edit Application Details: As a co-op student, I want to edit the details of an existing application because I realize I made a typo in one of the fields.
    - <u>Acceptance Criteria:</u>
	    - Given that I’m on the page showing all the applications I logged and given that I have previously logged an application, when I click on an “edit application” button that appears next to an existing application, I will see an interface for changing the company name, job description, job title, and link to the application
	    - Given that I’m looking at the new interface for changing the job’s details, when I change one of the fields and click “submit”, then I will be returned to the page showing all my applications, with the new changes I just input being shown
	    - Given that I’m looking at the new interface for changing the job’s details, when I click “cancel”, then I will be returned to the page showing all my applications, with no changes to the applications
	    - Given that I’m looking at the new interface for changing the job’s details, when I don’t change any of the fields, then I will not be able to click submit


3. Application Filtering/Search
- Co-op students will often apply for many jobs, sometimes 30+, so they need a way to find specific information within the large lists of applications; they may want to find a specific company or filter out unimportant ones.
- Priority: Medium
- Cost: 3 Days
- Search by Company Fields: As a co-op student, I want to search my applications by the name of the company so I can quickly pull up the company's information when I get a phone call from the recruiter out of the blue.
    - <u>Acceptance Criteria:</u>
	    - Given that I’m on the “applications” screen, when I type in a search bar, then I will see a list of applications that “match” what I input into the search bar, while applications that don’t “match” are hidden
	    “Match” to be decided later. Either “starts with” or some other fuzzy search quality.
	        - Currently the plan is to perform the filtering with every keystroke, but if this leads to performance issues then we can have it change to filter on click of a search button
	    - Given that I have typed something into a search bar, then when I delete the input, then I will see the full list of applications once more

- Filter by Status: As a co-op student with many ongoing applications, I want to filter my list to show only "Active" or "Interviewing" applications because I don’t want to see the rejections.
    - <u>Acceptance Criteria:</u>
	    - Given that I’m on the applications screen, when I click on a “filter by status” button, then I will be shown a list of statuses that I can select from
	    - Given that I see the list of statuses, when I click on one or more of the statuses, then I will only see applications that have statuses that match my selections.
	    - Given that I’m on the applications screen and have previously selected statuses to filter by, when I click on a “filter by status” button, then I will be shown the list of statuses again
	    - Given that I see the list of statuses and have previously selected statuses to filter by, when I click on one or more of the statuses that I have previously selected, then I have de-selected those statuses as filters.
- Sort by Date: As a co-op student, I want to sort my applications by "Date Applied" so I can identify applications I submitted weeks ago that I haven't heard back from and decide whether to move on.
	    - <u>Acceptance criteria:</u>
	    - Given that I’m on the applications screen, when I click on an “up arrow” button next to the date applied field, then I will be shown the list of applications in order of the date ascending
	    - Given that I’m on the applications screen, when I click on an “down arrow” button next to the date applied field, then I will be shown the list of applications in order of the date descending
	    - Given that I’m on the applications screen and have previously selected one of the up or down arrows, when I clicked on the arrow that I selected, then the list will be returned to its “default” ordering
	        - Default refers to however the API sends it back the application list

4. Company Wiki ("Rate My Co-op")

- Co-op students want to know more about the companies they’re applying to than what’s on the job application. They should be able to access a shared list of companies to read reviews from former co-op students about culture, pay, or tech, and also be able to add their own experiences.
- Priority: Low
- Cost: 5 Days
- Add Company Profile: As a student, I want to create a profile for a Company (Name, Location, Website) if it doesn't exist.
	- <u>Acceptance criteria:</u>
	    - Given that I’m on the Company Wiki screen and want to create a new company entry, when I click the option “Create A New Company Profile” within the page, then I will be directed to the Create A New Company form to create a new company profile. 
	    - Given that I have completely filled in the form with valid information and the company has not yet been created, when I select the “Create” option, then I should see a notification saying the company profile is successfully created. 
	    - Given that I have completely filled in the form with valid information and the company has been created, when I select the “Create” option, then I should see a notification saying the company already exists and the company profile could not be created.
	    - Given that I have incompletely filled in the form, when I select the “Create” option, then I should remain on the form and the missing fields should be displayed in red. 
- Write Review: As a former co-op at a company, I want to post a star rating and a written review for a company I worked at so I can help my fellow co-op students.
	- <u>Acceptance criteria:</u>
	    - Given that I’m on the Company Wiki screen, when I click on a company name, then I should be directed to the company profile. 
	    - Given that I’m looking at a company profile, when I scroll to the reviews section, then I should see an option “Add A New Review”. 
	    - Given that I’m looking at the option “Add A New Review”, when I click the option, then I should be directed to the form to add a new review. 
	    - Given that I’m looking at the form to add a new review, when I fill in the form with both star rating and a written review and I click the option “Submit”, then I should see a notification saying that the review has been created. 
	    - Given that I’m looking at the form to add a new review, when I fill in the form with only the star rating and I click the option “Submit”, then I should see a notification saying that the review has been created. 
	    - Given that I’m looking at the form to add a new review, when I click the option “Submit” without selecting a star rating and entering a written review, then I should remain on the form and there should be a message saying “Please add a star rating to share your review”.
	    - Given that I’m looking at the form to add a new review, when I enter a written review but does not select a star rating and I click the option “Submit”, then I should remain on the form and there should be a message saying “Don’t forget to add a star rating to submit your review”. 
- Read Reviews: As a co-op student, I want to read reviews from other students about a company's interview process so I can prepare.
	- <u>Acceptance criteria:</u>
	    - Given that I’m on the Company Wiki screen, when I click on a company name, then I should be directed to the company profile. 
	    - Given that I’m looking at a company profile, when I scroll to the reviews section, then I should be able to see the reviews about the company. 
	    - Given that I’m looking at the reviews about the company, when I scroll down to see more reviews, then I should be able to see an option “See More Reviews”. 
	    - Given that I’m looking at the option “See More Reviews”, when I click the option, then I should be directed to another page that displays all the reviews for the company. 


5. Interview Calendar
- Interview schedules and application deadlines can get quite hectic, so Co-op students want to visualize their applications and schedule to avoid conflicts. They should be able to see their upcoming interviews and application deadlines with a calendar view.
- Priority: Low
- Cost: 4 Days
- Log Interview Date: As a user, I want to add a specific date and time for an interview to an application entry so the system can track my schedule.
    - <u>Acceptance criteria:</u>
	    - Given that I’m on the Interview Calendar page and I want to log a new interview date, when I click on the option “Add A New Interview”, then I should be directed to the form to add a new interview. 
	    - Given that I’m looking at the form to add a new review, when I fill in the form with the company, interview date, and interview time and I click “Submit”, then there should be a notification saying that the interview has been successfully created. 
	    - Given that I’m looking at the form to add a new review, when I click “Submit” without completely filling in the form (missing at least one of the following: company, date, and time), then I should remain on the form and the missing fields should be displayed in red. 
- Monthly Calendar View: As a visual learner, I want to view a monthly calendar with my interview dates and application deadlines so I know what to prioritize and see where I have conflicts with my classes.
    - <u>Acceptance criteria:</u>
	    - Given that I’m on the Interview Calendar page, when I look at the calendar in the page, then the current month should be shown by default. 
	    - Given that I’m looking at the calendar, if I click the next month arrow located on the top right corner of the calendar, then the next month should be shown. 
	    - Given that I’m looking at the calendar, if I click the previous month arrow located on the top right corner of the calendar, then the previous month should be shown. 
	    - Given that I’m looking at the calendar and I have previously logged an interview, when I navigate to the month in which the interview is scheduled, then the interview should be visible in the calendar. 
	    - Given that I’m on the Interview Calendar page and I have upcoming interviews or application deadlines, when I look at the calendar, I should see my upcoming interviews or deadlines listed on their scheduled dates. 
	    - Given that I’m on the Interview Calendar page and I have no upcoming interviews or application deadlines, when I look at the calendar, I should see a message stating that I have no upcoming scheduled interviews or application deadlines. 
- Quick Navigation: As a co-op student, I want to click an event on the calendar to jump directly to the full application details so I can quickly get to any important information for that day like an interview.
	- <u>Acceptance criteria:</u>
	    - Given that I’m on the Interview Calendar page and I have previously logged an interview, when I click on the interview in the calendar, then there should be a popup showing the interview details (company name, date, time). 
	    - Given that I’m looking at the popup displaying the interview details, when I locate and click the X button in the top right corner of the popup, then the popup should close and I should be redirected back to the Interview Calendar page. 
	    - Given that I’m looking at the popup displaying the interview details, when I click outside the popup area, then the popup should close and I should be redirected back to the Interview Calendar page. 
	    - Given that I’m on the Interview Calendar page and I have previously logged multiple interviews on the same day, when I locate the day in the calendar and click on one of the interviews listed for that day, then there should be a popup showing the correct details for the selected interview. 


6. AI Resume Helper
- Co-op students often struggle with writing their resumes and cover letters, so they can use the platform's built-in chatbot integration to get assistance.
- Priority: Low
- Cost: 5 Days
- Enter a query: As a student, being able to ask a chatbot questions to tailor my resume bullet points to a specific job posting would help me write and improve my resume.
	- <u>Acceptance criteria:</u>
	    - Given that I’m on the main page, when I select the option “Improve my resume with AI” located on the navbar, then I should be directed to the conversation UI like ChatGPT.
	    - Given that I’m on the conversation UI, when I copy and paste sections of my resume into the prompt and ask the AI chatbot to perform the tasks, then I should be able to see the feedback from the chatbot about my resume. 
- Auto-fill job context: As a co-op student, I want to click a button on an application entry to automatically send that job's details to the AI chatbot so I don't have to copy-paste the job description myself.
	- <u>Acceptance criteria:</u>
	    - Given that I’m on the main page, when I select the option “Improve my resume with AI” on the navbar, then I should be directed to the conversation UI like ChatGPT.
	    - Given that I’m on the conversation UI, when I click on the option "Select a job", then I should see a selection of the jobs that have been listed so that I can ask the AI chatbot for specific feedback for the selected job listing.
	    - Given that I clicked on the option "Select a job" and I see the listed jobs, when I select one of the jobs, then I will receive specific feedback from the chatbot regarding tailoring my resume to that job.
- Understand context about me: As a co-op student, I don’t want to tell the AI the same information about me every time, so I want a place to enter information about myself like technical skills, job experience, etc so that it can better tailor its responses for me.
	- <u>Acceptance criteria:</u>
	    - Given that I’m on the main page, when I select the option “Improve my resume with AI” on the navbar, then I should be directed to the conversation UI like ChatGPT.
	    - Given that I’m on the conversation UI, when I perform prompting with GenAI as in feature 1, I should receive feedback from the AI chatbot with the context of my profile.

**Additional Features**

7. Personal Interview Question Bank
- Co-op students find practicing for interviews very challenging. So, they need a space to practice technical and behavioural questions that were asked or that they found elsewhere.
- Priority: Low
- Cost: 2 Days
- Log Question: As a student, I want to log specific technical questions I was asked after an interview so I don't forget them and can study them later.
- Practice existing questions: As a student, I want to go through the practice questions in a randomized order.
- Tag by Topic: As a user, I want to tag questions by topic so I can filter my list and study specific categories that I struggle with.

8. Documents for Jobs
- Priority: Low
- Cost: 2 Days
- Upload Targeted Resume
- Link Cover Letter
- Download Uploaded Stuff

9. Application Statistics Dashboard
- Priority: Low
- Cost: 2 Days
- Status Distribution Chart
- Total Count Metrics


10. Peer Document Review
- Priority: Low
- Cost: 4 Days
- Request Critique
- Leave Comments
- Resolve Feedback


### Technologies:
1. React 
2. React Bootstrap 
3. MongoDB 
4. Spring/Springboot 
5. OnRender (frontend/backend hosting)
6. Atlas (MongoDB hosting) 
7. GitHub Docker 
8. GitHub Actions 
9. Gradle 
10. npm/node 
11. Vite (front-end)


### Timeline

| Date | High Priority Tasks | Additional Tasks |
|-----|---------------------|------------------|
| Sprint 2, Week 1 (February 6) | - Start developing a Testing Plan according to the sprint 2 requirements.<br>- Create sequence diagrams for features 1-3. | - Complete Feature 1: User Authentication which includes: Create Account, Login, Logout, Change Password<br>(there has already been significant headway on this feature prior to sprint 2) |
| Sprint 2, Week 2 (February 13) | - Start developing the backend for Feature 2 and 4. Specifically, start implementing the API.<br>- Finalize the testing plan. | - Feature 2 and Feature 4 front-end development: have a basic UI ready. |
| Sprint 2, Week 3 (February 27) | - Finalize detailed testing for features 1,2 and 4. | - Start planning out features 3,5 and 6, including api design and sequence diagrams |
| Sprint 2, Week 4 (March 6) | - Finalize deployment, put out fires<br>- Polish all existing code in the repo before submission.<br> - UI review for features 1,2,4 | - Start developing the backend for Feature 3 and 5. Specifically, start implementing the API designed already.<br>- Start on presentation for technique seminar |
| Sprint 3, Week 1 (March 13) | - Have basic UI complete for features 3 and 5<br>- Finish and showcase technique seminar presentation| - Implement the API in the backend for Feature 6. 
| Sprint 3, Week 2 (March 20) | - Finalize detailed testing for features 3 and 5.<br>- Begin Final Report | - Have basic UI ready for feature 6. |
| Sprint 3, Week 3 (March 27) | - Polish all existing code in the repo before submission.<br>- Finalize Final Report | - UI review for features 3,5 and 6 |
| Sprint 4, Week 1 (April 3) | - Perform load testing and integrate security scanning into CI Pipeline | - Complete and prepare for Presentation. |



