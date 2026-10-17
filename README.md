<div align="center">

<img src="https://raw.githubusercontent.com/AraGhah/AraGhah/main/Assets/hero.svg" alt="Ara Ghahramanyan, backend and full-stack developer in Montréal" width="100%"/>

<br/>





</div>

Third-year Computer Science Technology student at Collège de Bois-de-Boulogne, graduating June 2027. I work mostly in C#/.NET and TypeScript, with AWS and PostgreSQL underneath.

Looking for a software development internship starting January 2027, in Montréal or Laval (on-site or hybrid), or fully remote within Canada.

Projects

Dossier

AI-powered prospect research and personalized cold email generation.

Dossier tackles a common problem in outbound sales: meaningful personalization takes time, but generic messages rarely stand out. The platform automates prospect research and turns information about people and companies into tailored outreach at scale.

The workflow gathers information from external sources, processes it through AI models, and generates personalized messages that can be used in outbound campaigns. It connects research, generation, validation, and delivery-oriented workflows rather than treating each email as an isolated prompt.

The engineering challenge is reliability when an external AI service does not always return predictable output. During development, some responses contained incorrect information, missing fields, or invalid JSON. I improved the prompts and added backend validation to reject malformed or incomplete responses before they reached the database.

Built with n8n automation, Supabase/PostgreSQL, Apify for prospect data, and Claude for research and generation.

n8n Supabase PostgreSQL Apify Claude API REST APIs JSON Validation Workflow Automation

Live site

SentinelOps

Incident management and on-call platform, in the vein of PagerDuty.

<img src="https://raw.githubusercontent.com/AraGhah/AraGhah/main/Assets/pipeline-sentinelops.svg" alt="Duplicate alerts are grouped into an incident and routed to an on-call responder" width="100%"/>

Alerts arrive from multiple sources at unpredictable rates, and the same underlying failure often fires dozens of times. SentinelOps ingests those alerts, deduplicates them into a single incident, routes it to a responder, and tracks state through to resolution in real time.

A key concurrency problem is that two alerts describing the same failure can arrive milliseconds apart on different Lambda invocations. Without a carefully designed write path, both can create separate incidents. Handling duplicate events and keeping incident state consistent are central concerns in the system.

Event-driven on AWS Lambda with infrastructure defined in CDK, so environments are reproducible rather than hand-configured.

C# ASP.NET Core AWS Lambda AWS CDK PostgreSQL Redis Next.js TypeScript Docker

Repository

TradeCatch

AI receptionist and missed-call recovery for local service businesses.

<img src="https://raw.githubusercontent.com/AraGhah/AraGhah/main/Assets/flow-tradecatch.svg" alt="TradeCatch missed-call recovery flow: webhook, SMS follow-up, and owner notification" width="100%"/>

A plumber who misses a call while under a sink can lose the job to whoever answers next. TradeCatch helps contractors capture those opportunities through an AI receptionist and automated follow-up workflows.

The AI receptionist is designed to answer incoming calls, respond to common customer questions, book appointments, and transfer calls to the contractor when a human is needed. If a call still goes unanswered, the missed-call workflow sends an SMS follow-up, captures the lead, and alerts the owner.

Most of the engineering sits in the parts customers never see. Telephony webhooks may arrive out of order or more than once, so message handling must be idempotent. Delivery is not guaranteed, so failures need retries and a record of what actually reached the customer. The platform also supports bilingual English and French communication across the site and customer-facing messages.

Next.js TypeScript PostgreSQL Twilio Resend Cloudflare Tailwind CSS AI Integration Webhooks CI/CD

Repository

Stack

<div align="center">

<img src="https://skillicons.dev/icons?i=cs,dotnet,ts,react,nextjs,nodejs,postgres,redis,aws,docker,cloudflare,githubactions,tailwind,linux&theme=dark&perline=7" alt="C#, .NET, TypeScript, React, Next.js, Node.js, PostgreSQL, Redis, AWS, Docker, Cloudflare, GitHub Actions, Tailwind, Linux"/>

</div>

How I work

I design before I implement, because the cost of a bad data model compounds and the cost of a bad function does not. I assume every external service will fail, arrive twice, or arrive out of order, and I write the handler accordingly. I automate anything I have done manually three times.

<div align="center">
<br/>

ara@montreal ~ $ echo "Open to internships starting January 2027."
Open to internships starting January 2027.

ara@montreal ~ $ _

</div>
