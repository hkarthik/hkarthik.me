---
layout: post
title: "Beating the Talent Crunch With a Distributed Team"
date: 2011-12-12 19:05
comments: true
categories: 
---
There's been a lot of press lately about the severe shortage of software 
engineers across the country. I have been involved in hiring engineers in 
multiple companies over the past few years and I've seen a steady 
shrinking and dispersion of the available talent pool. I believe 
that the only solution to the talent crunch in the short term is to build 
and grow distributed teams. 

After working closely with successful distributed teams in the past, I 
became aware of how well they work when grown carefully. To that end, 
I sought out a role with a distributed team to learn how they operate and 
utilize these skills to help build and lead teams in the future.

This post is to share some of what I've observed and learned after 6 
months of working in a distributed team at [Pure Charity](http://purecharity.com).

## Distributed Hiring
Hiring members of a distributed team is not all that different from 
hiring a colocated team. Here are some core guidelines.

- Focus on internal referrals from active team members.
- If your internal referrals run dry, reach out to the larger community.
- Look at actual code via OSS contributions or code snippets they share.
- Spend a day pair programming remotely on a real world problem to see how they 
  fit in with the existing team.
- Try to keep everyone within a single timezone.

Everyone knows a weak link hurts the whole team, but in a distributed 
team, it can hurt even more. The good news is, you have a wider talent 
pool to work with and can afford to be a bit pickier with whom you hire 
to mitigate this risk.

## The Chatroom
The team chatroom provides a number of advantages. Here are a few.

- A common communication area where team members can get rapid feedback 
  and bounce ideas around.
- A focused area for private messaging without the noise of typical IM 
  networks.
- A watercooler for the random banter that builds camaraderie among 
  teams.  
- Relief from the constant flood of email.

The last point is very important. Since working in a distributed team, 
my email volume has dropped significantly and I don't have to spend much 
time managing my inbox to stay on top. That has been invaluable.

There a number of products, aside from the standard IRC, that can host 
the chatroom. My favorite is [HipChat](http://hipchat.com), but many 
teams use [Campfire](http://campfirenow.com). I like the hosted services 
since they can parse code, share files, embed images/video, 
and log conversations. Plus, they are a lot of fun when you add a
[Hubot](http://hubot.github.com).

## Audio Conferencing
When ideas are not easily communicated via IM, email, or the 
Chatroom, it's best to hold an audio conversation. There are a number of 
solutions to this but I suggest the following guidelines:

- Choose one that runs on low bandwidth networks with good audio quality.
- Everyone on the team should use the same product.
- Have everyone stay online as much as possible during the work day.

Our team, being composed entirely of Mac users, uses iChat to quickly have push button audio 
communication within small groups. Many other teams use Skype. Choose 
what you like, but make sure everyone uses the same thing and it remains 
frictionless. 

## Video Conferencing
A robust video conferencing solution is essential to help team members
hold both regular meetings and ad-hoc touch points. The things to look for here are:

- Good cross platform support 
- Excellent audio and video quality for multiple participants 
- The ability to quickly let participants share their screen.

My favorite tool for this is GoToMeeting, but many teams 
use WebEx, Skype, or free products for this. The better solutions come at a 
premium price, but it's well worth it. Regular face time over video
conferencing helps the team gel better.

## Remote Pair Programming
A great way to help development teams stay focused and productive is to give them the right 
tools for pair programming. In our team, nearly everyone is comfortable 
using Vim as their editor. With the combination of Tmux + Vim, team 
members can remotely pair program and control a single shared terminal 
session. In this termimal session, everyone has keyboard control on a low bandwidth 
connection. This is extremely useful when pair programming or mentoring more junior developers. 

If your development environment really requires the use of an 
IDE, I have heard good things about using [TeamViewer](http://www.teamviewer.com) as an alternative.

## The Workstream 
This suggestion may be a little controversial, but I suggest having every team 
member keep a running log of what they work on during the day. When you're working in a
distributed team, it's easy to lose track of what each team member is 
working on. While you can always IM or make calls, it's far less 
intrusive to glance at the workstream to get a heartbeat on the team's 
progress. 

In addition, the workstream provides the whole team with transparency and 
helps keep everyone focused. You can more easily see if someone is spinning their 
wheels and help them get unstuck long before they have to ask. This helps a lot with 
onboarding and ramping up new team members without making them feel 
too micro-managed. Also, it helps build an environment of mutual trust and 
understanding.

We use [Coopapp](http://coopapp.com) and [Harvest](http://harvesthq.com) to have team members track their work hours along 
with any paid time off.

If tracking time feels a little too intrusive to you, I recommend using [Yammer](http://yammer.com) and having 
your team provide micro-updates periodically. 

## Don't Cross the Streams
One of the biggest areas where I see companies go wrong is mixing remote 
team members with colocated members. Nothing sucks more than being the 
one guy on the phone in a room full of colocated developers. It can be isolating, 
frustrating, and terribly unproductive for everyone involved. 

If you've already got a colocated team, the best thing you can do is 
hire more colocated team members. If you're struggling to hire locally, 
then hire two or more remote workers that have worked together 
previously to seed a distributed team. Keep their work separate from 
that of your colocated team. Or let some of your colocated team members 
work from home to help seed the distributed team.

## Plan for Face Time
At least once a quarter, plan on getting everyone together in one
physical location for a few days of work, along with a night or two out. Such
sessions will be highly effective and the evenings are great for team building. During
the day, set a clear agenda and try to stick to it. 

## Final Thoughts
Distributed teams definitely come with certain challenges, and it's 
critical to keep the teams small to minimize the communication difficulties. Many companies 
like 37signals, GitHub, and Living Social have all used these 
strategies effectively to build a remote workforce so there's no reason 
it can't work for you too. If you have thoughts or experiences to share,
please do so in the comments.

