---
layout: home
title: Local Explanations for Deep Learning Models
nav_exclude: true
toc: true
seo:
  type: Course
  name: Local Explanations for Deep Learning Models
---

# {{ site.tagline }}
{: .no_toc .mb-2 }
{{ site.description }}
<br>
TuTh / 09:10AM-10:30AM, [GC 2781](https://map.utah.edu/index.html?code=GC)
{: .fs-6 .fw-300 }

{% assign instructors = site.staffers | where: 'role', 'Instructor' %}
{% for staffer in instructors %}
{{ staffer }}
{% endfor %}

{% assign teaching_assistants = site.staffers | where: 'role', 'Teaching Assistant' %}
{% assign num_teaching_assistants = teaching_assistants | size %}
{% if num_teaching_assistants != 0 %}

{% for staffer in teaching_assistants %}
{{ staffer }}
{% endfor %}
{% endif %}

Office hours are **TBD**.

## Announcements

* **8/8: Course website is live.**
  Welcome.
  
## Description

Although neural models have obtained great success across various machine learning (ML) tasks in recent years, they are poorly understood. Consequently, people (including ML experts) have little perception of how to control ML systems they interact with and are typically left wondering:

* Which part of the input led to assigning this label?            
* How to change the answer to another?                           
* In plain English, why is this input assigned this label?                        
* Which training examples caused the prediction?                      

In the first part of this course, we'll go over methods that aim to address these questions. These methods are developed by ML researchers, usually without involving experts in other fields and human subjects such as doctors or fact checkers. 

In the second part of this course, we will revisit evaluation of these methods and focus on how to develop and evaluate methods that best accomplish a specific utility of explanations (e.g., they speed-up information search of a fact checker collaborating with a ML model, reduce cognitive load, etc.). Such methods are developed by considering how people explain between each other (extensively studied by social sciences) and conducting application-grounded human-subject evaluations that are common in HCI.  

Methods and examples in this course will heavily focus on **Natural Language Processing (NLP)** and **Computer Vision (specifically images)**. This course will _not_ cover global methods that analyze models' average behavior and internals. 

## Calendar

Calendar is **tentative and subject to change**.
More details will be added as the semester continues.

<table>
  <thead>
  <tr>
    <th>Week</th>
    <th>Date</th>
    <th width="20%">Theme</th>
    <th width="30%">Contents</th>
    <th width="13%">Work due</th>
  </tr>
  </thead>
  <tbody>
  {% for week in site.data.calendar %}
    {% for day in week.days %}
      <tr>
        {% if forloop.index == 1 %}
        <td rowspan="{{week.size}}">{{week.week}}</td>
        {% endif %}
        <td>{{day.date}}</td>
        <td>{{day.theme}}</td>
        <td class="cal-content">
          {{day.topics}}
          {% if day.slides %}
            <a href="{{day.slides}}" class="cal-content-link">[slides]</a>
          {% endif %}
          {% if day.readings %}
            <a href="{{day.readings}}" class="cal-content-link">[readings]</a>
          {% endif %}
        </td>
        <td class="cal-content">{{day.due}}</td>
      </tr>
    {% endfor %}
  {% endfor %}
  </tbody>
</table>


## Resources

* **MS Teams.** Course communication will be via MS Teams.  You should sign into using your uNID and join the "team" for the class using an invite link which has been sent to you via email. MS Teams will be used for sharing discussion points and questions prior to in-class paper discussions.

* **Google Drive.** Course materials, including lectures, reading lists, etc., are in a
  [Google Drive folder](https://drive.google.com/drive/folders/13i2Sor2M7it72aGlMd87Iejw6fzqsBxI?usp=sharing) which has been shared with all students. You will also use Google Drive for submitting your reviews and project proposals.

## Assignments/Grading

There will be three components to course grades.


* **[Project](assignments/project/) (50%).**
    * Form a project team and submit project team information (5%).
    * Submit a project proposal: 1-2 paragraphs identifying the focus area of the project (10%).
    * Submit intermediate status report (20%):
      * The progress you have made towards your goal. (This cannot be just "We collected data".) (50%)
      * Details of your plan for rest of the semester (30%)
      * Pointers to literature (20%)
    * Submit a project report (35%): A document no longer than 8 pages, structured like a research paper.
    * Presentation (30%): Instead of the final exam, we will have a presentation of the projects in the class. More details as we go along.
* **[Paper readings and discussion](assignments/paper_discussions/) (30%).**
    * 20%: Submit discussion questions before class and participate regularly during class. Note that not every question gives you points (e.g., a question cannot be just "What's X?" where X is explicitly described in the paper.)
    * 10%: Lead at least one discussion.
* **[Paper review](assignments/review/)** (20%) Review ACL/EMNLP reviewing guidelines and write a review for a research paper in explainable AI.

## Policies

<!-- * **Late policy.** Students will have 4 late days that may be used for HW assignments at any point during the semseter. Late days may not be used for project benchmarks. After all late days have been used, no credit will be given for homework submitted late. -->

### Late Policy

 All submissions should be made by the deadline. We will use the timestamp on Canvas as the submission time. Submissions will be accepted up to 24 hours after deadline, but will be assessed a 10% penalty. That is, if your submission is late and scores 90, then your actual grade will be 81=90-9. 
 
 Submissions will not be accepted 24 hours after the deadline. 
 
 We will be strict about this policy: If the deadline is midnight and you submit the assignment at 12:01 AM, you will face the 10% penalty!

### No double dipping projects across multiple classes

You can not submit the same project to this class and another class that you may be taking at the same time. If you are doing related projects in two different classes, there may be some overlap (e.g. in code libraries, etc.), but they should not be identical. A project that is found to be double-submitted will receive zero credit. If you have questions about this policy, please contact the instructor.

### Diversity

It is our intent that students from all diverse backgrounds and perspectives be well-served by this course, that students' learning needs be addressed both in and out of class, and that the diversity that the students bring to this class be viewed as a resource, strength and benefit. It is our intent to present materials and activities that are respectful of diversity: gender identity sexuality, disability, age, socioeconomic status, ethnicity, race, nationality, religion, and culture. Your suggestions are encouraged and appreciated. Please let us know ways to improve the effectiveness of the course for you personally, or for other students or student groups.

## School of Computing Policies and Guidelines  

The class operates under the School of Computing's [policies and guidelines](https://handbook.cs.utah.edu/2019-2020/Academics/policies.php). Among other things, linked page provides information about the [academic misconduct policy](https://www.cs.utah.edu/docs/misc/cheating_policy.pdf) that we will adhere to. 

Also see the [College of Engineering guidelines](https://www.coe.utah.edu/students/current/semester-guidelines/) for information about appeals procedures, withdrawal procedures, and adding and repeating courses.

### University Drop/Withdrawal Policy 

Students may drop a course within the first two weeks of a given semester without any penalties.

Students may officially withdraw (W) from a class or all classes after the drop deadline through the midpoint of a course. A “W” grade is recorded on the transcript and appropriate tuition/fees are assessed. The grade “W” is not used in calculating the student’s GPA.

For deadlines to withdraw from full-term, first, and second session classes, see the U's [Academic Calendar](https://registrar.utah.edu/academic-calendars/index.php).

### University Plagiarism and Cheating Policy

It is assumed that all work submitted to your instructor is your own work. When you have used the ideas of others, you must properly indicate that you have done so.

Plagiarism and cheating are serious offenses and may be punished by failure on an individual assignment, and/or failure in the course. Academic misconduct, according to the University of Utah Student Code,

>...Includes, but is not limited to, cheating, misrepresenting one’s work, inappropriately
> collaborating, plagiarism, and fabrication or falsification of information...It also includes
> facilitating academic misconduct by intentionally helping or attempting to help another to commit
> an act of academic misconduct.

For details on plagiarism and other important course conduct issues, see the U's [Code of Student Rights and Responsibilities.](http://regulations.utah.edu/academics/6-400.php).

### Course Materials Copyright

**The Content is made available only for your personal, noncommercial educational, and scholarly use.** You may not use the Content for any other purpose, or distribute, post or make the Content available to others unless you obtain any required permission from the copyright holder. Some Content may be provided via streaming or other means that restrict copying; you may not circumvent those restrictions. You may not alter or remove any copyright or other proprietary notices included in the Content.
 
Please see the [Code of Student Rights and Responsibilities](https://regulations.utah.edu/academics/6-400.php), Section III.A.5 regarding the [use and distribution of class Content](https://regulations.utah.edu/academics/6-400.php) and materials. Section III.A.5. prohibits the following:
Sale or distribution of information representing the work product of a faculty member to a commercial entity for financial gain without the express written permission of the faculty member responsible for the course. (“Work product” means original works of authorship that have been fixed in a tangible medium and any works based upon and derived from the original work of authorship.)

### University Safety Statement 

The University of Utah values the safety of all campus community members. You will receive important emergency alerts and safety messages regarding campus safety via text message.

For more safety information and to view available training resources, including helpful videos, visit safeu.utah.edu.

To report suspicious activity or to request a courtesy escort, contact:

* **[Campus Police & Department of Public Safety](dps.utah.edu)**
* 801-585-COPS (801-585-2677)
* 1735 E. S. Campus Dr., Salt Lake City, UT 84112

### Wellness

Take care of yourself! As a student, you may experience a range of challenges that can interfere with learning, such as strained relationships, increased anxiety, substance use, feeling down, difficulty concentrating and/or lack of motivation. All of us benefit from support during times of struggle. There are many helpful resources available on campus and an important part of having a healthy life is learning how to ask for help. Asking for support sooner rather than later is almost always helpful. 

You can learn more about confidential mental health services available on campus:

* **[Center for Student Wellness](https://www.wellness.utah.edu)**
  * 801-581-7776
  * 2100 Eccles Student Life Center, 1836 Student Life Way, Salt Lake City, UT 84112
* **[Women's Resource Center](https://womenscenter.utah.edu/)**
  * 801-581-8030
  * 411 Union Building, 200 S. Central Campus Dr., Salt Lake City, UT 84112 
  
Crisis services are available from the [National Suicide Prevention Lifeline network](https://988lifeline.org/) 24/7 by phone at **988** ([more details here](https://healthcare.utah.edu/hmhi/programs/crisis-diversion/)).


### Addressing Sexual Misconduct

Title IX makes it clear that violence and harassment based on sex and gender (which includes sexual orientation and gender identity/expression) is a civil rights offense subject to the same kinds of accountability and the same kinds of support applied to offenses against other protected categories such as race, national origin, color, religion, age, status as a person with a disability, veteran's status or genetic information.

If you or someone you know has been harassed or assaulted, you are encouraged to report it to university officials: 

* **[Title IX Coordinator in the Office of Equal Opportunity and Affirmative Action](https://oeo.utah.edu/)**
  * 801-581-8365
  * 135 Park Building, 201 Presidents' Cir., Salt Lake City, UT 84112

* **[Office of the Dean of Students](https://deanofstudents.utah.edu/)**
  * 801-581-7066
  * 270 Union Building, 200 S. Central Campus Dr., Salt Lake City, UT 84112 
 
To file a police report, contact:

* **[Campus Police & Department of Public Safety](dps.utah.edu)**
* 801-585-COPS (801-585-2677)
* 1735 E. S. Campus Dr., Salt Lake City, UT 84112

If you do not feel comfortable reporting to authorities, the U's Victim-Survivor Advocates provide **free**, **confidential**, and **trauma-informed** support services to **students**, **faculty**, and **staff** who have experienced interpersonal violence.

To **privately** explore options and resources available to you with an advocate, contact:

* **[Center for Student Wellness](wellness.utah.edu)**
  * 801-581-7776
  * 328 Student Services Building, 201 S. 1460 E., Salt Lake City, UT 84112


### The Americans with Disabilities Act

The University of Utah seeks to provide equal access to its programs, services and activities for people with disabilities. 

All written information in this course can be made available in an alternative format with prior notification to the Center for Disability & Access (CDA). CDA will work with you and the instructor to make arrangements for accommodations. Prior notice is appreciated. To read the full accommodations policy for the University of Utah, please see Section Q of the [Instruction & Evaluation regulations](http://regulations.utah.edu/academics/6-100.php).

If you will need accommodations in this class, or for more information about what support they provide, contact:

* **[Center for Disability & Access](disability.utah.edu)**
  * 801-581-5020
  * 162 Union Building, 200 S. Central Campus Dr., Salt Lake City, UT 84112
  


