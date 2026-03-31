---
name: trend-monitor
description: Monitor trending topics and breaking news across web sources using Firecrawl for real-time content discovery and analysis
---

# Trend Monitor

Monitor trending topics, breaking news, and emerging discussions across the web using Firecrawl's search and extraction capabilities.

## Use Cases

- **Real-time trend discovery** for reactive content creation
- **Breaking news monitoring** for timely responses
- **Topic emergence tracking** for early adoption opportunities
- **Industry buzz analysis** for strategic positioning

## Parameters

- `topic` - Main topic area to monitor (e.g., "AI", "politics", "technology")
- `timeframe` - Recency filter ("24h", "week", "month")
- `sources` - Specific domains to focus on (optional)
- `format` - Output format ("summary", "detailed", "urls")

## Basic Usage

```bash
# Monitor AI trends in last 24 hours
strategic-research-intelligence:trend-monitor topic="artificial intelligence" timeframe="24h"

# Breaking news in technology
strategic-research-intelligence:trend-monitor topic="breaking tech news" timeframe="6h" format="summary"

# Monitor specific sources
strategic-research-intelligence:trend-monitor topic="politics" sources="reuters.com,apnews.com" format="detailed"
```

## Integration with Social Media Automation

This skill pairs perfectly with social media automation for reactive content:

```yaml
Workflow Example:
1. strategic-research-intelligence:trend-monitor topic="tech trends" timeframe="24h"
2. Analyze trending topics for relevance to brand voice
3. social-media-manager:create-for-x args="reaction thread to [trend]"
4. social-media-manager:create-for-linkedin args="professional take on [trend]"
```

## Output Format

### Summary Format
```yaml
trending_topics:
  - title: "Topic Title"
    relevance_score: 0.85
    source_count: 15
    key_points: ["Point 1", "Point 2", "Point 3"]
    representative_url: "https://..."

  - title: "Another Topic"
    relevance_score: 0.72
    source_count: 8
    key_points: ["Point A", "Point B"]
    representative_url: "https://..."
```

### Detailed Format
```yaml
trend_analysis:
  topic: "Artificial Intelligence"
  timeframe: "24h"

  trending_themes:
    - theme: "AI Safety Regulations"
      momentum: "rising"
      sources: 12
      key_articles:
        - title: "Article Title"
          url: "https://..."
          summary: "Brief summary..."
          published: "2024-03-29T10:30:00Z"

  breaking_news:
    - headline: "Breaking News Title"
      urgency: "high"
      source: "Reuters"
      summary: "Brief summary..."

  discussion_volume:
    social_media: "high"
    news_coverage: "moderate"
    expert_commentary: "emerging"
```

## Implementation

Leverages the official Firecrawl plugin for search and extraction:

### Workflow Steps
1. **Discovery Phase**: Use official Firecrawl plugin for multi-pattern searches
   ```bash
   # News search with time filtering
   firecrawl:firecrawl-cli search "artificial intelligence" --sources news --tbs qdr:d --limit 20

   # Tech publication search
   firecrawl:firecrawl-cli search "AI developments" --sources web --limit 15

   # Academic source search
   firecrawl:firecrawl-cli search "AI research" --categories research --limit 10
   ```

2. **Content Extraction**: Scrape full content from trending URLs
   ```bash
   # Parallel content extraction
   firecrawl:firecrawl-cli scrape $url --only-main-content --format markdown
   ```

3. **Trend Analysis**: Process content for momentum and relevance scoring
4. **Intelligence Synthesis**: Generate strategic insights and recommendations
5. **Formatted Output**: Present results in actionable formats

### Integration Pattern
```yaml
trend-monitor skill (this plugin)
  ↓ calls
firecrawl:firecrawl-cli (official plugin)
  ↓ executes
firecrawl CLI commands
```

## Advanced Features

### Multi-Source Monitoring
Monitor trends across different source types:
- News sites (Reuters, AP, BBC)
- Tech publications (TechCrunch, Ars Technica, Wired)
- Social platforms (Reddit, Hacker News)
- Academic sources (arXiv, research institutions)

### Momentum Detection
Track how topics gain or lose momentum:
- **Emerging**: New discussions starting
- **Rising**: Growing attention and coverage
- **Peak**: Maximum coverage reached
- **Declining**: Interest waning

### Custom Filtering
Filter trends by:
- Relevance to brand voice
- Geographic focus
- Language preferences
- Source credibility scoring

## Error Handling

- **No trends found**: Returns empty result with suggested broader queries
- **API limits**: Implements backoff and retry logic
- **Source unavailable**: Skips failed sources, continues with available ones
- **Content extraction failure**: Falls back to search snippet content

## Best Practices

1. **Regular Monitoring**: Run every 2-4 hours for active trend tracking
2. **Topic Specificity**: Balance broad vs specific topic queries
3. **Source Diversity**: Include multiple source types for comprehensive coverage
4. **Relevance Filtering**: Focus on topics aligned with brand voice and expertise
5. **Integration Timing**: Use results immediately for maximum relevance

## Examples

### Technology Trend Monitoring
```bash
strategic-research-intelligence:trend-monitor topic="emerging technology trends" timeframe="24h" format="summary"
```

Expected output: 3-5 trending tech topics with relevance scores, source counts, and key discussion points.

### Breaking News Response
```bash
strategic-research-intelligence:trend-monitor topic="AI regulation news" timeframe="6h" format="detailed"
```

Expected output: Detailed analysis of recent AI regulation developments with full article summaries and expert commentary.

### Industry Buzz Analysis
```bash
strategic-research-intelligence:trend-monitor topic="startup funding rounds" timeframe="week" sources="techcrunch.com,crunchbase.com" format="detailed"
```

Expected output: Weekly funding trend analysis with specific deals, patterns, and industry implications.