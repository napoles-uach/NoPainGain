---
title: Frequently Asked Questions
menu_title: FAQ
menu_icon: question-circle
---

## What is Bayesian optimization, and why is it important for the physical sciences?

Bayesian optimization is a key technique in chemistry and materials science, particularly useful for tackling complex experiments that are time-consuming and costly. It uses a smart model, often based on Gaussian Processes, to predict where to look next in an experiment to find the best results with minimal trials. This method is especially handy when dealing with experiments that don't have straightforward outcomes or involve a lot of variables, which is often the case in these fields. It's like having a smart assistant that tells you the most promising experiments to run next, helping you save time and resources. Moreover, Bayesian optimization is good at dealing with uncertain results through its smart handling of the exploration-exploitation trade-off. This approach helps speed up the discovery of new materials and chemical processes by making the experimental process more efficient and informed.

## Am I eligible to participate in the hackathon?

Yes! The hackathon is open to everyone, regardless of background or experience. We encourage participants from all career stages, including students, researchers, and professionals, to join us. For code-based projects, we recommend at least beginner Python programming experience[<sup>(?)</sup>][faq]{:title="Do I need to use Python, or can I use other languages?"} and basic familiarity with git and GitHub. Prior to the hackathon, we also recommend that participants study the basic concepts behind Bayesian optimization. For those looking to learn or refresh their knowledge on these topics, please study the items provided in the [resources page](_/../resources.md).

## Are there specific packages I should use?

This is a BYOP ("bring-your-own-package") event 😉. We have some recommendations for newcomers, but we hope to see a diverse set of solutions applied to the benchmark tasks. Likewise, multiple teams using the same package is not a problem, since solutions can remain private during the course of the hackathon.

## Do I need to use Python, or can I use other languages?

We recommend using Python, as it is the most common language for scientific computing and has a wide range of libraries for Bayesian optimization. However, you are welcome to use other languages if you prefer.
<!-- To be considered for the prizes, your implementation must be based in Python. If you choose a language other than Python, your project can still be highlighted on the projects page and elsewhere. -->

## Does it have to be Bayesian optimization, or are other algorithms allowed?

There is certainly a focus on Bayesian optimization, but you are welcome to use other algorithms. It would be best if there's some kind of adaptive design component to it, though this isn't a strict requirement. If you're unsure, feel free to reach out to the organizers.

## Is the hackathon a competition?

Yes, in some sense. Rather than collaborating on a single problem together, you will work either solo or in small teams to accomplish one of several tasks: applying a Bayesian optimization algorithm to one of the provided benchmark tasks, designing new optimization benchmarks, creating concept-focused instructional tutorials, proposing real-world chemistry and materials science optimization tasks, or a general topic project. Submissions will be reviewed by a team of judges[<sup>(?)</sup>][faq]{:title="What is expected from me if I act as a judge?"}, and top-ranked projects will receive prizes sponsored by [Matterhorn Studio](https://matterhorn.studio/).

## Do I need to have a team to participate?

No, you are allowed to participate as an individual. However, we encourage you to form a team with other participants to work on a project together. This will allow you to share ideas and learn from others! It is up to you to identify and form a team, and you can do so at any time leading up to the hackathon.

## What is required for me to participate in the scholarly article?

We would love to have you contribute to the manuscript! Depending on the level of involvement, you will be offered the opportunity to co-author or be acknowledged in the manuscript. The following are the criteria for co-authorship, which will be evaluated at the discretion of the organizing team:

- **Participation in the hackathon**: You must have participated in the hackathon to be eligible to contribute to the scholarly article. This is indicated in part by commit history, pull requests, and issues on the team's GitHub repository, as well as other public evidence of participation.
- **Complete project submission**: You or your team must have submitted a complete project. This includes a complete implementation of a Bayesian optimization algorithm, a new benchmark task, an instructional tutorial, a real-world optimization task proposal, or a general submission based on the provided templates. Additionally, this project must be made publicly available on GitHub and [licensed appropriately](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/licensing-a-repository) (e.g., MIT License).
- **Completion of a CRediT form**: You must complete a CRediT form to be eligible for co-authorship. Additionally, you will need to acknowledge that your submitted work belongs to you, with the appropriate references and acknowledgements made. This form will be sent to you after the hackathon.

## Can I participate in multiple projects?

Yes, you may participate in multiple projects. For example, one may wish to apply a particular algorithm to a benchmark *and* create a concept-focused instructional tutorial to accompany it. Each of these would be considered a separate project with its own template. However, we encourage participants to be realistic about the limited time available during the hackathon as well as communicate this to other team members if participating in multiple projects.

## Does my GitHub repository need to be public?

During the course of the hackathon, your repository can remain private. However, to be considered for the prizes and to contribute to the scholarly article, your repository must be made public. This helps ensure that the work is accessible to the community and can be reviewed by the judges[<sup>(?)</sup>][faq]{:title="What is expected from me if I act as a judge?"} during the [judging and showcase section](_/../agenda.md). You are also welcome to make your repository public at any time leading up to or during the hackathon.

## What is expected from me if I act as a judge?

If you are interested in acting as a judge, please indicate so in the corresponding question when you [register](_/../registration.md). If you are selected as a judge, you are expected to attend the [project showcase and judging session](_/../agenda.md) on {{ site.event_close_date }}. Prior to this session, you will be provided with a [Gavel](https://anishathalye.com/gavel-an-expo-judging-system/) link which you will use to evaluate projects using the method of pairwise comparisons. You are welcome to spend as little or as much time as you'd like on each project, and you are not required or expected to review all projects. However, you should review at least two projects. If you are a participant in the hackathon, we ask that you use the "skip" button in the Gavel app if your own project is sent to you for evaluation.

## How do I prepare for the project showcase?

This can either be a poster image ([Better Poster generation 2](https://www.youtube.com/watch?v=SYk29tnxASs) format encouraged), a link to a video, or an embedded website. One of these objects will be placed into an interactive "poster" object for your project. The image or links must be supplied to the organizers 15 min prior to the showcase (see [agenda](_/../agenda.md)). The project showcase happens at the end of the second day of the hackathon where peers and judges will move around the virtual event space and browse projects in Poster Rooms A and B. Final submissions are due the next day, which involves a 2-minute video submission.

<!-- Better poster? -->

[faq]: {{ site.baseurl }}{% link faq.md %}
