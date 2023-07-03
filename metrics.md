## Metrics, why, what, and how

#### Why

* You measure to understand your team's performance.
* You measure to understand your team's problems and solve them.
* You measure to understand and replicate the goodness in your team.
* You measure to understand the external limitations on your team and address them.

#### Why not

* You don't measure to report. Reporting is a side effect unless you are an executive who is trying to set a narrative.
* You don't measure to set targets. Targets are an incidental and often temporary choice. E.g., a team might choose to reduce their cycle time or not, but they must always measure it as a metric if they include it in their metrics list. Always remember [Goodhart's law](https://en.wikipedia.org/wiki/Goodhart%27s_law)

#### What

Ideal measures for an engineering team to start with

**Team performance**

Cycle time - the average time it takes for a ticket to go from in-progress to done.
    *Note: Done in this case refers to deployment to production. If your team is not in a position to ship to production regularly, then figure out the nearest finish line. And set a vision to make the production the finish line in the future.*

Incident count - the number of incidents reported from the field by customers or the CS team. Measure this grouped by priority.

Defect count - the number of defects reported by QA or other team members. Measure this grouped by priority.

**Application performance**

Up-time - the percentage of time an application (could be an entire website or individual services/infrastructure) has been available and functional.

Mean-time-to-resolve - the average time it takes to restore an application or service or infrastructure to a functional state.

[Apdex score](https://en.wikipedia.org/wiki/Apdex) - A standardized measure to understand user experience and satisfaction.

As a team gets more practice with measuring, debugging, and solving metrics, they can adopt more measures such as lead time, number of deployments, A11y scores, etc.

#### How

TODO: How should the metrics be measured? How often must metrics be measured? How must they be reviewed? What should be done with observations?
