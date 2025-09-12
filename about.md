---
title: About the Hackathon
menu_title: About
menu_icon: globe2
---
{% assign current_date = 'now' | date: "%Y-%m-%d" %}
{% assign event_start_date = site.event_start_date | date: "%Y-%m-%d" %}
{% assign event_close_date = site.event_close_date | date: "%Y-%m-%d" %}
{% assign registration_opens_date = site.registration_opens_date | date: "%Y-%m-%d" %}
{% assign registration_closes_date = site.registration_closes_date | date: "%Y-%m-%d" %}

{% if current_date < registration_opens_date %}
    {% assign registration_status = 'soon' %}
{% elsif current_date >= registration_opens_date and current_date <= registration_closes_date %}
    {% assign registration_status = 'open' %}
{% else %}
    {% assign registration_status = 'closed' %}
{% endif %}

{% if current_date < event_start_date %}
    {% assign event_status = 'soon' %}
{% elsif current_date >= event_start_date and current_date <= event_close_date %}
    {% assign event_status = 'now' %}
{% else %}
    {% assign event_status = 'over' %}
{% endif %}

{% if event_status != "over" %}
The AC BO Hackathon is a 2-day virtual hackathon event on {{ site.event_date }}, co-organised by the [Acceleration Consortium @ University of Toronto](https://acceleration.utoronto.ca/) and [Merck KGaA](https://www.emdgroup.com/en). The event is open to researchers at all levels who are interested in applying Bayesian optimization for accelerated discovery in chemistry and materials science.
{% else %}
The AC BO Hackathon was a 2-day virtual hackathon event hosted on {{ site.event_date }}, organised by the [Acceleration Consortium @ University of Toronto](https://acceleration.utoronto.ca/) and [Merck KGaA](https://www.emdgroup.com/en). The event included researchers at all levels who worked on projects applying Bayesian optimization for accelerated discovery in chemistry and materials science.
{% endif %}

### The organizing team

<!-- {:.lead}
To contact us about the hackathon, please contact us on Twitter or Slack. -->

<table class="team-list">
    <tr>
        <td>
            <img alt="Sterling Baird" src="https://avatars.githubusercontent.com/u/45469701?s=400&u=ab65e519709791f38a49a44fc03588058407be63&v=4">
        </td>
        <td>
            <strong>Sterling Baird</strong>
            <span class="profile-links">
                <a title="Profile &amp; contact" href="https://acceleration.utoronto.ca/researcher/sterling-baird"><i class="bi bi-person-lines-fill"></i></a>
                <!-- <a title="Website" href="https://jatonline.co.uk/"><i class="bi bi-globe2"></i></a> -->
                <a title="GitHub" href="https://github.com/sgbaird"><i class="bi bi-github"></i></a>
                <a title="Twitter" href="https://twitter.com/JGIBristol"><i class="bi bi-twitter"></i></a>
            </span>
            <br>Acceleration Consortium, University of Toronto
            <br>Director of Training and Programs
        </td>
    </tr>
    <!-- <tr>
        <td>
            <img alt="Andrew White" src="https://pbs.twimg.com/profile_images/1610864530216591361/9_HA-bt8_400x400.jpg">
        </td>
        <td>
            <strong>Andrew White</strong>
             <span class="profile-links">
                <a title="Website" href="https://thewhitelab.org/"><i class="bi bi-globe2"></i></a>
                <a title="GitHub" href="https://github.com/whitead"><i class="bi bi-github"></i></a>
                <a title="Twitter" href="https://twitter.com/andrewwhite01"><i class="bi bi-twitter"></i></a>
            </span>
            <br>University of Rochester, Vial
            <br>Professor, VP of AI
        </td>
    </tr>
    <tr>
        <td>
            <img alt="Kevin Jablonka" src="../assets/kevin.jpg">
        </td>
        <td>
            <strong>Kevin M Jablonka</strong>
            <span class="profile-links">
                <a title="Website" href="https://kjablonka.com/"><i class="bi bi-globe2"></i></a>
                <a title="GitHub" href="https://github.com/kjappelbaum"><i class="bi bi-github"></i></a>
                <a title="Twitter" href="https://twitter.com/kmjablonka"><i class="bi bi-twitter"></i></a>
            </span>
            <br>EPFL
            <br>PhD Student
        </td>
    </tr>
    <tr>
        <td>
            <img alt="KJ Schmidt" src="../assets/kj.jpeg">
        </td>
        <td>
            <strong>KJ Schmidt</strong>
            <span class="profile-links">
                <a title="Website" href="http://kjschmidt.us/"><i class="bi bi-globe2"></i></a>
                <a title="GitHub" href="https://github.com/kjschmidt913"><i class="bi bi-github"></i></a>
                <a title="Twitter" href="https://twitter.com/kj_schmidt"><i class="bi bi-twitter"></i></a>
            </span>
            <br>University of Chicago/Argonne National Lab
            <br>Research Scientist
        </td>
    </tr>
        <tr>
        <td>
            <img alt="Ari Scourtas" src="../assets/ari.JPG">
        </td>
        <td>
            <strong>Aristana Scourtas</strong>
            <span class="profile-links">
                <a title="GitHub" href="https://github.com/ascourtas"><i class="bi bi-github"></i></a>
                <a title="Twitter" href="https://twitter.com/aristana_s"><i class="bi bi-twitter"></i></a>
            </span>
            <br>University of Chicago/Argonne National Lab
            <br>Research Scientist
        </td>
    </tr> -->
</table>

### Acknowledgements

We thank Ben Blaiszik, Kevin Jablonka, and the rest of the organizing team for the [LLMs in Materials and Chemistry '23 Hackathon](https://materials-data-facility.github.io/llm-hackathon/), for which this event is heavily templated off of.
