# Cost Curve & Pricing Strategy
Leader feature: AI Claims Decision Support - AI assisted claims intake, analysis, and best-action recommendations
Filler feature: AI Claim summaries and insights
Killer feature and usage %: Processing of large volumes of claims documents and complex multimodal content like pdfs, images, forms, or handwritten or unstructured content. 30-50%.
Pricing strategy bundle or add-on: add-on as usage based.

## Cost Model
| Cost Category | Per-User/Month | Notes |
|--------------|----------------|-------|
| Inference (primary model) | $15 | Frontier model used for complex claim analysis, decision support, and reasoning. |
| Inference (cascading/triage) | $5 | Lower-cost model used for routine claim classification, summaries, and initial document review. |
| Infrastructure | $6 | Compute, orchestration, API processing, and system maintenance. |
| Data/storage | $2 | Storage and retrieval of claim documents, extracted data, and processing results. |
| Human-in-the-loop | $12 | Human review of low-confidence claims (below 50%) and complex exceptions. |
| **Total AI COGS** | \*\*$40\*\* | Estimated monthly AI cost per active user. |


\*Note: Illustrative planning estimates, not actual vendor quotes or measured operating costs.\*\
\
\## Cascading Strategy\
\<!-- Cheap model → frontier model routing logic -->\
\
\*\*Triage model:\*\* Lower-cost LLM used for initial document classification, data extraction, claim summaries, and straightforward claims processing.\
\
\*\*Frontier model:\*\* More advanced LLM used for complex claim analysis, conflicting evidence, beneficiary disputes, policy interpretation, and multi-step reasoning.\
\
\*\*Routing rule:\*\* \
\- Routine claims with clear documentation and straightforward policy requirements are processed using the lower-cost triage model.\
\- Complex claims, conflicting information, and cases requiring advanced reasoning are routed to the frontier model.\
\- Claims with confidence below 50% are automatically flagged and routed to a human claims specialist.\
\- Fraud indicators, beneficiary disputes, and high-risk exceptions require human review regardless of confidence score.\
\- The system must not approve or reject claims solely based on confidence scores.\
\
\*\*Expected cascade ratio:\*\* 70% triage model / 30% frontier model. Target is to process the majority of routine claims through lower-cost models while reserving more expensive models for complex scenarios.\
\
\## Pricing Model\
\
\*\*Current pricing:\*\* Existing enterprise platform licensing / subscription pricing. Specific current pricing to be determined based on the organization's existing commercial model.\
\
\*\*Proposed AI pricing:\*\* Base platform subscription with an additional usage-based fee for complex multimodal claims processing. Include a predefined monthly usage allowance with additional charges for claims exceeding the allowance.\
\
\*\*Model:\*\* Hybrid (seat-based + usage-based).\
\
\- Seat-based pricing covers AI Claims Decision Support and AI Claim Summaries and Insights.\
\- Usage-based pricing applies to high-volume document processing, multimodal extraction, and complex claims analysis.\
\- Additional usage charges apply when customers exceed their monthly processing allowance.\
\- Enterprise volume tiers provide discounted rates for higher processing volumes.\
\
\## Stress Tests\
\
\| Scenario | Impact on Margin | Response |\
\|----------|-----------------|----------|\
\| Inference costs 3x | Significant increase in AI COGS and reduced gross margin. | Increase cascading to route more routine claims through lower-cost models, optimize prompts, and introduce usage limits or additional processing fees. |\
\| Heaviest segment doubles | Increased document processing, multimodal inference, storage, and infrastructure costs. | Introduce volume-based pricing tiers, processing limits, and additional usage charges for high-volume customers. |\
\| Model provider raises prices 50% | Increased inference costs and reduced profitability. | Evaluate alternative model providers, optimize model selection, negotiate enterprise pricing, and adjust usage-based fees if necessary. |




## Cascading Strategy
<!-- Cheap model → frontier model routing logic -->

**Triage model:**
**Frontier model:**
**Routing rule:**
**Expected cascade ratio:**

## Pricing Model

**Current pricing:**
**Proposed AI pricing:**
**Model:** seat-based / usage-based / outcome-based / hybrid

## Stress Tests

| Scenario | Impact on Margin | Response |
|----------|-----------------|----------|
| Inference costs 3x | | |
| Heaviest segment doubles | | |
| Model provider raises prices 50% | | |

## Board One-Pager
<!-- Before/After: Old SaaS revenue vs. AI usage revenue for your product -->

**Before (traditional SaaS):**
**After (AI-enabled):**
**Net margin shift:**
