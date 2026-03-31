---
name: ai-research-agent
description: Autonomous AI-powered research using Firecrawl FIRE-1 agents for complex multi-step investigations, schema-driven data extraction, and intelligent source discovery across multiple sites and workflows
---

# AI Research Agent

Deploy autonomous AI agents (FIRE-1) to conduct complex, multi-step research investigations that navigate websites, extract structured data, and synthesize findings from multiple sources without human intervention.

## Core Capabilities

- **Autonomous Navigation**: AI agents independently browse and navigate complex websites
- **Schema-driven Extraction**: Extract structured JSON data using custom schemas
- **Multi-step Workflows**: Handle pagination, form submissions, and complex user journeys
- **Intelligent Source Discovery**: Dynamically find and evaluate relevant sources
- **Cross-source Synthesis**: Combine findings from multiple sites into coherent analysis

## Use Cases

### Strategic Intelligence
- **Market Research**: Autonomous competitive landscape analysis across multiple competitor sites
- **Due Diligence**: Comprehensive company research including financials, news, and partnerships
- **Industry Analysis**: Systematic analysis of industry players, trends, and market dynamics

### Content Research
- **Expert Discovery**: Find and analyze thought leaders, their content, and perspectives
- **Topic Exploration**: Deep dive into complex topics across academic, news, and industry sources
- **Fact Verification**: Cross-reference claims across authoritative sources with evidence tracking

### Competitive Intelligence
- **Product Analysis**: Compare features, pricing, and positioning across competitor sites
- **Content Strategy**: Analyze competitor content themes, frequency, and engagement patterns
- **Technology Tracking**: Monitor competitor tech stack, integrations, and platform changes

## Parameters

- `objective` - High-level research goal and success criteria
- `schema` - JSON schema defining the structure of extracted data
- `sources` - Starting points for investigation (domains, search terms, or specific URLs)
- `depth` - Investigation depth ("focused", "comprehensive", "exhaustive")
- `model` - Agent model ("spark-1-mini" for cost efficiency, "spark-1-pro" for accuracy)
- `constraints` - Ethical and scope boundaries for the investigation

## Advanced Usage

### Market Intelligence with Schema
```bash
# Comprehensive competitor analysis with structured output
strategic-research-intelligence:ai-research-agent \
  objective="Analyze SaaS competition in project management space" \
  schema='{
    "competitors": [{
      "company": "string",
      "pricing_model": "string",
      "key_features": ["string"],
      "target_market": "string",
      "recent_updates": ["string"],
      "funding_stage": "string"
    }]
  }' \
  sources="asana.com,monday.com,notion.so" \
  depth="comprehensive" \
  model="spark-1-pro"
```

### Expert Discovery and Analysis
```bash
# Find and analyze thought leaders in specific domain
strategic-research-intelligence:ai-research-agent \
  objective="Identify top AI governance experts and their current positions" \
  schema='{
    "experts": [{
      "name": "string",
      "affiliation": "string",
      "expertise_areas": ["string"],
      "recent_publications": ["string"],
      "key_positions": ["string"],
      "contact_info": "string"
    }]
  }' \
  sources="search:AI governance experts 2024" \
  depth="focused" \
  model="spark-1-mini"
```

### Multi-source Fact Verification
```bash
# Verify claims across multiple authoritative sources
strategic-research-intelligence:ai-research-agent \
  objective="Verify claims about quantum computing breakthrough" \
  schema='{
    "verification": {
      "claim": "string",
      "verdict": "verified|disputed|inconclusive",
      "evidence": [{
        "source": "string",
        "statement": "string",
        "credibility": "high|medium|low",
        "date": "string"
      }],
      "consensus": "string"
    }
  }' \
  sources="nature.com,science.org,arxiv.org,ieee.org" \
  depth="comprehensive"
```

## Schema Design Patterns

### Company Intelligence Schema
```json
{
  "company_profile": {
    "basic_info": {
      "name": "string",
      "founded": "string",
      "headquarters": "string",
      "employee_count": "string",
      "industry": "string"
    },
    "financials": {
      "revenue": "string",
      "funding_stage": "string",
      "recent_funding": {
        "amount": "string",
        "date": "string",
        "investors": ["string"]
      }
    },
    "products": [{
      "name": "string",
      "description": "string",
      "pricing": "string",
      "target_market": "string"
    }],
    "competitive_position": {
      "strengths": ["string"],
      "differentiators": ["string"],
      "market_position": "string"
    }
  }
}
```

### Content Analysis Schema
```json
{
  "content_analysis": {
    "themes": [{
      "topic": "string",
      "frequency": "number",
      "sentiment": "positive|neutral|negative",
      "key_points": ["string"]
    }],
    "publishing_patterns": {
      "frequency": "string",
      "optimal_times": ["string"],
      "popular_formats": ["string"]
    },
    "engagement_insights": {
      "high_performing_content": ["string"],
      "audience_preferences": ["string"],
      "content_gaps": ["string"]
    }
  }
}
```

### Expert Analysis Schema
```json
{
  "expert_analysis": {
    "expert_profile": {
      "name": "string",
      "credentials": ["string"],
      "affiliations": ["string"],
      "expertise_areas": ["string"]
    },
    "thought_leadership": {
      "key_positions": ["string"],
      "recent_content": [{
        "title": "string",
        "url": "string",
        "summary": "string",
        "publication_date": "string"
      }],
      "influence_metrics": {
        "citation_count": "string",
        "media_mentions": "string",
        "social_following": "string"
      }
    }
  }
}
```

## Agent Model Selection

### Spark-1-Mini (Cost Efficient)
- **Best for**: Routine research, structured data extraction, known domains
- **Cost**: ~60% savings vs Pro model
- **Accuracy**: High for straightforward tasks
- **Speed**: Faster execution
- **Use cases**: Regular competitive monitoring, content analysis, fact-checking

### Spark-1-Pro (High Accuracy)
- **Best for**: Complex analysis, ambiguous domains, critical decisions
- **Cost**: Premium pricing for maximum accuracy
- **Accuracy**: Highest available for complex reasoning
- **Speed**: Slower but more thorough
- **Use cases**: Strategic intelligence, expert discovery, market research

## Multi-step Workflow Examples

### Competitive Intelligence Pipeline
```yaml
Objective: "Complete competitive analysis of fintech lending platforms"

Step 1: Market Discovery
- Agent searches for "fintech lending platforms 2024"
- Identifies top 10 competitors automatically
- Creates target list with company domains

Step 2: Deep Site Analysis
- Agent navigates each competitor site
- Extracts pricing, features, positioning
- Gathers recent news and funding information

Step 3: Cross-source Verification
- Agent searches news sources for each competitor
- Verifies claims from company sites
- Gathers third-party analysis and reviews

Step 4: Synthesis & Analysis
- Agent combines all findings into structured output
- Identifies patterns, gaps, and opportunities
- Generates competitive positioning insights
```

### Expert Research Workflow
```yaml
Objective: "Identify and analyze climate policy experts"

Step 1: Expert Discovery
- Agent searches academic databases, think tanks
- Identifies experts based on publication frequency and citations
- Gathers basic profiles and affiliations

Step 2: Content Analysis
- Agent analyzes recent publications and positions
- Extracts key arguments and policy recommendations
- Maps expert positions across policy spectrum

Step 3: Influence Assessment
- Agent searches for media mentions and citations
- Analyzes social media presence and engagement
- Maps network connections between experts

Step 4: Position Synthesis
- Agent synthesizes expert consensus and disagreements
- Identifies emerging trends in expert thinking
- Maps policy position evolution over time
```

## Integration with Social Media Automation

### Research-to-Content Pipeline
```yaml
Content Creation Enhancement:
1. ai-research-agent (gather expert insights on topic)
2. Extract key findings and unique angles
3. social-media-manager:post-to-substack (create expert-backed article)
4. social-media-manager:create-for-linkedin (share insights)

Strategic Positioning:
1. ai-research-agent (analyze competitor positioning)
2. Identify differentiation opportunities
3. social-media-manager:create-for-x (position against gaps)
4. Track competitive responses over time
```

### Expert Engagement Workflow
```yaml
Relationship Building:
1. ai-research-agent (discover thought leaders in domain)
2. Analyze their content themes and positions
3. social-media-manager:engage-linkedin (thoughtful engagement)
4. social-media-manager:like-partner-posts (support their content)
```

## Output Formats

### Structured Intelligence Report
```yaml
research_intelligence:
  objective: "Original research objective"
  methodology: "Agent approach and source strategy"

  key_findings: [
    {
      finding: "Primary insight discovered",
      confidence: 0.95,
      evidence_sources: 8,
      supporting_data: "Quantitative or qualitative support"
    }
  ]

  structured_data: {
    # Custom schema output here
  }

  source_analysis: {
    total_sources: 25,
    source_types: ["company_sites", "news", "academic", "social"],
    credibility_distribution: {high: 15, medium: 8, low: 2},
    geographic_coverage: ["US", "EU", "Asia"],
    temporal_coverage: "2023-2024"
  }

  limitations: [
    "Access restrictions encountered",
    "Data gaps in specific areas"
  ]

  recommendations: {
    for_decision_making: ["Strategic recommendation 1", "Tactical advice 2"],
    for_further_research: ["Deep dive area 1", "Validation need 2"]
  }
```

### Agent Execution Log
```yaml
agent_workflow:
  execution_summary: {
    total_steps: 12,
    successful_navigations: 45,
    data_extraction_points: 38,
    synthesis_operations: 3,
    total_execution_time: "18 minutes"
  }

  step_breakdown: [
    {
      step: 1,
      action: "Initial source discovery",
      result: "Found 15 relevant competitor sites",
      confidence: 0.88
    },
    {
      step: 2,
      action: "Deep site analysis on competitor1.com",
      result: "Extracted pricing and feature data",
      confidence: 0.92
    }
  ]

  quality_metrics: {
    schema_compliance: 0.96,
    data_completeness: 0.84,
    source_diversity: 0.91,
    cross_validation_rate: 0.78
  }
```

## Error Handling & Resilience

### Adaptive Problem Solving
- **Site Navigation Failures**: Agent tries alternative paths and fallback approaches
- **Schema Extraction Errors**: Agent adapts extraction strategy based on site structure
- **Source Access Issues**: Agent automatically finds alternative sources for same information
- **Data Quality Problems**: Agent validates findings across multiple sources

### Quality Assurance
- **Cross-source Validation**: Agent verifies key findings across multiple independent sources
- **Confidence Scoring**: Each extracted data point includes confidence assessment
- **Bias Detection**: Agent identifies potential bias in sources and accounts for it
- **Completeness Tracking**: Agent monitors schema fulfillment and identifies gaps

## Best Practices

### Objective Setting
1. **Clear Success Criteria**: Define what constitutes successful research completion
2. **Scope Boundaries**: Set ethical and practical limits for investigation
3. **Quality Standards**: Specify minimum confidence and validation requirements
4. **Time Constraints**: Balance thoroughness with execution speed

### Schema Design
1. **Progressive Complexity**: Start simple, add detail as needed
2. **Validation Fields**: Include confidence and source tracking in schemas
3. **Flexible Structure**: Allow for optional fields and nested arrays
4. **Business Alignment**: Design schemas to match decision-making needs

### Model Selection
1. **Task Matching**: Use mini for routine work, pro for complex analysis
2. **Cost Management**: Monitor credit usage and optimize model selection
3. **Accuracy Requirements**: Match model capability to decision criticality
4. **Performance Testing**: Benchmark model performance for your specific use cases

## Advanced Configuration

### Ethical Constraints
```yaml
research_boundaries:
  respect_robots_txt: true
  avoid_personal_data: true
  respect_rate_limits: true
  attribution_required: true

content_restrictions:
  no_proprietary_data: true
  respect_copyright: true
  avoid_confidential_info: true

behavioral_guidelines:
  transparent_agent_identity: true
  respectful_interaction: true
  minimal_site_impact: true
```

### Performance Optimization
```yaml
efficiency_settings:
  parallel_processing: true
  intelligent_caching: true
  adaptive_depth: true
  result_deduplication: true

cost_optimization:
  model_selection_strategy: "adaptive"
  early_termination_criteria: true
  result_quality_thresholds: true
  credit_usage_monitoring: true
```

## Cost Considerations

### Credit Usage Patterns
- **Simple Research**: 100-500 credits for basic company analysis
- **Comprehensive Analysis**: 1,000-2,500 credits for multi-source investigation
- **Expert Discovery**: 500-1,200 credits for thought leader identification
- **Market Intelligence**: 2,000-5,000 credits for full competitive analysis

### Optimization Strategies
- **Progressive Research**: Start with mini model, upgrade to pro only when needed
- **Smart Caching**: Leverage agent memory to avoid redundant operations
- **Targeted Schemas**: Request only necessary data to reduce processing time
- **Batch Operations**: Combine related research objectives for efficiency

## Examples

### SaaS Market Research
```bash
strategic-research-intelligence:ai-research-agent \
  objective="Analyze project management SaaS market positioning" \
  schema='{"competitors": [{"company": "string", "positioning": "string", "pricing": "string", "features": ["string"]}]}' \
  sources="asana.com,monday.com,clickup.com,notion.so" \
  depth="comprehensive"
```

### Expert Thought Leadership Analysis
```bash
strategic-research-intelligence:ai-research-agent \
  objective="Map AI safety expert positions on regulation" \
  schema='{"experts": [{"name": "string", "position_summary": "string", "key_arguments": ["string"], "policy_recommendations": ["string"]}]}' \
  sources="search:AI safety experts regulation 2024" \
  depth="focused"
```

### Startup Due Diligence
```bash
strategic-research-intelligence:ai-research-agent \
  objective="Research fintech startup for potential partnership" \
  schema='{"company_analysis": {"financials": {}, "products": [], "market_position": "string", "risk_factors": ["string"]}}' \
  sources="company-site.com,crunchbase.com,news-sources" \
  depth="exhaustive" \
  model="spark-1-pro"
```