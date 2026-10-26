<div align="center"> <img src="https://raw.githubusercontent.com/AraGhah/AraGhah/main/Assets/hero.svg" alt="Ara Ghahramanyan, backend and full-stack developer in Montréal" width="100%"/> <br/>

Portfolio LinkedIn Email

</div>

Third-year Computer Science Technology student at Collège de Bois-de-Boulogne, graduating June 2027. I build backend and full-stack applications with C#/.NET and TypeScript, with a focus on reliable APIs, automation, and cloud infrastructure. I have shipped two SaaS products end to end.

Looking for a software development internship starting January 2027, in Montréal or Laval (on-site or hybrid), or fully remote within Canada.

Projects
SentinelOps

Cloud native incident management and on-call platform, in the vein of PagerDuty.

<img src="https://raw.githubusercontent.com/AraGhah/AraGhah/main/Assets/pipeline-sentinelops.svg" alt="Three duplicate alerts are fingerprinted, collapsed into one incident, and routed to an on-call responder" width="100%"/>

Alerts arrive from multiple sources at unpredictable rates, and the same underlying failure can fire dozens of times. SentinelOps ingests those alerts, deduplicates them into a single incident, assigns a responder, and tracks the incident through resolution.

The tricky part is concurrency. Two alerts describing the same failure can land milliseconds apart on separate Lambda invocations; without a safe write path, both can create an incident. A DynamoDB deduplication layer with a concurrency safe write path handles duplicate events and retries, so incident state stays consistent instead of assuming each alert arrives exactly once.

Event driven on AWS Lambda behind API Gateway, with a secure ASP.NET Core REST API, DynamoDB for deduplication and incident state, and CloudWatch for monitoring.

C# ASP.NET Core AWS Lambda API Gateway DynamoDB CloudWatch

Repository

TradeCatch

Bilingual (FR/EN) AI receptionist and missed-call recovery for local service businesses in Québec.

<img src="https://raw.githubusercontent.com/AraGhah/AraGhah/main/Assets/flow-tradecatch.svg" alt="Missed-call recovery flow: incoming call, webhook, SMS follow-up, and owner notification" width="100%"/>

A plumber who misses a call while working can lose the job to whoever answers next. TradeCatch helps service businesses capture those opportunities with an AI receptionist that can answer incoming calls, respond to customer questions, book appointments, and transfer calls to the contractor when a person needs to step in.

When a call goes unanswered, a separate recovery flow sends an SMS follow-up, captures the lead, and notifies the business owner. The goal is simple: a potential customer should not disappear just because nobody was available to pick up.

The engineering sits in the handoffs. Telephony webhooks can arrive out of order or more than once, so handlers are idempotent. SMS delivery is not guaranteed, so failures are retried and delivery is tracked. The site and customer-facing workflows support both English and French.

Next.js TypeScript PostgreSQL Twilio Resend Cloudflare Workers Webhooks CI/CD

Website | Repository

Dossier

Past startup (January 2026 to July 2026). AI powered prospect research and personalized cold email openers for outbound agencies and B2B founders.

Personalized outreach works better when it reflects something specific about the person receiving it, but doing that research manually does not scale. For each prospect, Dossier pulled a verifiable public signal (recent posts, launches, hiring, funding news) and drafted three opener variants. A separate QA pass scored each one from 1 to 5 and flagged thin profiles, so weak copy was rewritten or rejected before delivery. Pilots of 100 prospects were delivered within 24 to 48 hours as CSV files ready for Smartlead, Instantly, Lemlist, Clay and Apollo.

The backend was custom built in TypeScript with Node.js and Express, with Apify supplying prospect data and PostgreSQL storing the structured results.

The most interesting problem was making AI output dependable. Some model responses contained unsupported details, missing fields, or invalid JSON. I analyzed the failed responses, restructured the prompts, and added backend schema validation that rejects bad output before it reaches the database. That turned a fragile generation step into a reliable part of the pipeline.

TypeScript Node.js Express PostgreSQL React Apify JSON Validation

Website

Stack
<div align="center"> <img src="https://skillicons.dev/icons?i=cs,dotnet,java,py,ts,react,angular,nextjs,nodejs,postgres,aws,docker,cloudflare,githubactions,linux&theme=dark&perline=8" alt="C#, .NET, Java, Python, TypeScript, React, Angular, Next.js, Node.js, PostgreSQL, AWS, Docker, Cloudflare, GitHub Actions, Linux"/> </div>
How I work

I design before I implement, because the cost of a bad data model compounds and the cost of a bad function does not. I assume external services can fail, retry, or send the same event twice, and I build the integration accordingly. I automate anything I have done manually three times.

<div align="center"> <br/>
text
ara@montreal ~ $ echo "Open to internships starting January 2027."
Open to internships starting January 2027.

ara@montreal ~ $ _
</div>
