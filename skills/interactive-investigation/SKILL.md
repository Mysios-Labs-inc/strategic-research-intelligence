---
name: interactive-investigation
description: Advanced browser-based investigation using Firecrawl's interactive sessions for login-protected content, form submissions, dynamic content extraction, and multi-step user journeys requiring persistent browser state
---

# Interactive Investigation

Conduct sophisticated investigations requiring browser interaction, form submissions, login authentication, and session persistence to access protected content and navigate complex user workflows.

## Core Capabilities

- **Persistent Browser Sessions**: Maintain login state and cookies across multiple operations
- **Form Interaction**: Fill forms, submit data, handle multi-step processes
- **Authentication Workflows**: Login to protected sites and maintain authenticated sessions
- **Dynamic Content Extraction**: Handle JavaScript-heavy sites with dynamic loading
- **Natural Language Control**: Direct browser actions using plain English commands

## Use Cases

### Protected Content Research
- **Industry Reports**: Access gated research reports and industry analyses
- **Financial Data**: Extract data from investor portals and financial platforms
- **Academic Resources**: Access journal articles and research databases
- **Government Data**: Navigate government portals and regulatory databases

### Complex User Journeys
- **Product Research**: Navigate product catalogs, pricing configurators, trial workflows
- **Competitive Analysis**: Access competitor tools, pricing pages, demo environments
- **Market Research**: Complete surveys, access market research platforms
- **Due Diligence**: Navigate complex corporate information systems

### Interactive Data Collection
- **Lead Generation**: Extract contact information from business directories
- **Event Research**: Gather attendee lists, speaker information from event platforms
- **Social Research**: Navigate social platforms for trend and sentiment analysis
- **Regulatory Research**: Access compliance databases and regulatory filings

## Parameters

- `objective` - Investigation goal and target information
- `start_url` - Initial URL or platform to begin investigation
- `session_type` - Session management ("persistent", "temporary", "authenticated")
- `credentials` - Authentication information (when provided by user)
- `interaction_steps` - Specific actions to perform in sequence
- `extraction_targets` - Data points to collect during navigation
- `timeout` - Maximum session duration and step timeouts

## Basic Usage

### Simple Form-based Research
```bash
# Extract data from a business directory
strategic-research-intelligence:interactive-investigation \
  objective="Gather contact information for fintech companies in NYC" \
  start_url="business-directory.com/search" \
  interaction_steps='[
    "fill search field with fintech NYC",
    "click search button",
    "navigate through result pages",
    "extract company contact information"
  ]' \
  session_type="temporary"
```

### Authenticated Content Access
```bash
# Research competitor pricing with trial account
strategic-research-intelligence:interactive-investigation \
  objective="Analyze competitor pricing tiers and features" \
  start_url="competitor.com/login" \
  session_type="authenticated" \
  interaction_steps='[
    "login with trial credentials",
    "navigate to pricing page",
    "explore feature comparisons",
    "extract pricing data and feature lists"
  ]' \
  extraction_targets='{
    "pricing_tiers": ["string"],
    "features_by_tier": {"tier": ["features"]},
    "trial_limitations": ["string"]
  }'
```

### Complex Multi-step Investigation
```bash
# Navigate government regulatory database
strategic-research-intelligence:interactive-investigation \
  objective="Research regulatory filings for specific industry" \
  start_url="sec.gov/edgar/search" \
  interaction_steps='[
    "select company search type",
    "enter company identifier",
    "filter by filing type 10-K",
    "access most recent filing",
    "navigate to risk factors section",
    "extract key risk disclosures"
  ]' \
  session_type="persistent" \
  timeout="30 minutes"
```

## Session Management

### Persistent Sessions
**Use for**: Long investigations, multi-site workflows, complex authentication
```yaml
Benefits:
  - Maintains state across multiple operations
  - Preserves authentication and cookies
  - Enables complex multi-step workflows
  - Reduces authentication overhead

Limitations:
  - Higher credit consumption
  - Session timeout considerations
  - State management complexity
```

### Temporary Sessions
**Use for**: Quick extractions, single-site operations, public content
```yaml
Benefits:
  - Lower cost per operation
  - Clean state for each investigation
  - Simple configuration
  - Faster startup time

Limitations:
  - No state preservation
  - Re-authentication required
  - Limited to single workflows
```

### Authenticated Sessions
**Use for**: Protected content, member portals, trial accounts, premium features
```yaml
Requirements:
  - Valid credentials (user-provided)
  - Platform support for automated login
  - Session persistence configuration
  - Logout handling for cleanup

Capabilities:
  - Access gated content and premium features
  - Navigate authenticated user interfaces
  - Extract data from member-only sections
  - Maintain compliance with terms of service
```

## Interaction Patterns

### Natural Language Commands
```yaml
Navigation:
  - "click the login button"
  - "navigate to the pricing page"
  - "scroll to the bottom of the page"
  - "go back to the previous page"

Form Interaction:
  - "fill the email field with test@example.com"
  - "select 'Enterprise' from the dropdown"
  - "check the 'agree to terms' checkbox"
  - "submit the contact form"

Content Extraction:
  - "extract all company names from the results"
  - "save the pricing table data"
  - "capture the contact information"
  - "collect the product feature list"

Conditional Logic:
  - "if login required, use provided credentials"
  - "navigate to next page if available"
  - "extract data only if content is loaded"
  - "retry search if no results found"
```

### Complex Workflow Example
```yaml
Lead Generation Workflow:
  Step 1: "navigate to business directory search page"
  Step 2: "fill industry field with 'artificial intelligence'"
  Step 3: "fill location field with 'San Francisco'"
  Step 4: "click search and wait for results to load"
  Step 5: "for each company result:"
    - "extract company name and website"
    - "click company profile link"
    - "extract contact information from profile"
    - "navigate back to results list"
  Step 6: "click next page if available, repeat extraction"
  Step 7: "compile all extracted data into structured format"
```

## Data Extraction Capabilities

### Structured Data Collection
```yaml
Contact Information:
  schema: {
    "contacts": [{
      "company": "string",
      "contact_person": "string",
      "email": "string",
      "phone": "string",
      "website": "string",
      "linkedin": "string"
    }]
  }

Product Features:
  schema: {
    "product_analysis": {
      "pricing_tiers": [{
        "tier_name": "string",
        "price": "string",
        "features": ["string"],
        "limitations": ["string"]
      }]
    }
  }

Market Intelligence:
  schema: {
    "market_data": {
      "companies": [{
        "name": "string",
        "size": "string",
        "industry": "string",
        "recent_news": ["string"],
        "key_personnel": ["string"]
      }]
    }
  }
```

### Dynamic Content Handling
- **JavaScript Rendering**: Full execution of client-side code
- **AJAX Loading**: Wait for dynamic content to load completely
- **Infinite Scroll**: Handle continuously loading content
- **Pop-up Handling**: Manage modals, overlays, and pop-ups
- **Form Validation**: Navigate client-side validation requirements

## Integration Workflows

### With AI Research Agent
```yaml
Combined Intelligence Workflow:
1. interactive-investigation (access protected competitor data)
2. ai-research-agent (analyze public information about same competitors)
3. Cross-reference findings for comprehensive analysis
4. Generate strategic intelligence report

Example: SaaS Competitive Analysis
- Interactive: Access competitor trial accounts, extract pricing/features
- AI Agent: Research public information, news, funding data
- Synthesis: Complete competitive positioning analysis
```

### With Social Media Automation
```yaml
Research-to-Content Pipeline:
1. interactive-investigation (gather exclusive insights from industry portals)
2. Extract unique data points not publicly available
3. social-media-manager:post-to-substack (create insider analysis article)
4. social-media-manager:create-for-linkedin (share exclusive insights)

Lead Generation to Outreach:
1. interactive-investigation (collect prospect information from directories)
2. Validate and enrich contact data
3. social-media-manager:engage-linkedin (strategic outreach to prospects)
```

## Advanced Features

### Session Recording and Replay
```yaml
Session Documentation:
  - Record all browser interactions for audit trail
  - Capture screenshots at key decision points
  - Log all data extraction operations
  - Generate step-by-step workflow documentation

Replay Capabilities:
  - Reproduce successful investigation workflows
  - Debug failed extraction attempts
  - Create template workflows for similar tasks
  - Train other team members on investigation processes
```

### Intelligent Error Recovery
```yaml
Adaptive Problem Solving:
  - Retry failed interactions with alternative approaches
  - Adapt to site changes and layout modifications
  - Handle unexpected pop-ups and interruptions
  - Graceful degradation when features are unavailable

Quality Assurance:
  - Validate extracted data for completeness
  - Cross-reference information across multiple pages
  - Detect and flag suspicious or inconsistent data
  - Maintain extraction confidence scores
```

### Multi-site Session Management
```yaml
Cross-platform Intelligence:
  - Maintain multiple authenticated sessions simultaneously
  - Transfer insights between different platforms
  - Correlate information across disparate sources
  - Manage complex multi-platform workflows

Example: Due Diligence Workflow
- Session 1: Company website and investor portal
- Session 2: LinkedIn for employee and network analysis
- Session 3: News and regulatory sites for recent developments
- Synthesis: Comprehensive due diligence report
```

## Security and Compliance

### Authentication Best Practices
- **Credential Security**: Never store or log authentication credentials
- **Session Cleanup**: Properly logout and clear sessions after use
- **Rate Limiting**: Respect site rate limits and avoid aggressive behavior
- **Terms Compliance**: Operate within platform terms of service

### Data Privacy
- **Personal Data**: Avoid collecting personally identifiable information
- **Data Minimization**: Extract only necessary information for objectives
- **Retention Policies**: Follow data retention and deletion requirements
- **Attribution**: Properly credit sources and respect intellectual property

### Ethical Investigation
- **Transparent Intent**: Operate with legitimate business purposes
- **Respectful Interaction**: Minimize site impact and server load
- **Legal Compliance**: Follow applicable laws and regulations
- **Professional Standards**: Maintain high ethical standards in research

## Cost and Performance

### Credit Usage Patterns
```yaml
Simple Form Interactions: 2-7 credits/minute
Complex Multi-step Workflows: 5-15 credits/minute
Authenticated Sessions: 10-25 credits/session setup + usage
Data-intensive Extractions: Variable based on content volume

Optimization Strategies:
- Plan workflows to minimize session time
- Use targeted extraction rather than full page capture
- Batch similar operations within single sessions
- Cache results to avoid duplicate extractions
```

### Performance Optimization
- **Concurrent Sessions**: Run multiple investigations in parallel when possible
- **Smart Navigation**: Use direct URLs when available instead of navigation
- **Selective Extraction**: Target specific data elements rather than full pages
- **Session Reuse**: Maintain sessions for related operations

## Error Handling

### Common Challenges and Solutions
```yaml
Authentication Failures:
  - Verify credentials and account status
  - Check for captcha or security challenges
  - Try alternative login methods
  - Implement retry logic with delays

Dynamic Content Issues:
  - Increase wait times for content loading
  - Use element visibility detection
  - Handle JavaScript errors gracefully
  - Implement alternative extraction methods

Site Changes:
  - Adapt to layout modifications automatically
  - Use fuzzy matching for element detection
  - Maintain multiple extraction strategies
  - Flag significant changes for human review
```

## Examples

### Business Directory Mining
```bash
strategic-research-intelligence:interactive-investigation \
  objective="Extract technology company contacts from directory" \
  start_url="techcrunch-directory.com" \
  interaction_steps='["search for AI companies", "navigate results", "extract contact data"]' \
  extraction_targets='{"companies": [{"name": "string", "email": "string", "website": "string"}]}'
```

### Competitor Trial Analysis
```bash
strategic-research-intelligence:interactive-investigation \
  objective="Analyze competitor features through trial access" \
  start_url="competitor.com/trial" \
  session_type="authenticated" \
  interaction_steps='["sign up for trial", "explore dashboard", "test key features", "analyze limitations"]' \
  timeout="45 minutes"
```

### Regulatory Data Extraction
```bash
strategic-research-intelligence:interactive-investigation \
  objective="Extract regulatory compliance requirements" \
  start_url="regulatory-portal.gov" \
  interaction_steps='["navigate to industry regulations", "filter by date range", "extract compliance requirements"]' \
  session_type="persistent"
```

### Market Research Survey
```bash
strategic-research-intelligence:interactive-investigation \
  objective="Complete market research survey for industry insights" \
  start_url="research-platform.com/survey/tech-trends" \
  interaction_steps='["complete demographic questions", "answer industry trend questions", "submit survey", "access results"]' \
  session_type="temporary"
```