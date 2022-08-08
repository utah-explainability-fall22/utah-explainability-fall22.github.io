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
T/Th 10am-11:20am, CSE2 G04
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

* Which part of the input led to assigning this answer?            
* How to change the answer to another?                           
* In plain English, why is this input assigned this label?                        
* Which training examples caused the prediction?                      

In the first part of this course, we’ll go over methods that aim to address these questions. These methods are developed by machine learning researchers, usually without involving experts in other fields and human subjects such as doctors or fact checkers. In the second part of this course, we will revisit evaluation of these methods and focus on how to develop and evaluate methods that best accomplish a specific utility of explanations (e.g., they speed-up information search of a fact checker collaborating with a ML model, reduce cognitive load, etc.). Such methods are developed by considering how people explain between each other (extensively studied by social sciences) and conducting application-grounded human-subject evaluations that are common in HCI.  

Methods and examples in this course will heavily focus on Natural Language Processing (NLP) and Computer Vision (specifically images). This course will not cover global methods that analyze models’ average behavior and internals. 

## Calendar

Calendar is tentative and subject to change.
More details will be added as the quarter continues.

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

<!-- ## Additional Resources -->
<!-- * [Extended readings list](https://docs.google.com/document/d/1GxKMCP-A4gypu3VsOqKeefIwqSACBHvcFl7pVcaVPLQ/edit?usp=sharing) -->
<!-- * [Stanford Ethical and Social Issues in Natural Language Processing course](https://web.stanford.edu/class/cs384/) -->
<!-- * [University of Washington Ethics in NLP course](http://faculty.washington.edu/ebender/2019_575/) -->
<!-- * [University of Washington Computer Ethics course](https://courses.cs.washington.edu/courses/cse492e/20sp/) -->
<!-- * [ACL Ethics resources](https://aclweb.org/aclwiki/Ethics_in_NLP) -->
<!-- * [Embedded EthiCS at Harvard](https://embeddedethics.seas.harvard.edu/) -->

## Resources

* **Mattermost.** Course communication will be via Mattermost, an open-source communications platform similar to IRC
  for which the Allen School has an [internally-hosted instance](https://mattermost.cs.washington.edu).
  You should sign into using your CSE NetID and join the "team" for the class using an invite link
  which has been sent to you via email. Mattermost will be used for sharing discussion points and
  questions prior to in-class paper discussions.

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

* **Academic honesty.** Homework assignments are to be completed individually. Verbal collaboration on homework assignments is acceptable, as well as re-implementation of relevant algorithms from research papers, but everything you turn in must be your own work, and you must note the names of anyone you collaborated with on each problem and cite resources that you used to learn about the problem. The project proposal is to be completed by a team. Suspected violations of academic integrity rules will be handled in accordance with [UW guidelines](https://www.washington.edu/cssc/for-students/overview-of-the-student-conduct-process/) on academic misconduct.

* **Accommodations.** If you have a disability and have an accommodations letter from the Disability Resources office, I encourage you to discuss your accommodations and needs with me as early in the semester as possible. I will work with you to ensure that accommodations are provided as appropriate. If you suspect that you may have a disability and would benefit from accommodations but are not yet registered with the office of Disability Resources for Students, I encourage you to apply [here](https://denali.accessiblelearning.com/Washington/ApplicationStudent.aspx).

## Note to Students

Take care of yourself! As a student, you may experience a range of challenges that can interfere with learning, such as strained relationships, increased anxiety, substance use, feeling down, difficulty concentrating and/or lack of motivation. All of us benefit from support during times of struggle. There are many helpful resources available on campus and an important part of having a healthy life is learning how to ask for help. Asking for support sooner rather than later is almost always helpful. UW services are available, and treatment does work. You can learn more about confidential mental health services available on campus [here](https://www.washington.edu/counseling/). Crisis services are available from the counseling center 24/7 by phone at 1 (866) 743-7732 ([more details here](https://www.washington.edu/counseling/services/crisis/)).

## COVID-19 Safety

In light of the COVID-19 pandemic and recent surge in cases due to the Omicron variant, and in accordance with [UW guidelines](https://www.washington.edu/coronavirus/winter2022/), we are implementing the following policies to ensure the safety of our students and instructors to the maximum extent possible:

* **Remote access.** If you are sick or have potentially been exposed to COVID-19, **stay home**! While we encourage everyone to attend class in-person when they are well, there will always be a Zoom meeting for the class and there is no penalty for attending remotely. Office hours are also available both in-person and over Zoom (by appointment).

* **Masking.** When in public, indoor spaces occupied by other people, **you must wear a mask**. This includes class sections and office hours. See more about UW's masking requirements [here](https://www.ehs.washington.edu/covid-19-prevention-and-response/face-covering-requirements). The instructors will abide by the same masking policy.

  For the purposes of this policy, a face covering must fit snugly against the sides of the face and completely cover the nose and mouth. Bandanas and gaiters are not considered face coverings under this policy. Students who do not wear a face mask will be asked to leave the classroom. Repeated failure to wear a face covering may result in being referred to the Student Conduct Office for possible disciplinary action.

  UW has approved a hydration exemption which allows students and instructors to briefly move aside their mask if they are drinking water even in class. This exemption is meant be used only for a brief moment to hydrate, and does not allow talking with one's mask off or having one's mask removed for a prolonged period of time. This exemption does not allow for eating food in classes.
  
* **Social distancing.**  Currently, UW does not require social distancing in the classroom or office hours for students who are vaccinated and wearing a mask; it can also make it difficult to navigate and interact in such spaces. We do not mandate social distancing, but ask that if another student asks you to maintain distance from them, that you respect their request.

* **What if you get sick?** See [this FAQ](https://www.washington.edu/coronavirus/faq/) for what to do.

* **What if we get sick?** We will reschedule class, hold it remotely, or bring in a substitute lecturer/facilitator if necessary to prevent exposing students. We will try to give notice as far in advance as possible if an in-person event is moving to be held remotely, but please check your email beforehand to be sure you don't miss anything.
