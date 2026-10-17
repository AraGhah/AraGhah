<div align="center">

<img src="https://raw.githubusercontent.com/AraGhah/AraGhah/main/Assets/hero.svg" alt="Ara Ghahramanyan, backend and full-stack developer in Montréal" width="100%"/>

<br/>

[![Portfolio](https://img.shields.io/badge/Portfolio-Hall_of_Projects-000000?style=flat-square\&logo=vercel\&logoColor=white)](http://araghah.com/)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-ara--ghahramanyan-0A66C2?style=flat-square\&logo=linkedin\&logoColor=white)](https://www.linkedin.com/in/ara-ghahramanyan)
[![Email](https://img.shields.io/badge/Email-Contact-c9d1d9?style=flat-square\&logo=maildotru\&logoColor=white)](mailto:YOUR_EMAIL)

</div>

Third-year Computer Science Technology student at Collège de Bois-de-Boulogne, graduating June 2027. I build backend and full-stack applications with C#/.NET and TypeScript, with a focus on reliable APIs, automation, and cloud infrastructure.

**Looking for a software development internship starting January 2027**, in Montréal or Laval (on-site or hybrid), or fully remote within Canada.

## Projects

### SentinelOps

Incident management and on-call platform, in the vein of PagerDuty.

<img src="https://raw.githubusercontent.com/AraGhah/AraGhah/main/Assets/pipeline-sentinelops.svg" alt="Three duplicate alerts are fingerprinted, collapsed into one incident, and routed to an on-call responder" width="100%"/>

Alerts arrive from multiple sources at unpredictable rates, and the same underlying failure can fire dozens of times. SentinelOps ingests those alerts, deduplicates them into a single incident, routes it to an on-call responder, and tracks state through resolution.

The tricky part is concurrency. Two alerts describing the same failure can land milliseconds apart on separate Lambda invocations; without a safe write path, both can create an incident. The design has to account for duplicate events, retries, and consistent incident state rather than assuming each alert arrives exactly once.

Event-driven on AWS Lambda, with infrastructure defined in CDK so environments are reproducible rather than hand-configured.

`C#` `ASP.NET Core` `AWS Lambda` `AWS CDK` `PostgreSQL` `Redis` `Next.js` `TypeScript` `Docker`

[Repository](https://github.com/AraGhah/SentinelOps)

### TradeCatch

AI receptionist and missed-call recovery for local service businesses.

<img src="https://raw.githubusercontent.com/AraGhah/AraGhah/main/Assets/flow-tradecatch.svg" alt="Missed-call recovery flow: incoming call, webhook, SMS follow-up, and owner notification" width="100%"/>

A plumber who misses a call while working can lose the job to whoever answers next. TradeCatch helps service businesses capture those opportunities with an AI receptionist that can answer incoming calls, respond to customer questions, book appointments, and transfer calls to the contractor when a person needs to step in.

When a call goes unanswered, a separate recovery flow sends an SMS follow-up, captures the lead, and notifies the business owner. The goal is simple: a potential customer should not disappear just because nobody was available to pick up.

The engineering sits in the handoffs. Telephony webhooks can arrive out of order or more than once, so handlers need to be idempotent. SMS delivery is not guaranteed, so failures require retries and delivery tracking. The site and customer-facing workflows also support both English and French.

`Next.js` `TypeScript` `PostgreSQL` `Twilio` `Resend` `Cloudflare` `Tailwind CSS` `AI Integration` `Webhooks` `CI/CD`

[Repository](https://github.com/AraGhah/TradeCatch)

### Dossier

AI-powered prospect research and personalized cold email generation.

Personalized outreach works better when it reflects something specific about the person receiving it, but doing that research manually does not scale. Dossier collects prospect and company context, uses AI to turn that research into tailored outreach, and connects the results to an automated campaign workflow.

The pipeline brings together data collection, enrichment, generation, validation, and storage. n8n coordinates the workflow, Apify supplies prospect research data, Claude generates personalized copy, and Supabase/PostgreSQL stores the structured results. It is designed for repeatable campaigns involving hundreds or thousands of prospects, not one-off prompts.

The most interesting problem was making AI output dependable. Some model responses contained unsupported details, missing fields, or invalid JSON. I analyzed the failed responses, improved the prompt structure, and added backend validation to reject bad outputs before saving them to the database. That turned a fragile generation step into a more reliable part of the pipeline.

`n8n` `Supabase` `PostgreSQL` `Apify` `Claude API` `REST APIs` `JSON Validation` `Workflow Automation`

[Live site](https://rundossier.co)

## Stack

<div align="center">

<img src="https://skillicons.dev/icons?i=cs,dotnet,ts,react,nextjs,nodejs,postgres,redis,aws,docker,cloudflare,githubactions,tailwind,linux&theme=dark&perline=7" alt="C#, .NET, TypeScript, React, Next.js, Node.js, PostgreSQL, Redis, AWS, Docker, Cloudflare, GitHub Actions, Tailwind, Linux"/>

</div>

## How I work

I design before I implement, because the cost of a bad data model compounds and the cost of a bad function does not. I assume external services can fail, retry, or send the same event twice, and I build the integration accordingly. I automate anything I have done manually three times.

<div align="center">
<br/>

```text
ara@montreal ~ $ echo "Open to internships starting January 2027."
Open to internships starting January 2027.

ara@montreal ~ $ _
```

</div>
