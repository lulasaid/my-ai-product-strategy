# Kill Switch Audit

## Vendor Dependency Assessment

| Dimension | Current State | Risk Level | 48-Hour Action |
|-----------|--------------|------------|---------------|
| **Provider** | Primary Gen AI capabilities depend on one preferred model/provider | H | Maintain pre-approved backup model/provider and validate that the same core claims use cases can run on it|
| **Abstraction** | Some claims logic, prompts, workflows, and integrations may be tied directly to primary model implementation. | H  | Model needs to be placed behind a common API/service layer so the claims application calls an internal AI service rather than a specific vendor.|
| **Routing** | Requests go primarily to one model rather than dynamically selecting the best model based on task, cost, risk or availability. | M  | Create routing rules so tasks like doc extraction, summaries, and reasoning can be sent to different models|
| **Eval** |Understand desired outcomes need to be formalized. | M | Create standard eval set and require replacement models to meet threshholds for accuracy, latency, compliance, etc.|

## Portability Score
*Partial** 
<!-- proprietary data for claims, domain context, workflows -->

## If [primary vendor] doubles pricing tomorrow: Route high volume or low complexity claims to the approved backup model while keeping higher-value reasoning tasks on the primary model until cost/performance evaluations support broader migration.
<!-- What's your 48-hour response? -->

## If [primary vendor] ships a competing product:Move model workloads to the secondary provider while retaining proprietary claims data, business rules, workflows, and feedback loops as the differentiated intelligence layer.
<!-- What's defensible that they can't replicate? -->
