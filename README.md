# Attio CRM MCP Starter Kit — Manage Attio with AI

[![MCP Compatible](https://img.shields.io/badge/MCP-compatible-blue)](https://modelcontextprotocol.io)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Platform: Attio](https://img.shields.io/badge/Platform-Attio-5856D6)](https://attio.com)

**A modern CRM built for data-driven teams — now with AI agents.** Open this repo in Amp, Cursor, or VS Code and manage Attio people, companies, and lists with AI — then export enriched data to ad platforms for targeted campaigns.

---

## Why Attio + AI?

Attio is the CRM for teams that outgrew spreadsheets but find Salesforce overkill. With a flexible data model, automatic contact enrichment, and relationship intelligence, Attio is the choice of startups, VC firms, agencies, and modern B2B teams.

For advertising, Attio's strength is data quality. It automatically enriches contacts with company data (size, industry, funding, tech stack), tracks relationship strength, and maintains flexible lists that can segment your contacts however you need.

An AI agent turns Attio into an ad targeting pipeline. Export your highest-value contacts to Google Customer Match. Build company lists for LinkedIn ABM. Sync deal-stage contacts to retargeting audiences. The agent handles the export, hashing, and upload.

**Best for:** Startups, VC firms managing deal flow, agencies managing client relationships, modern B2B teams wanting CRM-to-ad-platform synchronization.

---

## Quick Start (30 Seconds)

### Amp / Cursor / VS Code (Copilot)

1. **Get a free API key** at [syntermedia.ai/developer](https://syntermedia.ai/developer)
2. **Set the key:**
   ```bash
   export SYNTER_API_KEY=syn_your_key_here
   ```
3. **Open this repo** in your editor
4. **Start chatting** — MCP tools are pre-configured in `.mcp.json`

### Claude Desktop

Copy `claude_desktop_config.json` to your Claude config directory and replace the API key:

- **macOS:** `~/Library/Application Support/Claude/claude_desktop_config.json`
- **Windows:** `%APPDATA%\Claude\claude_desktop_config.json`

---

## What You Can Do

| Capability | Example |
|-----------|---------|
| **People Search** | "Find all people at Series B+ SaaS companies with VP+ titles" |
| **Company Intelligence** | "Show me everything we know about Stripe — contacts, notes, deals" |
| **List Management** | "Create a list of companies using React in their tech stack" |
| **Audience Export** | "Export our top 100 customers to Google Customer Match" |
| **Deal Tracking** | "What deals are in the pipeline? Which are stalled?" |
| **Relationship Mapping** | "Who at our firm has the strongest relationship with Acme Corp?" |
| **Enrichment Queries** | "Which companies in our CRM recently raised funding?" |
| **Attribution Notes** | "Add conversion attribution data to this person's record" |
| **Segment Building** | "Build a segment of contacts in fintech who've engaged in the last 30 days" |

---

## Example Conversations

### 1. VC Deal Flow to Ad Targeting

> **You:** I'm a VC and I want to advertise our fund to founders who match our investment thesis.
>
> **Agent:** I'll use your Attio data to build a targeted audience. Let me analyze your successful portfolio companies...
>
> **Portfolio company patterns (from Attio):**
> - 23 portfolio companies, all B2B SaaS
> - Average at investment: Series A, 20-50 employees, $2-5M ARR
> - Industries: DevTools (8), Fintech (6), MarTech (5), HealthTech (4)
> - Common founder traits: 2nd+ time founders, ex-FAANG, based in SF/NYC/Austin
>
> **Targeting strategy:**
> 1. Export portfolio founder emails → Google Customer Match → 1% Similar Audience
> 2. Export portfolio company domains → LinkedIn Matched Audience → Company Lookalike
> 3. Layer LinkedIn targeting: Founders/CEOs at Seed-Series A companies, 10-100 employees, SaaS industry
>
> **Ad messaging:** Not "Invest with us" — founders don't respond to that. Instead: "How [Portfolio Company] scaled from $2M to $15M ARR in 18 months" with a CTA to your founder network page.
>
> **You:** Love it. Start with LinkedIn only. $2,000/month.
>
> **Agent:** Exported 23 portfolio company domains from Attio. Created LinkedIn Matched Audience with 89% match rate. Campaign targets CEO/Founder at Seed-A companies in DevTools/Fintech. PAUSED until you approve.

### 2. Agency Client Relationship Management

> **You:** I run a marketing agency. Show me clients whose contracts are ending in the next 60 days.
>
> **Agent:** Pulling from your Attio "Clients" list with contract end dates...
>
> **Contracts expiring within 60 days:**
>
> | Company | Contract End | Monthly Retainer | Relationship Score | Last Contact |
> |---|---|---|---|---|
> | TechCorp | April 15 | $8,500 | Strong | 3 days ago |
> | GrowthHQ | April 22 | $5,200 | Declining | 18 days ago |
> | DataViz Inc | May 4 | $12,000 | Strong | 1 day ago |
> | CloudStart | May 11 | $3,800 | Weak | 42 days ago |
>
> **⚠️ At-risk renewals:**
> - **GrowthHQ:** Relationship score declining + 18 days since last contact = churn risk. Schedule a check-in this week.
> - **CloudStart:** Weak relationship + 42 days no contact = high churn risk. This needs immediate attention.
>
> **Retention strategy:**
> 1. Schedule renewal conversations with all 4 clients
> 2. For at-risk accounts, prepare a "wins recap" document showing ROI delivered
> 3. Consider running LinkedIn ads targeting their leadership team with case study content — so when they Google your agency, they see positive signals
>
> Want me to update the notes in Attio with renewal task reminders?

### 3. Tech Stack-Based Targeting

> **You:** I sell a Salesforce integration. Can I find companies using Salesforce in my CRM?
>
> **Agent:** Attio's enrichment includes tech stack data. Let me query...
>
> **Companies in your Attio using Salesforce:**
> - 847 companies total
> - 312 have a contact with VP+ title
> - 89 are in your "Engaged" list (opened emails or attended events)
>
> **Best targeting approach:**
> 1. **Warmest (89 engaged):** Direct outreach + LinkedIn retargeting
> 2. **Decision-makers (312 VP+):** Google Customer Match with Salesforce-specific ad copy
> 3. **Broad (847 total):** LinkedIn Matched Audience for awareness
>
> **Google Customer Match export:**
> - Export 312 VP+ contact emails from Attio
> - Upload to Google Ads → target with keywords like "Salesforce integration," "Salesforce automation"
> - These people already use Salesforce AND know your brand — conversion rates will be 3-5x higher than cold targeting
>
> **You:** Export the 89 engaged contacts to LinkedIn and Google.
>
> **Agent:** Done. 89 contacts exported. LinkedIn matched 73 (82%), Google matched 61 (69%). Both audiences are live and ready for campaign targeting.

### 4. Enriched Company Lists for ABM

> **You:** Show me companies in our Attio that recently raised funding.
>
> **Agent:** Querying Attio for companies with recent funding events...
>
> **Recently funded companies (last 90 days):**
>
> | Company | Round | Amount | Industry | Your Status |
> |---|---|---|---|---|
> | NeoData | Series B | $28M | Analytics | Cold — no engagement |
> | StreamLabs AI | Series A | $12M | DevTools | Warm — demo scheduled |
> | PayVault | Seed | $4M | Fintech | Cold — in ICP |
> | CloudMesh | Series C | $65M | Infrastructure | Cold — enterprise |
>
> **Why this matters for advertising:** Companies that just raised are actively spending on tools. They have budget, they're hiring, and they're making buying decisions. Post-funding is the best time to reach them.
>
> **Recommended actions:**
> 1. Add all 4 to your ABM target list in Attio
> 2. Export to LinkedIn Matched Audience for awareness ads
> 3. Create Google Ads campaigns targeting each company's brand name + your product category
> 4. Custom ad copy: "Congratulations on the raise! Here's how [your product] helps fast-growing teams scale"

### 5. Conversion Attribution Write-Back

> **You:** A lead just signed up from our Google Ads campaign. Can you record that in Attio?
>
> **Agent:** I'll create an attribution note on the person's Attio record. Give me their email or name.
>
> **You:** jane@techcorp.com — she came from our "SaaS Analytics" Google campaign.
>
> **Agent:** Found Jane Chen, VP Engineering at TechCorp in Attio. I'll add:
>
> **Note added to Jane's record:**
> - Source: Google Ads — "SaaS Analytics" campaign
> - Medium: cpc
> - Campaign: SaaS Analytics Q1
> - Landing page: /features/analytics
> - Conversion: Free trial signup
> - Date: March 22, 2026
> - Value: $0 (trial) — potential $18,000 ARR if converts
>
> This attribution data helps your team understand which ads are reaching which contacts. When reviewing TechCorp for deal review, they'll see that Jane found you through paid search — useful context for the sales conversation.
>
> I've also added her to the "Paid Acquisition" list in Attio for cohort tracking.

---

## Attio Tips for Ad Targeting

1. **Export enriched company lists to Google Customer Match.** Attio's auto-enrichment adds industry, size, and funding data. Use these segments for precision targeting.
2. **Use relationship scores for audience prioritization.** Strong relationships = warm audiences (retarget with conversion CTAs). Weak relationships = cold audiences (nurture with content).
3. **Track tech stack for product targeting.** If you sell integrations or complementary tools, query Attio's tech stack enrichment to find companies using the products you integrate with.
4. **Post-funding targeting is gold.** Companies that just raised are buying tools. Query Attio for recent funding events and run targeted campaigns to these companies within 30 days.
5. **Flexible lists = flexible audiences.** Attio's list system lets you create any segmentation you need. Each list can become an ad audience — maintain them as living documents.
6. **Write attribution back to Attio.** When a contact converts from an ad campaign, add the attribution data as a note. This closes the loop between ads and CRM.

---

## FAQ

### Is there an MCP for Attio CRM?
Yes — this repo. It pre-configures the Synter MCP server for Attio CRM management. Works with Amp, Cursor, VS Code, and Claude Desktop.

### Can I export Attio contacts to ad platforms?
Yes. The agent exports contacts with email addresses, hashes them for privacy, and uploads to Google Customer Match, Meta Custom Audiences, or LinkedIn Matched Audiences.

### Does this work with Attio's API?
Yes. The agent uses Attio's REST API to query people, companies, lists, notes, and custom objects.

### How is Attio different from HubSpot or Salesforce?
Attio has a more flexible data model (like Notion for CRM), built-in relationship intelligence, and automatic contact enrichment. It's popular with startups, VCs, and modern B2B teams who find traditional CRMs too rigid.

### Can the agent write data back to Attio?
Yes — the agent can create notes, update records, and manage list memberships. This enables conversion attribution write-back and audience tagging.

---

## Related Repos

- [hubspot-agent](https://github.com/Synter-Media-AI/hubspot-agent) — Traditional CRM integration
- [salesforce-agent](https://github.com/Synter-Media-AI/salesforce-agent) — Enterprise CRM
- [audience-sync-agent](https://github.com/Synter-Media-AI/audience-sync-agent) — Multi-platform audience sync
- [linkedin-ads-agent](https://github.com/Synter-Media-AI/linkedin-ads-agent) — B2B ABM campaigns
- [google-ads-agent](https://github.com/Synter-Media-AI/google-ads-agent) — Customer Match targeting
- [pipedrive-agent](https://github.com/Synter-Media-AI/pipedrive-agent) — Sales pipeline CRM

---

## License

MIT — see [LICENSE](LICENSE) for details.

Built by [Synter](https://syntermedia.ai) · [Get API Key](https://syntermedia.ai/developer) · [Documentation](https://syntermedia.ai/docs)
