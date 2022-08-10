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
  
## Summary

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
  [Google Drive folder](https://drive.google.com/drive/u/1/folders/15eLW-7qMSF58FLYaHTm91MWd80fykGps)
  which has been shared with all students. You will also use Google Drive for submitting your
  ethics reviews and project proposals.

## Assignments/Grading

There will be three components to course grades.

* **[Paper readings and discussion](assignments/paper_discussions/) (40%).**
    * 30%: Submit discussion questions before class and participate regularly during class.
    * 10%: Lead at least one discussion.
* **[Ethics review](assignments/ethics_review/) (30%).** Review ethics reviewing guidelines and write an ethics review
  for a research paper.
* **Project proposal (30%).** Write a proposal for a research project in ethical AI.
  * 2%: Pre-proposal: 1-2 paragraphs identifying the focus area of the project and team members.
  * 20%: Proposal.
  * 8%: Class presentation.
  * **Bonus (15%):** Implement the proposed project.

<!-- * Pre-proposal: A 1-2 paragraph document describing the focus area of the project and defining team members (Due 1/23) -->
<!-- * Proposal: (7.5%) A 2-3 page document (ACL format) containing a literature review, concrete problem definition, identification of baseline models, and ideas for final models. Sections should include Introduction, Related Work, Data, Baseline, Proposed Approach. Baselines should be clearly defined but do not need to be implemented yet (Due 2/25) -->
<!-- * Midterm Presentations: (7.5%) An in-class presentation of project and current progress. Presentation should include problem definition, baseline models and results, and description of proposed models (3/19-3/24) -->
<!-- * Final Report and Presentations: (15%) In-class presentations of the project will be held during the final week of class. A final project report will be due the following week. The final report should be formated as a standard research paper with appropriate sections (ACL format, 8 pages) (Presentations 4/28-4/30; Report due 5/8) -->

## Policies

<!-- * **Late policy.** Students will have 4 late days that may be used for HW assignments at any point during the semseter. Late days may not be used for project benchmarks. After all late days have been used, no credit will be given for homework submitted late. -->

### Late Policy

 All submissions should be made by the deadline. We will use the timestamp on Canvas as the submission time. Submissions will be accepted up to 24 hours after deadline, but will be assessed a 10% penalty. That is, if your submission is late and scores 90, then your actual grade will be 81=90-9. 
 
 Submissions will not be accepted 24 hours after the deadline. 
 
 We will be strict about this policy: If the deadline is midnight and you submit the assignment at 12:01 AM, you will face the 10% penalty!

### No double dipping projects across multiple classes

You can not submit the same project to this class and another class that you may be taking at the same time. If you are doing related projects in two different classes, there may be some overlap (e.g. in code libraries, etc.), but they should not be identical. A project that is found to be double-submitted will receive zero credit. If you have questions about this policy, please contact the instructor.

### School of Computing Policies and Guidelines  

The class operates under the School of Computing's [policies and guidelines](https://handbook.cs.utah.edu/2019-2020/Academics/policies.php). Among other things, linked page provides information about the [academic misconduct policy](https://www.cs.utah.edu/docs/misc/cheating_policy.pdf) that we will adhere to. 

Also see the [College of Engineering guidelines](https://www.coe.utah.edu/students/current/semester-guidelines/) for information about appeals procedures, withdrawal procedures, and adding and repeating courses.

### Collaboration and Cheating

Collaboration is encouraged; cheating will not be tolerated. 

*<center><u>Honor code for this class</u></center>*
 
> You are encouraged to discuss class materials with your peers. If you want you
> can form study groups because discussions help understanding. You are also
> welcome to discuss assignments.
> 
> However, you must write your own solutions, proofs, and code and submit your
> own solution. Do not copy or ask for assignments from other students or the
> internet. Do not let someone else copy your submissions either.

If you are caught cheating once, you *will* receive a failing grade for that
submission. If you are caught cheating again, you will fail the class.
 
For projects, you are free to discuss the project with your classmates, but your
work should be your own.
 
For both assignments and the project, you should cite all sources that you refer
to. This includes personal communication, books, papers, websites, etc. Doing so
reflects academic integrity.

### The Americans with Disabilities Act

The University of Utah seeks to provide equal access to its programs, services and activities for people with disabilities. If you will need accommodations in the class, reasonable prior notice needs to be given to the [Center for Disability and Access](http://disability.utah.edu). CDA will work with you and the instructor to make arrangements for accommodations. Accommodations cannot be given without paperwork from this office.

### University Safety Statement 

The University of Utah values the safety of all campus community members. To report suspicious activity or to request a courtesy escort, call campus police at **801-585-COPS** or **801-585-2677**. You will receive important emergency alerts and safety messages regarding campus safety via text message. For more information regarding safety and to view available training resources, including helpful videos, visit [safeu.utah.edu](https://safeu.utah.edu).

### Addressing Sexual Misconduct

Title IX makes it clear that violence and harassment based on sex and gender (which includes sexual orientation and gender identity/expression) is a civil rights offense subject to the same kinds of accountability and the same kinds of support applied to offenses against other protected categories such as race, national origin, color, religion, age, status as a person with a disability, veteran's status or genetic information.

If you, or someone you know, are harassed or assaulted, you are encouraged to report it to the Title IX Coordinator in the Office of Equal Opportunity and Affirmative Action, 135 Park Building, **801-581-8365**, or the Office of the Dean of Students, 270 Union Building, **801-581-7066**. For support and confidential consultation, contact the Center for Student Wellness, 426 SSB, **801-581-7776**. To report to the police, contact the Department of Public Safety, **801-585-COPS** or **801-585-2677**.

### Wellness

Take care of yourself! As a student, you may experience a range of challenges that can interfere with learning, such as strained relationships, increased anxiety, substance use, feeling down, difficulty concentrating and/or lack of motivation. All of us benefit from support during times of struggle. There are many helpful resources available on campus and an important part of having a healthy life is learning how to ask for help. Asking for support sooner rather than later is almost always helpful. 

You can learn more about confidential mental health services available on campus:

* [Center for Student Wellness](https://www.wellness.utah.edu) 
* [College of Engineering counseling services](https://www.coe.utah.edu/students/current/counseling/)

Crisis services are available from the [National Suicide Prevention Lifeline network](https://988lifeline.org/) 24/7 by phone at **988** ([more details here](https://healthcare.utah.edu/hmhi/programs/crisis-diversion/)).

### Diversity

It is our intent that students from all diverse backgrounds and perspectives be well-served by this course, that students' learning needs be addressed both in and out of class, and that the diversity that the students bring to this class be viewed as a resource, strength and benefit. It is our intent to present materials and activities that are respectful of diversity: gender identity sexuality, disability, age, socioeconomic status, ethnicity, race, nationality, religion, and culture. Your suggestions are encouraged and appreciated. Please let us know ways to improve the effectiveness of the course for you personally, or for other students or student groups.
