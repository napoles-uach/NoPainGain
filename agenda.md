---
title: Hackathon agenda 🗓️
menu_title: Agenda
menu_icon: clock
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

## Schedule
{% if event_status != "over" %}
The anticipated schedule is as follows, with all times listed in Eastern Time (ET). Be sure to add the events to your calendar using the [Gather links](https://app.gather.town/events/nHv-tpANR6a7kCsPCgqJ).
{% else %}
The schedule for the event was as follows, with all times listed in Eastern Time (ET):
{% endif %}

## Feb 22 - Mar 27

Brainstorm, build, team up.

1. Add the events to your calendar using the ["Add to Calendar" link from the Gather Town event page](https://app.gather.town/events/nHv-tpANR6a7kCsPCgqJ) (for Outlook calendars, you will need to login to Outlook online)
2. Enter your email into [this form](https://forms.gle/1AKnQrdgCPk2Yts96) or send an email to [sterling.baird@utoronto.ca](mailto:sterling.baird@utoronto.ca) with subject line "Slack guest invite request" so that we can manually add you as a guest to the `#ac-bo-hackathon` slack channel, or if your workspace has Slack Pro, join the [Slack channel directly](https://join.slack.com/share/enQtNjg2ODE3OTIwMDcwNC1iNzhiOGYxNzJiN2JkMWIxN2VkMDc4ODNlM2RjMDQ4ZTYyNTI0ZTdhZTZiMDgwMzE3ZTdjZjQ1ZmUxN2E4MjMz). These are the preferred options over starting a Slack Pro free trial, since you will lose access to the channel once the trial has expired. The free trial route (e.g., in a personal workspace) is a fallback if you need immediate access to the slack channel.
3. Brainstorm project ideas and form teams
   1. Browse [the existing project proposals](_/../projects.md)
   2. If you'd like to solicit team members or get feedback, post your project idea in the slack channel with the `#team` hashtag to make it easier to search for these posts. You may also consider using social media
   3. If you would like to join a team, use the slack channel to express your interest and describe your background, again using the `#team` hashtag
   4. Submit your [project proposal](_/../submission.md) (multiple allowed)
4. For coding-related projects, [complete the orientation modules](_/../resources.md)

<!-- 4. If you plan to join an existing project, use the GitHub Classroom link corresponding to the project topic and select the appropriate team on the GitHub Classroom interface (see [submission](_/../submission.md)). Reach out to [sterling.baird@utoronto.ca](mailto:sterling.baird@utoronto.ca) if you have trouble getting added to your team -->

### Day 1: Mar 27

A map of the foyer in the Gather Town space is shown below. You will enter the foyer from the south, and you can access the various rooms by walking through the corresponding doorways.

![gather town foyer](assets/gather-town-foyer.png)

| Time  | Activity |
|-------|----------|
| 09:00 | Welcome (Talk Room) |
| 09:05 | Speakers (Talk Room): <br> - Dr. Taylor Sparks (University of Utah) \| *Discovering materials twice as fast at a fraction of the cost through Bayesian optimization* <br> - Dr. Martin Fitzner (Merck KGaA) \| *Industrial view on BO – a perfect match for the low- to no-data regime* <br> - Dr. Max Balandat (Meta Adaptive Experimentation) \| *Bayesian Optimization for Sustainable Concrete* |
| 10:00 | Orientation (Talk Room) |
| 10:10 | Breakout (Breakout Rooms A-G) / Team-building (Talk Room) |
| 13:00 | End of Day 1 |

### Day 2: Mar 28

| Time  | Activity |
|-------|----------|
| 09:00 | Welcome |
| 09:10 | Breakout (Breakout Rooms A-G) |
| 12:00 | Project showcase and judging (Poster Rooms A-B) |
| 12:55 | Closing remarks and takeaways |
| 13:00 | End of Day 2 |

### Mar 29

[Submissions](_/../submission.md) due by {{ site.submissions_due }}.

Prizes to be announced March 29 at 1:00 PM Eastern Time (ET).

### Post-hackathon

Preparation of scholarly article.[<sup>(?)</sup>][faq]{:title="What is required for me to participate in the scholarly article?"}


[faq]: {{ site.baseurl }}{% link faq.md %}

<!-- {:.agenda} -->

<!-- {:.agenda} -->
<!-- Time (BST)    | Activity | Where to go
------------- | -------- | -----------
09:15 – 09:30 | Zoom meeting opens for informal networking | Zoom main room
09:30 – 10:00 | **Welcome talk**<br>Speaker name | Zoom main room
10:00 – 11:55 | **Breakout groups**<br>Recap and continue working on projects | Zoom breakout rooms
12:00 – 12:30 | **Yoga**<br>Take some time away from your keyboard | Zoom main room
12:30 – 13:30 | Lunch break |
13:30 – 16:30 | **Breakout groups**<br>Continue working on projects | Zoom breakout rooms
16:30 – 17:00 | **End of day tidy-up**<br>Write up<br>Commit your changes to GitHub<br>Tidy Group Workspace | Zoom breakout rooms
17:00 – 17:25 | **Group updates**<br>90 seconds per group<br>Zero or one slide 😊<br>How things are going; what problems you have faced | Zoom main room
17:25 – 17:30 | **Close of day** | Zoom main room -->


<!-- ## Day 2: Mar 28

Live session to announce prizes. -->
