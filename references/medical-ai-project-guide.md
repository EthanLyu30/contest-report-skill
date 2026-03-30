# Medical AI Project Guide

Use this file when the project involves medical images, annotation workflows, model-assisted labeling, or sensitive data.

## Minimum Topics To Cover

### 1. Workflow Roles

Name the real actors and their responsibilities, for example:

- data uploader
- annotator
- reviewer or expert
- administrator
- model service

The report should show who can create tasks, label images, review results, export data, and manage permissions.

### 2. Data Lifecycle

State clearly:

- what image types are supported
- how data is uploaded and stored
- whether patient identifiers are removed or masked
- who can view or export the data
- whether logs or operation histories are kept

### 3. Human In The Loop

If AI assists the process, make the boundary explicit:

- AI suggests annotations, but humans confirm or reject them
- reviewers can revise low-confidence predictions
- uncertain cases trigger manual review
- exporting final labels requires a confirmed state

Do not describe the model as if it replaces human judgment unless the project truly does that and the claim can be defended.

### 4. Model Or Algorithm Boundaries

Explain:

- what the model is responsible for
- what input it receives
- what output it produces
- when fallback behavior is used
- how errors surface to the user

Good examples:

- lesion segmentation suggestion
- bounding box proposal
- classification-assisted triage
- automatic pre-labeling for later manual correction

### 5. Metrics

Choose metrics that match the project rather than forcing generic ones.

Possible metrics:

- average annotation time per image
- annotation efficiency improvement
- review turnaround time
- model-assisted acceptance rate
- overlap or consistency metrics for segmentation tasks
- inter-annotator consistency
- platform response time for common operations

### 6. Risk And Privacy

At contest-report level, usually a concise explanation is enough:

- role-based access control
- de-identification or anonymization
- secure storage and transmission
- export permissions
- operation logging

If the user wants a stronger security section, pair this skill with `security-threat-model`.

## Where To Use These Ideas

- `需求分析`: practical significance, target users, privacy-sensitive context
- `概要设计`: roles, modules, trust boundaries, service decomposition
- `详细设计`: data flow, review flow, database tables, model interaction, fallback
- `测试报告`: efficiency, consistency, and accuracy related metrics
- `项目总结`: practical value, limitations, and future optimization
