---
layout: page
title: Measures & Metrics #a project title as it will appear on the website
img: /assets/img/m&m.png #thumbnail logo for the project overview
img2: /assets/img/m&m.png #a second banner for the second half of the page, contents of this banner should be related to the work stream
worktype: bg-success #select one of the colors (researchandmethods: bg-success, standardizationandregulation: bg-primary, softwaretooling: bg-info)
lifecyclesteps: 1 2 3 4 #select one or more of the numbers for the life cycle steps 1 2 3 4
description: Collection of SOTA ML quality assurance methods like bias, generalizations, robustness, uncertainty, and so forth about use cases and regulatory topics. #a very short description of
projecttag: measuresandmetrics #use this tag as the name for your project .bib file
contact: Luis Oala, luis@aiaudit.org #Firstname Lastname, email of the general contact
coordinates: Weekly, Thursday, 2:00 PM, CET #Interval and day, HH:MM PM, time zone
zoomroom: #link to the zoom room that is used for meetings
groupchat: #invite/access request link to the group chat
mailinglist: #email of the mailing list that people can subscribe to for this workstream
github: #provide a github link for the project if it exists
whiteboard: #link to the miro whiteboard that is used for the work stream
drive: #link to the shared drive of the work stream (for documents etc)
importance: 2
---
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ page.img | relative_url }}" alt="" title="" width="{{ site.max_width }}" height="100"/>
    </div>
</div>
<br/>

# Scope
Since 2020, the Measures & Metrics workstream has researched regulatory aspects inside of Machine Learning for Health. We study a collection of SOTA ML quality assurance methods like bias, generalizations, robustness, uncertainty, and so forth about use cases and regulatory topics. Our expectation is finish the project until the end of 2022.

Today, our multidisciplinary team has students and professionals from different companies, laboratories, universities worldwide focusing on creating regulatory documents and providing better solutions to society.

We already developed a paper about Machine Learning for Health Audit in this workstream (see in publications). Our objective is to move to easy to maintain and use web resources.

#### Aims
Develop better regulations by publications, international standards about measures, and metrics inside Machine Learning for Health.

#### Outputs
<div class="publications">
  {% bibliography -f {{ page.projecttag }} -q @*[projectoutput=true]* %}
</div>

---
# Collaboration resources
You are welcome to inquire about the work stream and opporunities for collaboration directly with the work stream team.
* **General contact** {{ page.contact }}

#### Meetings
Regular meetings for this work stream take place at the below coordinates.
* **Meetings** {{ page.coordinates }}
* **Zoom room** [Click here to join meeting]({{ page.zoomroom }})

#### Communication
You can subsbscribe to the work stream mailing list to receive updates and join the asynchronous group chat.
* **Group chat** {{ page.groupchat }}
* **Mailing list** {{ page.mailinglist }}

#### Tools
We use different tools in our remote work. They include shared documents, github projects for code as well as task tracking and a collaborative whiteboard for ideation. You can request access via the below links.
* **Shared drive** {{ page.drive }}
* **Github project** {{ page.github }}
* **Collaborative whiteboard** {{ page.whiteboard }}

You can find more information about the way we usually carry out our work remotely in teams [here](https://aiaudit.org/join).

---

# Milestones
<div class="news">
  {% if site.news  %}
    <div class="table-responsive">
      <table class="table table-sm table-borderless">
      {% assign news = site.news | reverse %}
      {% for item in news limit: site.news_limit %}
        {% if item.projecttag == page.projecttag %}
            <tr>
            <th scope="row">{{ item.date | date: "%b %-d, %Y" }}</th>
            <td>
                {% if item.inline %}
                {{ item.content | remove: '<p>' | remove: '</p>' | emojify }}
                {% else %}
                <a class="news-title" href="{{ item.url | relative_url }}">{{ item.title }}</a>
                {% endif %}
            </td>
            </tr>
        {% endif %}
      {% endfor %}
      </table>
    </div>
  {% else %}

  {% endif %}
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ page.img | relative_url }}" alt="" title="" width="{{ site.max_width }}" height="100"/>
    </div>
</div>
<br/>

# Important reference material
This is a list of related work and resources relevant for this work stream. It comprises resources the work stream contributors consider good practice.

<div class="publications">
  {% bibliography -f {{ page.projecttag }} %}
</div>
