---
name: intelligence-monitor
description: Real-time monitoring and change detection using Firecrawl for competitive intelligence, content tracking, pricing surveillance, and automated alerting on website changes, news developments, and market shifts
---

# Intelligence Monitor

Continuous monitoring and change detection across websites, competitor platforms, and information sources with automated alerting and trend analysis for real-time competitive intelligence.

## Core Capabilities

- **Change Detection**: Git-diff style monitoring of website content and structure changes
- **Competitive Surveillance**: Automated tracking of competitor pricing, features, and messaging
- **News Monitoring**: Real-time tracking of industry news, company mentions, and market developments
- **Automated Alerting**: Webhook-based notifications for significant changes and developments
- **Trend Analysis**: Pattern recognition in monitored changes and market movements

## Use Cases

### Competitive Intelligence
- **Pricing Surveillance**: Monitor competitor pricing changes, promotions, and new offerings
- **Feature Tracking**: Track new product launches, feature updates, and capability additions
- **Messaging Analysis**: Monitor changes in positioning, marketing campaigns, and brand messaging
- **Strategic Moves**: Alert on partnership announcements, executive changes, and strategic shifts

### Market Intelligence
- **Industry News**: Continuous monitoring of relevant news sources and industry publications
- **Regulatory Changes**: Track regulatory updates, policy changes, and compliance requirements
- **Market Trends**: Monitor trending topics, emerging technologies, and market sentiment shifts
- **Investment Activity**: Track funding announcements, IPOs, and M&A activity in your space

### Operational Intelligence
- **Content Monitoring**: Track changes to key customer-facing pages and documentation
- **Service Status**: Monitor competitor service status pages and outage notifications
- **Technology Changes**: Track technology stack changes, API updates, and platform modifications
- **Social Sentiment**: Monitor social media sentiment and conversation trends

## Parameters

- `targets` - URLs, domains, or search queries to monitor
- `monitor_type` - Type of monitoring ("content_changes", "pricing", "news", "social")
- `frequency` - Monitoring frequency ("hourly", "daily", "weekly", "real-time")
- `change_threshold` - Sensitivity level for change detection (0.1-1.0)
- `alert_channels` - Notification methods ("webhook", "email", "slack")
- `baseline_period` - Historical period for trend comparison

## Monitoring Types

### Content Change Monitoring
```bash
# Monitor competitor website for content changes
strategic-research-intelligence:intelligence-monitor \
  targets="competitor.com/features,competitor.com/pricing" \
  monitor_type="content_changes" \
  frequency="daily" \
  change_threshold="0.2" \
  alert_channels="webhook:https://your-webhook.com/alerts"
```

### Pricing Surveillance
```bash
# Track pricing changes across multiple competitors
strategic-research-intelligence:intelligence-monitor \
  targets="saas-competitor-1.com/pricing,saas-competitor-2.com/pricing" \
  monitor_type="pricing" \
  frequency="hourly" \
  change_threshold="0.1" \
  alert_channels="slack:pricing-alerts"
```

### News and Trend Monitoring
```bash
# Monitor industry news and company mentions
strategic-research-intelligence:intelligence-monitor \
  targets="search:fintech regulation 2024,search:competitor-name news" \
  monitor_type="news" \
  frequency="real-time" \
  alert_channels="webhook:https://alerts.yourapp.com/news"
```

### Social Sentiment Tracking
```bash
# Monitor social media sentiment and discussions
strategic-research-intelligence:intelligence-monitor \
  targets="search:your-company-name social,search:industry-hashtag" \
  monitor_type="social" \
  frequency="hourly" \
  baseline_period="30days" \
  alert_channels="email:marketing@yourcompany.com"
```

## Change Detection Capabilities

### Content Analysis
```yaml
Change Types Detected:
  - Text additions and deletions
  - Structural HTML modifications
  - Image and media updates
  - Link changes and redirects
  - Meta information updates
  - New page sections or features

Analysis Granularity:
  - Page-level changes (entire page modified)
  - Section-level changes (specific content areas)
  - Element-level changes (individual components)
  - Word-level changes (precise text modifications)
```

### Visual Change Detection
```yaml
Visual Monitoring:
  - Screenshot comparison for layout changes
  - Color scheme and branding modifications
  - New visual elements and design updates
  - Mobile vs desktop layout differences
  - Accessibility improvements tracking

Image Analysis:
  - Logo updates and branding changes
  - Product image modifications
  - Infographic and chart updates
  - Marketing creative variations
```

### Structured Data Monitoring
```yaml
Schema-based Tracking:
  - Product pricing and availability
  - Team member additions/changes
  - Contact information updates
  - Service offerings modifications
  - Technical specification changes

Database Integration:
  - Historical change logging
  - Trend analysis over time
  - Change frequency patterns
  - Impact assessment scoring
```

## Alert Configuration

### Smart Alerting
```yaml
Intelligent Filtering:
  - Significance scoring for changes
  - Noise reduction for minor updates
  - Context-aware change classification
  - Priority ranking based on business impact

Alert Types:
  - Critical: Major pricing changes, new product launches
  - Important: Content updates, feature additions
  - Informational: Minor text changes, formatting updates
  - Trend: Pattern recognition in change frequency
```

### Multi-channel Notifications
```yaml
Webhook Integration:
  format: JSON payload with change details
  includes: before/after comparison, confidence score
  customizable: filter rules and payload structure

Email Alerts:
  format: HTML with visual diff presentation
  scheduling: immediate, digest, or scheduled summaries
  segmentation: different alerts for different stakeholders

Slack Integration:
  format: Rich message with action buttons
  channels: route to appropriate team channels
  interactive: approve/dismiss/investigate options

Custom Integration:
  apis: Push to custom systems and databases
  formats: XML, JSON, or custom payload structures
  authentication: API keys, OAuth, or webhook secrets
```

## Competitive Intelligence Workflows

### Comprehensive Competitor Monitoring
```yaml
Multi-faceted Surveillance:
  1. Website Content: Monitor all competitor pages for changes
  2. Pricing Intelligence: Track pricing, promotions, and feature tiers
  3. News Monitoring: Track company mentions and announcements
  4. Social Listening: Monitor competitor social media activity
  5. Technology Tracking: Monitor tech stack and infrastructure changes

Integration Pipeline:
  1. intelligence-monitor (detect competitor changes)
  2. ai-research-agent (analyze significance of changes)
  3. competitive-analysis (update competitive intelligence database)
  4. social-media-manager:create-for-linkedin (strategic response content)
```

### Market Intelligence Dashboard
```yaml
Real-time Market Pulse:
  - Industry news sentiment analysis
  - Competitor activity heat map
  - Pricing trend visualization
  - Technology adoption tracking
  - Investment activity monitoring

Automated Insights:
  - Weekly competitor activity summaries
  - Pricing trend analysis reports
  - Market shift early warning system
  - Strategic opportunity identification
```

## Advanced Monitoring Features

### Pattern Recognition
```yaml
Trend Detection:
  - Pricing cycle identification (seasonal patterns)
  - Content update frequency analysis
  - Competitive response timing
  - Market announcement clustering

Anomaly Detection:
  - Unusual change frequency spikes
  - Out-of-pattern pricing modifications
  - Unexpected content removals
  - Suspicious activity patterns

Predictive Analytics:
  - Forecast competitor moves based on patterns
  - Identify early indicators of major changes
  - Market timing prediction for announcements
  - Competitive response likelihood scoring
```

### Historical Intelligence
```yaml
Change History Tracking:
  - Complete audit trail of all detected changes
  - Before/after snapshots with timestamps
  - Change frequency and pattern analysis
  - Rollback and revert detection

Trend Analysis:
  - Long-term competitive positioning shifts
  - Pricing strategy evolution
  - Content strategy development
  - Market response patterns

Intelligence Reports:
  - Monthly competitor activity summaries
  - Quarterly market intelligence briefings
  - Annual competitive landscape analysis
  - Strategic intelligence dashboards
```

## Integration with Social Media Automation

### Reactive Content Strategy
```yaml
Intelligence-to-Content Pipeline:
1. intelligence-monitor (detect significant competitor change)
2. Evaluate strategic implications of change
3. social-media-manager:create-for-x (rapid response content)
4. social-media-manager:post-to-substack (detailed analysis)

Example: Competitor Pricing Change
- Monitor detects 30% price reduction from competitor
- Alert triggers analysis of competitive implications
- Generate content positioning your value proposition
- Deploy across social channels within 2 hours
```

### Proactive Positioning
```yaml
Trend-based Content Planning:
1. intelligence-monitor (identify emerging market trends)
2. trend-monitor (validate trend significance)
3. research-assist (deep research on trend implications)
4. social-media-manager:post-to-substack (thought leadership content)

Market Opportunity Response:
1. intelligence-monitor (detect competitor service gaps)
2. ai-research-agent (analyze market opportunity)
3. social-media-manager:create-for-linkedin (position against gap)
```

## Output Formats

### Change Detection Report
```yaml
change_summary:
  target: "competitor.com/pricing"
  detection_time: "2024-03-29T10:30:00Z"
  change_type: "pricing_modification"
  significance_score: 0.85

changes_detected: [
    {
      section: "Enterprise Plan",
      change_type: "price_reduction",
      before: "$299/month",
      after: "$199/month",
      change_percentage: -33.4,
      confidence: 0.96
    },
    {
      section: "Feature Comparison",
      change_type: "feature_addition",
      before: "Basic Analytics",
      after: "Advanced Analytics with AI Insights",
      confidence: 0.92
    }
  ]

business_impact:
  competitive_threat_level: "high"
  recommended_actions: [
    "Review your pricing strategy",
    "Analyze competitive positioning",
    "Prepare counter-messaging"
  ]
  estimated_market_impact: "significant"

trend_analysis:
  similar_changes_pattern: "3 price reductions in last 90 days"
  market_context: "Industry-wide pricing pressure"
  timing_analysis: "Change made Friday evening"
```

### Intelligence Alert
```yaml
alert_notification:
  alert_id: "intel-2024-03-29-001"
  priority: "critical"
  category: "competitive_pricing"

  summary: "Major competitor reduced enterprise pricing by 33%"

  details:
    target: "saas-competitor.com"
    change_detected: "2024-03-29T10:30:00Z"
    change_magnitude: 0.85

  context:
    industry_trend: "Pricing pressure increasing across SaaS market"
    competitor_history: "Third price reduction this quarter"
    market_timing: "End of quarter pricing strategy"

  recommendations:
    immediate: ["Review pricing strategy", "Analyze positioning"]
    strategic: ["Consider value proposition enhancement"]
    content: ["Prepare competitive response messaging"]

  data_sources:
    primary: "Direct website monitoring"
    validation: "Cross-referenced with news sources"
    confidence: 0.94
```

### Trend Intelligence Summary
```yaml
intelligence_digest:
  period: "March 2024"
  monitoring_targets: 15
  total_changes_detected: 87

  significant_changes: [
    {
      category: "pricing",
      frequency: 12,
      trend: "downward_pressure",
      market_impact: "high"
    },
    {
      category: "features",
      frequency: 23,
      trend: "ai_integration",
      market_impact: "medium"
    }
  ]

  competitive_landscape:
    most_active_competitor: "competitor-b.com"
    change_frequency_leader: "competitor-c.com"
    pricing_aggressor: "competitor-a.com"

  market_intelligence:
    emerging_trends: ["AI feature integration", "Pricing transparency"]
    declining_trends: ["Feature complexity", "Premium pricing"]

  strategic_opportunities:
    positioning_gaps: ["SMB market pricing", "Integration simplicity"]
    timing_opportunities: ["Q2 announcement window"]
```

## Cost and Performance

### Monitoring Efficiency
```yaml
Credit Usage Patterns:
  Real-time monitoring: 50-100 credits/day per target
  Daily monitoring: 10-20 credits/day per target
  Weekly monitoring: 3-5 credits/week per target

Optimization Strategies:
  - Focus on high-value competitor pages
  - Use appropriate change thresholds
  - Batch similar monitoring operations
  - Leverage caching for frequently accessed content

Cost Management:
  - Set monitoring budgets and alerts
  - Prioritize targets by business impact
  - Use intelligent filtering to reduce noise
  - Optimize frequency based on change patterns
```

## Error Handling and Reliability

### Robust Monitoring
```yaml
Reliability Features:
  - Automatic retry on failed monitoring attempts
  - Fallback strategies for inaccessible sites
  - Change validation across multiple data points
  - False positive filtering and noise reduction

Quality Assurance:
  - Change confidence scoring
  - Cross-validation with multiple sources
  - Historical pattern verification
  - Human review triggers for significant changes
```

## Examples

### SaaS Competitor Monitoring
```bash
strategic-research-intelligence:intelligence-monitor \
  targets="competitor1.com/pricing,competitor2.com/features,competitor3.com/blog" \
  monitor_type="content_changes" \
  frequency="daily" \
  change_threshold="0.3" \
  alert_channels="slack:competitive-intel"
```

### Industry News Surveillance
```bash
strategic-research-intelligence:intelligence-monitor \
  targets="search:fintech regulation,search:banking technology trends" \
  monitor_type="news" \
  frequency="real-time" \
  alert_channels="webhook:https://api.yourapp.com/news-alerts"
```

### Technology Stack Monitoring
```bash
strategic-research-intelligence:intelligence-monitor \
  targets="builtwith.com/competitor1.com,stackshare.io/competitor2" \
  monitor_type="content_changes" \
  frequency="weekly" \
  change_threshold="0.1" \
  alert_channels="email:tech-team@yourcompany.com"
```

### Social Media Sentiment Tracking
```bash
strategic-research-intelligence:intelligence-monitor \
  targets="search:your-company social mentions,search:industry-sentiment" \
  monitor_type="social" \
  frequency="hourly" \
  baseline_period="14days" \
  alert_channels="slack:marketing-alerts"
```