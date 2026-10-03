---
title: team
layout: default
permalink: /team
excerpt: "Team"
title: "Team"
---

{% assign people_sorted = site.team | sort: 'joined'  %}
{% assign role_array = "pi|researcher|postdoc|gradstudent|intern|visiting|others|alumni" | split: "|" %}

<h2>Current members</h2>
<div style="align:left;">
{% for role in role_array %}
{% assign people_in_role = people_sorted | where: 'position', role %}

{% if role != 'alumni' %}
{% for profile in people_sorted %}
{% if profile.position contains role %}

<div class="list-item-people">
<hr>
<p class="list-post-title">
{% if profile.avatar %}
<a href="{{ site.url }}{{ site.baseurl }}{{ profile.url }}"><img class="profile-thumbnail"  src="{{ site.url }}{{site.baseurl}}/assets/images/member/{{profile.avatar}}"></a>
{% else %}
<a href="{{ site.url }}{{ site.baseurl }}{{ profile.url }}"><img class="profile-thumbnail"  src="{{ site.url }}{{site.baseurl}}/assets/images/member/bio.jpg"></a>
{% endif %}
</p>
<p>
<a class="name" href="{{ site.url }}{{ site.baseurl }}{{ profile.url }}">{{ profile.name }}</a>  
<br>
<span>
{% if profile.position=='pi' %}
{% assign pos = 'PI' %}
{% elsif profile.position=='researcher' %}
{% assign pos = 'Research Faculty' %}
{% elsif profile.position=='postdoc' %}
{% assign pos = 'Postdoc' %}
{% elsif profile.position=='gradstudent' %}
{% assign pos = 'Graduate student' %}
{% elsif profile.position=='visiting' %}
{% assign pos = 'Visiting' %}
{% elsif profile.position=='intern' %}
{% assign pos = 'Intern' %}
{% elsif profile.position=='others' %}
{% assign pos = 'Others' %}
{% endif %}
{{ pos }} since {{ profile.joined }}
</span>  
</p>
<p style="text-align:left;">
{% if profile.email %}
<a href="mailto:{{ profile.email }}"><i class="fa fa-envelope fa-align-left fa-lg"></i></a> 
{% endif %}
{% if profile.scholar  %}
<a href="{{ profile.scholar }}"><i class="ai ai-google-scholar icon-align-left fa-lg" ></i></a>
{% endif %}
{% if profile.web %}
<a href="{{ profile.web }}"><i class="fa fa-globe fa-align-left fa-lg"></i></a> 
{% endif %}
{% if profile.github  %}
<a href="https://github.com/{{ profile.github }}"><i class="fa fa-github fa-align-left fa-lg"></i></a>
{% endif %}
{% if profile.orcid  %}
<a href="https://orcid.org/{{ profile.orcid }}"><i class="ai ai-orcid icon-align-left fa-lg" ></i></a> 
{% endif %}
{% if profile.twitter  %}
<a href="https://twitter.com/{{ profile.twitter }}"><i class="fa fa-twitter fa-align-left fa-lg"></i></a>
{% endif %}
{% if profile.linkedin  %}
<a href="https://www.linkedin.com/in/{{ profile.linkedin }}"><i class="fa fa-linkedin fa-align-left fa-lg"></i></a>
{% endif %}
</p>
</div>
{% endif %}
{% endfor %}

{% endif %}
{% endfor %}

</div>

<br>
<hr>

## Former Members of DISP


| Name                        | Role                  | Year |
| --------------------------- | --------------------- | ---- |
| Chengyu Wang                | Graduate Student      | 2017–2022 |
| Qian Huang                  | Graduate Student      | 2018–2022 |
| Minghao Hu                  | Graduate Student      | 2018–2023 |
| Steve Feller                | AWARE project manager |      |
| Leah Goldsmith              | group administrator   |      |
| Dr. Mehadi Hassan           |                       |      |
| Dr. Ruoyu Zhu               |                       |      |
| Dr. Daniel Marks            |                       |      |
| Dr. Joel Greenberg          | CAXI program leader   |      |
| Dr. Ken MacCabe             |                       |      |
| Paul Vosburgh               | instrument maker      |      |
| Dr. Kalyani Krishnamurthy   | postdoc               |      |
| Dr. Jun Niu                 | postdoc               |      |
| Dr. Sean Pang               | postdoc               |      |
| Dr. Alex Mrozack            |                       |      |
| Dr. Evan Chen               |                       |      |
| Dr. Tsung Han Tsai          |                       |      |
| Dr. Andrew Holmgren         |                       |      |
| Dr. Patrick Llull           |                       |      |
| Lauren Bange                |                       |      |
| Dr. Orges Furxhi            | postdoc               |      |
| Sally Gewalt                | Senior Staff          |      |
| Joanna Clark                | Staff                 |      |
| Dr. David Kittle            |                       |      |
| Dr. Amar Chawla             | Staff                 |      |
| Dr. Se Hoon Lim             |                       |      |
| Dr. Joonku Hahn             | postdoc               |      |
| Dr. Kerkil Choi             | postdoc               |      |
| Dr. Ashwin Wagadarikar      |                       |      |
| Dr. Cristina Fernandez      |                       |      |
| Dr. Nathan Hagen            | postdoc               |      |
| Dr. Nikos Pitisianis        | Staff                 |      |
| Dr. Andrew Portnoy          |                       |      |
| Dr. Renu John               | postdoc               |      |
| Dr. Mohan Shankar           |                       |      |
| Dr. Yangqia Wang            | postdoc               |      |
| Dr. Scott McCain            |                       |      |
| Dr. Michael Gehm            | postdoc               |      |
| Dr. Evan Cull               |                       |      |
| Dr. John Burchett           |                       |      |
| Dr. Qi Hao                  |                       |      |
| James Adelmen               |                       |      |
| John Bower                  |                       |      |
| Dr. Unnikrishnan Gopinathan |                       |      |
| David Kowalski              |                       |      |
| Dr. Santosh Narayankhedkar  |                       |      |
| Dr. Prasant Potuluri        |                       |      |
| Adam Saltzman               |                       |      |
| Harsha Setty                |                       |      |
| Dr. Alan Shang              |                       |      |
| Dr. Arnab Sinha             |                       |      |
| Mike Sullivan               |                       |      |
| Lin Wang                    |                       |      |
| Zhanglei Wang               |                       |      |
| Mingbo Xu                   |                       |      |
| Dr. Yunhui Zheng            |                       |      |
| Zhaochun Xu                 |                       |      |


<hr>

## Former Members of Arizona Camera Lab

| Name             | Role             | Joined |
| ---------------- | ---------------- | ------ |
| Greg Nero        | Graduate Student | 2020   |
| Zhipeng Dong     | Graduate Student | 2021   |
| Xiao Wang        | Graduate Student | 2021   |
| Gordon Hageman   | Graduate Student | 2022   |
| Ahmed Al Ghamdi  | Graduate Student | 2022   |
| Shengtai Zhu     | Graduate Student | 2023   |




<hr>
## Former Members of Photonic Systems Group



| Name                         | Degree | Year |
| ---------------------------- | ------ | ---- |
| Eric Abbott                  | M.Sc   |      |
| Dr. Michal Balberg           | Ph.D.  |      |
| Dr. George Barbastathis      | Ph.D.  |      |
| Dr. Scott Basinger           | Ph.D.  |      |
| Colin Byrne                  |        |      |
| Dr. Geng-Sheng (Alan) Chen   | Ph.D.  |      |
| Dr. Matt Fetterman           | Ph.D.  |      |
| Jason Gallicchio             |        |      |
| Dr. Junpeng Guo              | Ph.D.  |      |
| Dr. Kent Hill                | Ph.D.  |      |
| Dr.  Jose Jimenez            | Ph.D.  |      |
| Dr. Andrew J. (A.J.) Johnson | Ph.D.  |      |
| Dr. Hai Lin                  | Ph.D.  |      |
| Dr. Daniel Marks             | Ph.D.  |      |
| Dr. Rick Morrison            | Ph.D.  |      |
| Dr. Ken Purchase             | Ph.D.  |      |
| Andrew Rittgers              |        |      |
| Ronald Stack                 |        |      |
| Marc Talbot                  |        |      |
| Dr. Richard Tarkka           | Ph.D.  |      |
| Dr. Remy Tumbar              | Ph.D.  |      |

