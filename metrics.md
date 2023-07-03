# Metrics, why, what, and how

## Why

* You measure to understand your team's performance.
* You measure to understand your team's problems and solve them.
* You measure to understand and replicate the goodness in your team.
* You measure to understand the external limitations on your team and address them.

### Why not

* You don't measure to report. Reporting is a side effect unless you are an executive who is trying to set a narrative.
* You don't measure to set targets. Targets are an incidental and often temporary choice. E.g., a team might choose to reduce their cycle time or not, but they must always measure it as a metric if they include it in their metrics list. Always remember [Goodhart's law](https://en.wikipedia.org/wiki/Goodhart%27s_law)

## What

Ideal measures for an engineering team to start with

**Team performance**

Cycle time - the average time it takes for a ticket to go from in-progress to done.
    *Note: Done in this case refers to deployment to production. If your team is not in a position to ship to production regularly, then figure out the nearest finish line. And set a vision to make the production the finish line in the future.*

Incident count - the number of incidents reported from the field by customers or the CS team. Measure this grouped by priority.

Defect count - the number of defects reported by QA or other team members. Measure this grouped by priority.

Velocity - measure of average work that a team can do in a delivery cycle. **Internal measure to be used only for forecasting purposes. Not of any value to anybody outside the team.**

**Application performance**

Up-time - the percentage of time an application (could be an entire website or individual services/infrastructure) has been available and functional.

Mean-time-to-resolve - the average time it takes to restore an application or service or infrastructure to a functional state.

[Apdex score](https://en.wikipedia.org/wiki/Apdex) - A standardized measure to understand user experience and satisfaction.

As a team gets more practice with measuring, debugging, and solving metrics, they can adopt more measures such as lead time, number of deployments, A11y scores, etc.

**Subjective measures**

Developer experience

Customer experience

CS experience

Measured via quick surveys.

## How

### to measure metrics?

* Use as much automation as required.
  - Pull cycle time reports from JIRA's control chart
  - Set up filters to measure incident and defect leaks
  - Use NewRelic and other DevOps tools to measure application performance
* But not more than required
  - Consider diminishing value of returns. If it takes 15 minutes every sprint to update values from your JIRA report to an excel sheet, is it worth investing a few weeks to automate that?
  - Consider the value of mindful toil. some amount of manual effort can bring about more awareness - you will wonder about why cycle time is high if you are copying the average value by hand.
* Improve automation incrementally. Start with a path of least resistance and then automate when required. 

### often to measure metrics?

* The ideal interval would be to measure at the end of your delivery cycle. If you follow a 2-week sprint cycle measure every 2 weeks. If you follow a Kanban approach, measure it before your retro.
* Experiment and learn. Some metrics might give you more insights when reviewed as monthly or quarterly aggregates - set up systems to get aggregated measures from your periodic measures.
* In case of aggregated measures, be mindful of the choice of aggregation. What insight can you learn or are you missing by choosing a monthly **mean** of incident count instead of a **median**?

### must they be reviewed?

* Use your retro to review your metrics. Share the metrics dashboard(s) before the retro.
* Get your entire team to care about the numbers. Explain what they indicate and what a change in them means. **Your team is driving a car. Your metrics are your dashboard. The entire team must care about fuel being low, the engine being at fault, or the accelerometer showing that you are going too fast.**
* Debug metrics together with your team. If your cycle time is too high, look into the control chart and review individual issues to see if there is a pattern. If your defect count is too high, look into the issues and see if there is a part of your application that is defect-prone and needs additional tests or even complete rewriting.
* Celebrate metrics together. Celebrate consistency in measurement. Celebrate improvements.
* Rotate and delegate metric duty - great way to get everybody to care about them. Great way to grow leaders - leaders will automatically spot areas of improvement that they can work on to add value.

### must they be debugged and addressed?

* Remember, most software engineering problems are solved problems.
  - You don't have to reinvent a new Agile process to improve your team's quality or redesign a revolutionary cache to improve your application's performance. Make a habit of [standing on the shoulders of giants](https://en.wikipedia.org/wiki/Standing_on_the_shoulders_of_giants).
* Prioritize culture over everything else.
  - You can't make meaningful improvements unless you have a blame-free culture that trusts the team.
* Prioritize quality over speed.
  - If your incident and/or defect count is too high, take on lesser work in future sprints and invest in automation and quality improvement processes like [3-amigos](https://www.scrum.org/resources/blog/3-amigos-bytesize-agile) and [example mapping](https://cucumber.io/blog/bdd/example-mapping-introduction/).
* Prioritize consistency over speed.
  - If your velocity or cycle time has been fluctuating get to a steady state by committing and completing the same amount of work before trying to accelerate. Use [planning poker](https://www.atlassian.com/blog/platform/a-brief-overview-of-planning-poker) with past stories and velocity data as reference to make estimates and commitments.
* Improvements in speed come from managing risk.
  - Break your work into smaller chunks that can be delivered quickly. Do you need to deliver all the charts on a particular screen? Do you need a forgot password link to finish the login feature? Can you rely on feature flags to deliver to production faster?
  - Focus on completion as a team. Limit work-in-progress items. Stop all new work if someone is blocked in code review or QA. Nobody has delivered if the team as a whole has not delivered. Corollary: It is better to have 50% of your sprint tasks 100% complete than 100% of your sprint tasks 75% complete.
  - Set a sprint goal and drive the team towards finishing that goal. A goal can be finished even with some of the tasks in the sprint being incomplete. E.g.,
    - *Launch the MVP version of our home page*
    - *Deliver reports via plain text email*
    - *Deliver rich text report with attachments*
   
### must they be reported?

* Report less frequently than you measure and review. If you have a 2-week review cycle, report monthly or quarterly. Go for a slightly shorter reporting cycle if there are trust issues or crises.
* Prepare for your reporting. Review the metrics, review your team's analysis, and review the changes you have done and plan to do. If you are reporting to executive leadership, be prepared for tough questions - it is their instinct to glean meaning from these metrics.
* Be honest in your reporting. Your leadership team has been through the journey that you are just starting on. They can catch attempts to gloss over. Your leadership team also wants you to succeed. So explain your challenges and take feedback on your ideas to address them.
* As an advanced technique, try to use the metrics to state your requirements to your leadership team. A low cycle time, high customer incident, and low defect count metric graph might be a good graph to show to your leadership and ask for a QA to be hired in your team.

## Conclusion

Measuring metrics is an exercise in balance. Why, what, and how you measure will change based on context and you have to make an informed choice. If you are not measuring them, then remember, to not measure is also a choice and one that can harm you and your team. With metrics that are measured, reviewed, and reported honestly, you can confidently say,

*It matters not how strait the gate,<br/>*
*How charged with punishments the scroll,<br/>*
*I am the master of my fate<br/>*
*I am the captain of my soul.<br/>*

and that is saying a lot in the software industry.
