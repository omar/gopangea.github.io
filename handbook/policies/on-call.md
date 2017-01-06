---
title: On Call
---

## Goal
Establish a fair, predictable schedule, and clear roles and responsibilities.

## Actors

- All Engineers

## Calendar

The calendar will be handled by Bardia and the Platform team to make changes and overrides. If an engineer will not be available to handle the scheduled
on call responsibility, they should switch schedules with another engineer. The calendar should reflect this change, otherwise that engineer is still
responsible for the scheduled period.

Should the calendar day happen to be a company holiday, the engineer on-call will be reimbursed with PTO if significant time was required on that day.

## Escalation

Escalation will happen automatically after X minutes without acknowledgement

- 15 minutes during working hours
- 45 minutes after hours

## Rotation

Engineers will be scheduled on a weekly rotation with handoff occuring on Monday at 9am.

## Responsibilities
Monitor all production application logs. Though the whole team should keep an eye on the alert-prod emails, it is the responsibility of the tech on-call
to ensure that they are monitered. Act as needed based on the email:

- Customer Impact
    - Determine severity of issue on customer funnel (i.e. creating an account, creating a transfer, delay in communications or staging of transfers etc.).
    - Determine scope of customer impact (i.e. how many customers are experiencing the issue).
    - Notify Senior team.
    - Collect list of impacted customers and send to Product team.
    - Conduct postmortem.

- Business Operations Impact
    - Determine severity of issue on business operations (i.e. Marketing/Compliance/Customer Service tooling and operations).
    - Determine scope of business operations impact (i.e. how many customers are experiencing the issue).
    - Notify affected groups (Marketing, Customer Service, Compliance, etc.)
    - Notify Senior team.
    - Conduct postmortem.
    - Handle all Customer Support Issues

## Acknowledgements
- During the on-call period, project work is secondary.
- Don’t investigate an email alert if a ticket exists in the backlog (Vantiv).
- All issues reported from tech on call that either affect team members or clients need to be prioritized and put on the current sprint.
- Notifications that do not require an action or need to be logged differently (i.e. as a warning instead of an error) need to be reported - as an issue and put on the current sprint immediately.
- The company will reimburse for expenses incurred for tech on call issues (i.e. mobile phone data and transportation to get to a computer).
- We need to agree on some form of compensation (PTO or other things) since the tech on call activities disrupt our normal activities - outside of working hours.
- Prioritize removing unnecessary alerts from being emailed (“Throw error to move to queue”).
- A shared MacBook Air for primary tech on call person to be used when expected to carry a laptop throughout the weekend.
- Though only one engineer will be on call and be the point of contact for the issue, we are a team and should act as such. If the tech oncall needs help, chip in.


## SLA

- Monday-Friday
    - 9am-6pm:
        - Product issues: 15 minutes response time
        - System outage: 15 minutes response time
    - 6pm-9am:
        - Product Issues: 60 minutes
        - System Outage: 15 minutes response time

- Saturday, Sunday, and Holidays:
    - 9am-6pm:
        - Product issues: 45 minute response time
        - System Outage issues: 15 minutes response time

    - 6pm-9am:
        - Product Issues: 60 minute response time
        - System Outage issues: 15 minute response time

## App Policy

Triage/diagnose every issue that comes in either through customer support or application error logs:

- Attempt to reproduce and determine customer impact right away.
- Determine severity of issue on customer funnel (i.e. creating an account, creating a transfer, delay in communications or staging of - transfers etc.).
- Determine scope of customer impact (i.e. how many customers are experiencing the issue).
- Collect list of impacted customers and send to Product team.
- Conduct postmortem (including tracking the ticket in JIRA).

### iOS/Android 

- For bugs fixed in new versions of the app, collect affected users and the version number to determine our force app update policy.
