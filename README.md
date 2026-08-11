<div align="center">

<img src="https://raw.githubusercontent.com/AraGhah/AraGhah/main/Assets/hero.svg" alt="Ara Ghahramanyan, backend and full-stack developer in Montréal" width="100%"/>

<br/>

[![Portfolio](https://img.shields.io/badge/Portfolio-Hall_of_Projects-000000?style=flat-square&logo=vercel&logoColor=white)](https://ara-hall-of-projects.vercel.app)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-ara--ghahramanyan-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/ara-ghahramanyan)
[![Email](https://img.shields.io/badge/Email-Contact-c9d1d9?style=flat-square&logo=maildotru&logoColor=white)](mailto:YOUR_EMAIL)

</div>

Third-year Computer Science Technology student at Collège de Bois-de-Boulogne, graduating June 2027. I work mostly in C#/.NET and TypeScript, with AWS and PostgreSQL underneath.

**Looking for a software development internship starting January 2027**, in Montréal or Laval (on-site or hybrid), or fully remote within Canada.

## Projects

### SentinelOps

Incident management and on-call platform, in the vein of PagerDuty.

<img src="https://raw.githubusercontent.com/AraGhah/AraGhah/main/Assets/pipeline-sentinelops.svg" alt="Three duplicate alerts are fingerprinted, collapsed into one incident, and routed to an on-call responder" width="100%"/>

Alerts arrive from multiple sources at unpredictable rates, and the same underlying failure often fires dozens of times. SentinelOps ingests those alerts, deduplicates them into a single incident, routes it to a responder, and tracks state through to resolution in real time.

The interesting problem is the one in the diagram: two alerts describing the same failure can land milliseconds apart on different Lambda invocations, and both will happily create an incident unless the write path is designed against it. [Add one sentence on how you actually solved it: fingerprint keys, a Redis lock, a unique constraint plus upsert, whichever it was. This is the line an interviewer will stop on.]

Event-driven on AWS Lambda with infrastructure defined in CDK, so environments are reproducible rather than hand-configured.

`C#` `ASP.NET Core` `AWS Lambda` `AWS CDK` `PostgreSQL` `Redis` `Next.js` `TypeScript` `Docker`

[Repository](https://github.com/AraGhah/SentinelOps)

### TradeCatch

Missed-call recovery for local service businesses.

<img src="https://raw.githubusercontent.com/AraGhah/AraGhah/main/Assets/flow-tradecatch.svg" alt="A missed call hits an idempotent webhook handler, which sends an SMS to the caller and alerts the owner" width="100%"/>

A plumber who misses a call while under a sink loses the job to whoever answers next. An unanswered call triggers an automated SMS follow-up, captures the lead, and notifies the owner, so the enquiry survives the moment nobody picked up.

Most of the engineering sits in the parts customers never see. Telephony webhooks arrive out of order and more than once, so message handling has to be idempotent. Delivery is not guaranteed, so failures need retries and a record of what actually reached the customer. The site is bilingual end to end, which means routing, content, and outbound templates all carry locale.

`Next.js` `TypeScript` `PostgreSQL` `Twilio` `Resend` `Cloudflare` `Tailwind CSS` `CI/CD`

[Repository](https://github.com/AraGhah/TradeCatch)

### Hall of Projects

My portfolio, built as a space you walk through rather than a page you scroll.

Each project is a door. Opening one leads to a case study covering the problem, the architecture, and the decisions I would make differently now. The build is an exercise in animation performance and state: transitions stay smooth while route changes, locale, and view state are kept in sync, and the whole thing is bilingual through next-intl.

`Next.js` `TypeScript` `Framer Motion` `next-intl` `Tailwind CSS`

[Live site](https://ara-hall-of-projects.vercel.app) · [Repository](https://github.com/AraGhah/Portfolio)

## Stack

<div align="center">

<img src="https://skillicons.dev/icons?i=cs,dotnet,ts,react,nextjs,nodejs,postgres,redis,aws,docker,cloudflare,githubactions,tailwind,linux&theme=dark&perline=7" alt="C#, .NET, TypeScript, React, Next.js, Node.js, PostgreSQL, Redis, AWS, Docker, Cloudflare, GitHub Actions, Tailwind, Linux"/>

</div>

## How I work

I design before I implement, because the cost of a bad data model compounds and the cost of a bad function does not. I assume every external service will fail, arrive twice, or arrive out of order, and I write the handler accordingly. I automate anything I have done manually three times.

<div align="center">
<br/>

```
ara@montreal ~ $ echo "Open to internships starting January 2027."
Open to internships starting January 2027.

ara@montreal ~ $ _
```

</div>
