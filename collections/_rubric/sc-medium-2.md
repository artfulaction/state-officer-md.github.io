---
layout: widepage
title: Questioning the Teams
dimension: sc2.2
overview: |
    To have a functioning software team, you gotta get folks on the same page. This lesson helps you figure out whether everyone on the team knows the story and how well they know it.
---
# Lesson {{ page.lesson }} - {{ page.title }}

*This lesson is about a medium priority "State capacity" indicator in the health rubric.* 

{% include rubric dimension="sc2.2" %}

To have a functioning software team, you gotta get folks on the same page. This lesson helps you figure out whether everyone on the team knows the story and how well they know it.

* TOC
{:toc}

## Reflection: What makes a team work? (15m, pair)

**Timer**: {% include countdowntimer id="rpvp" minutes=15 %}

First, take some time to think through what makes a good functioning team. Grab a colleague and brainstorm some good signs on teams. 

You can discuss when and how team members relate to each other and debate the value of everyone on the team understanding each other's piece of the pie vs. team members working away in their own silos. In what cases do team members have to know about each other's work, and how much should they know?

Take notes and be ready to share.

## Asking questions of teams

### Read: Asking Questions of Software Project Teams (45m, solo) 

It can be hard to know where to ask sofware teams questions that tease out their team and project health. There's a few items that may help you knmow what to ask.

1. [Asking Questions of Software Project Teams](https://federalist-eb7b399c-56d9-4c6b-b524-27e0627cdd86.app.cloud.gov/preview/jadudm/cms-htmd/staging/questioning/)
2. [Ask Technical Questions of Agencies](https://derisking-guide.18f.gov/state-field-guide/#ask-technical-questions-of-agencies)

And for bonus reading on evaluating projects, the [whole 18F State Field Guide](https://derisking-guide.18f.gov/state-field-guide/) is worth a look!

As you read these, take notes on anything that jumped out at you. Can you see yourself using this with any of your projects? How do you think it would go?


### Paying attention to who answers what (10m, solo)

We're going to go a bit further here and have some subejcts to think through for your questions.
As you think these through, remember you'll need to note a few things. Does the vendor give all the answers? Does the state know what they’re buying and the terms of their vendor contract? 

Subjects to ask about:

Technology
* Who hosts the software tool?
* Does the state have access to the code?
* Program/team goals
* What are the main goals of this tool and how do they solve the problem?


End Users
* What do we know about the users of the tool?
* How are we building and improving the tool to fit our desired user outcomes?

Vendor
* What’s the duration of the relationship with the vendor? Under what circumstances does it end?
* Which departments have to know what about the contract and how it affects the work? (IT, Procurement, software...do they all understand it?)


### Watch: Unpacking the Jargon (15m, solo)

I'll borrow a quote from a previous lesson on state capacity:

"To assess project health, you'll need to be able to keep up with the jargon. And, frankly, *jargon is a great way to bullshit someone*. If I want you to 1) think I know what I'm talking about, but 2) confuse you along the way, I'm going to use jargon and words that I think you don't know well. If a product manager or project manager wants to mislead you regarding the health of a project, or otherwise mislead you as to how things are going, they're going to hide behind the words of their trade, and try and hide the realities of a project's health in the details."

Another way to get around jargon is to ask the person speaking to explain it to you like you're a small child. Or a golden retriver. I'm sharing this movie clip for inspiration, but definitely not endorsing this using this sort of behavior to ask for simplified language.

<iframe width="560" height="315" src="https://www.youtube.com/embed/SmHl7hKlVj4" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


## Roleplay: Play the Part (45m, group)

To close out this lesson, come together with your learning cohort. *EDIT THIS TO BE ABOUT ASKING STATES!!!!!!*

1. **Checkin**. {% include countdowntimer id="checkin" minutes=10 %} How is everyone? Take a moment to go around the group, and offer up something that brought you joy this past week. Start with birthdays in December, and work backwards throguh the year.
2. **Prep**. {% include countdowntimer id="prep" minutes=3 %} Now, count off, so that half of the group is an "Green" group and half the group is "Purple." The green group should put themselves in the place of their state's project, and imagine themselves as a program manager for that project. The purple group should take this time and imagine they are prepping for a conversation with the program manager to work on assessing project health. Take three minutes to prep for the roleplay.
3. **Breakout I**. {% include countdowntimer id="uam" minutes=5 %} Break into pairs. The purple group should be playing the role of a state officer talking to the project's program manager, working to understand the health of the project. The green group should be playing the role of a program manager working on their state's software.
4. **Debrief I**. {% include countdowntimer id="uam" minutes=15 %} After 5 minutes, come back to your large group. As a group, discuss the roleplays. 
   * For the purple group: What questions were particularly useful? What words/behaviors did you note from the program managers that were encouraging or inspired confidence? 
   * For the green group: How did getting into the program manager's head shape your thinking about the role of the SO? What mindset did you bring to the conversation? Was it collaborative? Evasive? Why?
5. **Repeat**. Repeat steps 2, 3, and 4, but switching roles.
6. **Wrap**. {% include countdowntimer id="wrap" minutes=5 %} Take a moment, before leaving, to share what your favorite moments were from the learning activity. Go around the group, and offer one kudo to your roleplay partner---something they did that you thought was particularly wonderful, fun, or insightful. 


{% capture body %}
<p>
    Roleplays are fun.
</p>

<p>
   They are also a powerful simulation tool. When you roleplay the vendor-side, you're stepping out of your normal headspace, and attempting to imagine the system that you are part of from another perspective. In terms of evaluation, this is a critical skill.
</p>

<p>
   When you are roleplaying the State Officer engaging with the vendor, you're developing and practicing questioning skills that are fundamental to your work. But, you're practicing them in a safe environment where, if you make mistakes, you get to step back with colleagues and discuss what might have been a better approach.
</p>

<p>
   The point being: regardless of which role you are in, you're developing a powerful set of skills and habits of mind that are intended to improve your ability to imagine and detect bullshit (Learning Goal #2) as well as improve your confidence in digging into the work of your states and their vendors (Learning Goal #4). And, at the risk of being redundant, let's be honest... <em>roleplays are fun</em>. <pre>:)</pre>  
</p>
{% endcapture %}
{% include alert level="no-icon" heading="Regarding Roleplays" body=body %}

## Reflection (15-30m, solo)

CMS oversees large, complex projects that involve many people, lots of dollars, over a long period of time. The program and project managers on those projects are critical stakeholders in the process; they have leadership roles in the design and delivery of the software, and they are not without hopes, biases, and faults. As a SO, it is up to you to understand not only the projects they are overseeing, but these people and the roles they inhabit, so that you can better work with them and understand the progress being made on delivering excellent tools to the people.

Take some time to reflect on the roleplay, and the thoughts it inspired regarding your work with your state. 

* What questions might you begin asking going forward? 
* What processes do you think you might want change? 
* What processes are working well? 
* Are there more things you feel you need to learn to tackle this space better? 

Those questions are offered as starting points only. You are welcome to take your reflection in whatever direction is best for you.

{% include airtable-post.html %}
