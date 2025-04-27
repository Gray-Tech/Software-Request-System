# Summer Refresh - Software Request System

This project is a streamlined replica of a real-world software request and deployment workflow, built using **Airtable** to automate and simplify traditionally messy, spreadsheet-based processes.

---

## 📋 Project Overview

This system was designed to handle:
- Lecturer software installation requests
- Licensing checks
- Deployment scheduling
- Testing and feedback collection

The aim was to **eliminate manual coordination**, **increase transparency**, and **accelerate** software deployment cycles.

---

## 🧱 Data Structure

The Airtable database consists of four interconnected tables:
- **Requests**: Lecturer software requests, driving the workflow.
- **Business Partners**: Licensing contacts for approval flows.
- **Testing Machines**: Devices available for software testing.
- **Default Software List**: Software already installed by default for user visibility.

**Entity Relationship Diagram**

![Software Requests ERD](images/SoftwareRequestERD.png)

---

## 🤖 Key Automations

Five Airtable automations were created:
1. Acknowledgement email sent after form submission.
2. Licence verification emails sent automatically if needed.
3. Approval/rejection flow for new licences.
4. Notification when software is ready for testing.
5. Feedback collection with pass/fail triggers to deployment team.

---

## 🎨 Interfaces

Three custom-built Airtable Interfaces:
- **Software Request Interface** (Lecturers): Submit and track software requests.
- **Business Partner Interface**: Approve or reject licence needs.
- **Deployment Team Interface**: Monitor ready-for-packaging and deployment status.

---

## 📈 Future Improvements

- Add permissions-controlled pages.
- Enhance interface styling and helper text.
- Expand dashboard summaries for better tracking.
- Refine data validation to improve submission quality.

---

## Interfaces:

**Software Request Form:**
*For users to submit new software requests.*
![Software Request Form](images/SoftwareRequestForm.png)

**Software Awaiting Test:**
*Filtered for users to see software they need to test, updating the "Test result value" field moves it through the flow.*
![Software Awaiting Test](images/SoftwareAwaitingTest.png)

**Default Software List:**
*A simple searchable list for users to check if the software they are requesting will already be installed.*
![Default Software List ](images/DefaultSoftwareList.png)

**Business Partner Licence Approval Screen:**
*For business partners to access any requests that don't have already have a license and approve or deny the request. Filtered for their division.*
![BP Licence Screen](images/BPLicenceApprovalScreen.png)

**Software Awaiting Packing for Testing:**
*Deployment team's interface to see any software that already has a license/has been approved for a license and set it to be ready for testing*
![Software Awaiting Packaging](images/SoftwareAwaitingPackaging.png)

**Dashboard Tracking Request Status:**
*Dashboard for seeing where all requests are in the process and acknowledge their key metrics: Waiting for packaging (where they need to act), waiting for testing (where users need to act), and ready for deployment (any items that have been successfully tested).*
![Requests Tracking Dashboard](images/SoftwareTrackingDashboard.png)

## Tables:

**Requests Table:**

![Requests Table](images/requests-table.png)
![Requests Table](images/requests-table2.png)

**Business Partners Table:**

![Business Partners Table](images/bp-table.png)

**Test Machines Table:**

![Test Machines Table](images/test-machines-table.png)

## Automation Flow:

![Automation Flow](images/SummerRefreshSimplePoolDiagram.png)

**Example of automation**

*For the sake of not adding many more screenshots, here is an example of one of the 5 automations*

Condition 1: Catch approval, if the license is added in retrospect, will update the record to skip BP approval.

Condition 2: If it meets conditions to see a BP and is denied, send an email to the user to let them know it was denied.

Condition 3: If it meets conditions to see a BP and it approved, update request status to approved so it can be packed for testing.

![BP Approval Flow](images/ExampleAutomation.png)

---

## 🧠 Lessons Learned

Over the course of this project, I moved from **zero Airtable experience** to completing both the **Intro to Airtable** and **Builder Essentials** paths, designing a real-world process from start to finish.  

Some key takeaways from this learning sprint:

- **Airtable’s relational database model** felt intuitive to me after a short time, especially because of my prior experience designing SharePoint Lists and managing relationships across Microsoft tools. Airtable expands on that foundation with a cleaner, more user-friendly structure that clicked quickly.
- **Automation building** inside Airtable was surprisingly familiar thanks to my work with **Power Automate** — the principles of triggers, actions, and conditional logic carry over almost 1:1. Within hours, I was confident building multi-step flows with email notifications, approval branches, and record updates.
- **Interfaces in Airtable** offer a fast, polished way to build user-centric forms and dashboards. Designing multiple Interfaces for different roles (Requestor, Business Partner, Deployment Team) reinforced how important **audience-focused design** is when trying to drive system adoption.
- Creating a **Swimlane Diagram** for the first time helped me visualise parallel processes much more clearly than standard flowcharts — something I will keep using in future scoping work.

---

## 🔥 Areas for Further Growth

Although I feel confident with Airtable fundamentals, I’ve identified several areas where I want to level up as I continue into the **Builder Advanced** path:

- **Advanced Automation Logic**: Building complex branching flows and multi-table automations, using conditional lookups and more sophisticated triggers.
- **Scripting**: Exploring Airtable’s Scripting Block to handle custom automation that goes beyond the standard action templates (e.g., looping through multiple records, applying mass updates).
- **API Integration**: Starting to experiment with Airtable's API for basic data pushes and pulls, understanding how Airtable fits into larger system architectures.
- **Permissions Management**: Designing secure, role-based Interfaces that maintain data visibility without overcomplicating user experience.
- **Polished Interface Design**: Pushing my Interface work further with better visual hierarchy, field grouping, and user onboarding guidance.
- **Polished Automation**: Going back through my automations and making sure to use correct triggers e.g. using "When a record matches conditions" instead of "When record is updated" to trigger less often.

---

## ✨ Closing Thoughts

This project was a strong reminder that **the fundamentals of good system design — clean data structures, clear automation logic, and user-first thinking — apply across platforms**.  
Moving into Airtable felt natural because those principles stayed constant, even as the tools changed.

I'm excited to continue building mini-projects, exploring deeper functionality, and sharpening my skills as a low-code developer.


