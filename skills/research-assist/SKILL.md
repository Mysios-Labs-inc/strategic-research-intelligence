---
name: research-assist
description: Comprehensive web research using Firecrawl for in-depth content creation, fact-checking, and multi-source analysis
---

# Research Assist

Conduct comprehensive web research using Firecrawl's extraction capabilities to gather authoritative sources, verify facts, and build evidence-based content foundations.

## Use Cases

- **Long-form content research** for articles and deep-dive analysis
- **Fact verification** and source validation
- **Multi-perspective analysis** on complex topics
- **Academic and professional research** support

## Parameters

- `topic` - Research topic or question
- `depth` - Research depth ("quick", "standard", "comprehensive")
- `source_types` - Types of sources to prioritize ("news", "academic", "expert", "mixed")
- `perspective` - Analysis angle ("balanced", "pro", "con", "comparative")
- `output` - Output format ("summary", "citations", "full_analysis")

## Basic Usage

```bash
# Quick research on AI governance
strategic-research-intelligence:research-assist topic="AI governance frameworks" depth="quick" output="summary"

# Comprehensive analysis with academic sources
strategic-research-intelligence:research-assist topic="climate change policy effectiveness" depth="comprehensive" source_types="academic" output="full_analysis"

# Fact-checking specific claims
strategic-research-intelligence:research-assist topic="verify: renewable energy costs 2024" depth="standard" source_types="expert" output="citations"
```

## Integration with Content Creation

Perfect for feeding research into content creation workflows:

```yaml
Content Creation Workflow:
1. strategic-research-intelligence:research-assist topic="quantum computing breakthroughs" depth="standard"
2. Analyze findings and identify key insights
3. social-media-manager:substack-writer args="create article with research findings"
4. social-media-manager:create-for-linkedin args="professional summary of findings"
```

## Research Depth Levels

### Quick (5-10 sources)
- **Time**: ~2-3 minutes
- **Sources**: Top news articles and expert opinions
- **Output**: Key points and basic context
- **Use case**: Trending topic responses, quick fact-checks

### Standard (15-25 sources)
- **Time**: ~5-7 minutes
- **Sources**: News, expert analysis, some academic
- **Output**: Comprehensive overview with multiple perspectives
- **Use case**: Regular content creation, informed commentary

### Comprehensive (30-50 sources)
- **Time**: ~10-15 minutes
- **Sources**: Academic papers, expert analysis, news, official reports
- **Output**: In-depth analysis with citations and methodology
- **Use case**: Major articles, policy analysis, complex topics

## Source Type Priorities

### News Sources
- **Focus**: Current events and breaking developments
- **Examples**: Reuters, AP, BBC, WSJ, NYT
- **Best for**: Timely topics, policy changes, industry news

### Academic Sources
- **Focus**: Peer-reviewed research and scholarly analysis
- **Examples**: PubMed, arXiv, university publications
- **Best for**: Scientific topics, evidence-based arguments

### Expert Sources
- **Focus**: Professional analysis and industry expertise
- **Examples**: Think tanks, industry reports, expert blogs
- **Best for**: Strategic insights, trend analysis, technical topics

### Mixed Sources
- **Focus**: Balanced perspective across source types
- **Strategy**: Combine news, academic, and expert sources
- **Best for**: Complex topics requiring multiple viewpoints

## Output Formats

### Summary Format
```yaml
research_summary:
  topic: "AI Governance Frameworks"
  key_findings:
    - finding: "EU AI Act sets global precedent"
      confidence: "high"
      sources: 8

    - finding: "Industry self-regulation insufficient"
      confidence: "medium"
      sources: 5

  perspectives:
    regulatory: "Strict governance needed for safety"
    industry: "Innovation-friendly approaches preferred"
    academic: "Evidence-based policy development critical"

  knowledge_gaps:
    - "Long-term economic impacts unclear"
    - "Cross-border enforcement mechanisms undefined"
```

### Citations Format
```yaml
citations:
  primary_sources:
    - title: "EU AI Act: Comprehensive Analysis"
      author: "European Commission"
      url: "https://..."
      relevance: 0.95
      credibility: "government"
      key_quote: "Significant regulatory quote..."

    - title: "Industry Response to AI Regulation"
      author: "Tech Industry Association"
      url: "https://..."
      relevance: 0.87
      credibility: "industry"
      key_quote: "Industry perspective quote..."

  supporting_sources: [...]

  fact_checks:
    - claim: "EU AI Act applies globally"
      verdict: "partially_true"
      evidence: "Applies to EU market participation"
```

### Full Analysis Format
```yaml
full_analysis:
  executive_summary: "Comprehensive overview paragraph"

  methodology:
    sources_searched: 45
    sources_analyzed: 32
    search_strategy: "systematic keyword expansion"
    bias_considerations: "industry vs regulatory perspectives"

  detailed_findings:
    section_1:
      title: "Regulatory Landscape"
      key_points: [...]
      evidence: [...]
      contradictions: [...]

    section_2:
      title: "Industry Impact"
      key_points: [...]
      evidence: [...]

  synthesis:
    consensus_areas: [...]
    contested_areas: [...]
    evidence_gaps: [...]

  recommendations:
    for_content: "How to use these findings"
    for_further_research: "Areas needing deeper investigation"
```

## Advanced Features

### Multi-Hop Research
Follow research threads through multiple layers:
1. **Initial Search**: Broad topic exploration
2. **Deep Dive**: Follow promising leads from initial results
3. **Verification**: Cross-reference claims across sources
4. **Synthesis**: Combine findings into coherent analysis

### Bias Detection
Identify potential bias in sources:
- **Financial interests**: Funding sources and conflicts
- **Political alignment**: Editorial perspectives
- **Methodology concerns**: Research design issues
- **Source diversity**: Geographic and demographic representation

### Fact Verification
Systematic fact-checking process:
- **Claim identification**: Extract verifiable statements
- **Source triangulation**: Multiple independent confirmations
- **Authority assessment**: Source credibility evaluation
- **Recency validation**: Information currency verification

### Citation Management
Proper attribution and source tracking:
- **URL preservation**: Original source links maintained
- **Quote attribution**: Direct quotes with context
- **Source metadata**: Publication dates, authors, credentials
- **Relevance scoring**: Source importance to research question

## Integration Patterns

### With Social Media Automation
```yaml
Research → Content Pipeline:
1. strategic-research-intelligence:research-assist (gather evidence)
2. Content synthesis and analysis
3. social-media-manager:post-to-substack (publish analysis)
4. social-media-manager:create-for-x (share key insights)
```

### With Trend Monitoring
```yaml
Trend → Research → Response:
1. strategic-research-intelligence:trend-monitor (identify trends)
2. strategic-research-intelligence:research-assist (deep dive on trending topics)
3. social-media-manager:create-for-linkedin (informed response)
```

## Best Practices

1. **Clear Research Questions**: Define specific, answerable questions
2. **Source Diversity**: Include multiple perspectives and source types
3. **Fact Verification**: Cross-reference claims across sources
4. **Bias Awareness**: Acknowledge limitations and potential biases
5. **Citation Standards**: Maintain proper attribution throughout
6. **Synthesis Focus**: Combine rather than just aggregate information

## Error Handling

- **Limited sources found**: Suggests query modifications or alternative angles
- **Contradictory information**: Flags conflicts and provides multiple perspectives
- **Low-quality sources**: Filters out unreliable sources, focuses on credible ones
- **Access restrictions**: Works around paywalls and access limitations when possible

## Examples

### Technology Policy Research
```bash
strategic-research-intelligence:research-assist topic="impact of GDPR on AI development" depth="comprehensive" source_types="mixed" output="full_analysis"
```

### Quick Fact Check
```bash
strategic-research-intelligence:research-assist topic="verify: ChatGPT usage statistics 2024" depth="quick" output="citations"
```

### Balanced Analysis
```bash
strategic-research-intelligence:research-assist topic="nuclear energy vs renewables" depth="standard" perspective="comparative" output="summary"
```