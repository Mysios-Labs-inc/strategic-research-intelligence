# Strategic Research Intelligence Plugin

**Part of the Mysios Labs Professional Intelligence Suite**

Advanced business intelligence and competitive research workflows built on Firecrawl. Provides autonomous investigation capabilities, strategic trend analysis, and multi-source research for strategic decision-making.

*Works seamlessly with [Career Intelligence Plugin](../career-intelligence-plugin) for complete professional intelligence workflows.*

## Overview

The Firecrawl Research Plugin provides specialized skills for web-based research, trend monitoring, and competitive analysis. It leverages Firecrawl's sophisticated crawling and extraction technology to gather intelligence from across the web.

## Features

### 🔍 **Trend Monitoring**
- Real-time trend discovery across web sources
- Breaking news monitoring for timely responses
- Topic emergence tracking for early positioning
- Multi-source momentum analysis

### 📊 **Research Assistance**
- Comprehensive multi-source research
- Fact verification and source validation
- Academic and professional research support
- Evidence-based content foundation building

### 🎯 **Competitive Analysis**
- Competitor content strategy monitoring
- Market positioning analysis
- Strategic messaging tracking
- Gap identification for differentiation

## Skills Included

*Requires the official Firecrawl plugin for CLI operations*

### Strategic Intelligence Skills
| Skill | Purpose | Best For |
|-------|---------|----------|
| **trend-monitor** | Discover trending topics and breaking news | Reactive content creation, timely responses |
| **research-assist** | Comprehensive research with source validation | Long-form content, fact-checking, analysis |
| **competitive-analysis** | Monitor competitors and market positioning | Strategic planning, differentiation opportunities |

### Advanced Investigation Skills
| Skill | Purpose | Best For |
|-------|---------|----------|
| **ai-research-agent** | Autonomous AI-powered multi-step investigations | Complex market research, expert discovery, due diligence |
| **interactive-investigation** | Browser-based research with form interactions | Protected content access, complex user journeys |
| **intelligence-monitor** | Real-time monitoring and change detection | Competitive surveillance, automated alerting, trend tracking |

## Integration with Mysios Professional Intelligence Suite

This plugin is designed to work seamlessly with the Career Intelligence plugin for complete professional workflows:

### **Career + Market Intelligence Workflows:**
```yaml
# Research target companies for job search
strategic-research-intelligence:competitive-analysis competitors="target-company.com"
  ↓
career-intelligence:job-search company="Target Company"
  ↓
career-intelligence:resume-optimize based-on="company-research"

# Monitor industry trends for career positioning
strategic-research-intelligence:trend-monitor topic="AI industry trends"
  ↓
career-intelligence:skill-gap-analysis trends="AI-trends"
  ↓
career-intelligence:development-plan based-on="market-intelligence"
```

```yaml
Research → Content Creation Workflow:
1. firecrawl-research:trend-monitor (discover trending topics)
2. firecrawl-research:research-assist (deep research on topics)
3. social-media-manager:post-to-substack (create informed content)
4. social-media-manager:create-for-x (share key insights)
```

## Installation Requirements

### Prerequisites
- **Official Firecrawl Plugin** (install first):
  ```bash
  /plugin install firecrawl@claude-plugins-official
  ```
- Firecrawl API access (sign up at https://firecrawl.dev)
- API key configured in environment variables

### Setup
1. Install the official Firecrawl plugin (provides CLI access)
2. Install this Strategic Research Intelligence plugin (provides advanced workflows)
3. Configure API credentials: `firecrawl login --browser`
4. Test with strategic intelligence: `strategic-research-intelligence:trend-monitor topic="test"`

### Plugin Architecture
```
┌─────────────────────────────────────┐
│  Strategic Research Intelligence    │  ← Your strategic workflows
│  (this plugin)                     │
├─────────────────────────────────────┤
│  Official Firecrawl Plugin         │  ← CLI access layer
│  (claude-plugins-official)         │
├─────────────────────────────────────┤
│  Firecrawl CLI                     │  ← Core scraping engine
└─────────────────────────────────────┘
```

## Quick Start

*First install the official Firecrawl plugin for CLI access*

### Strategic Intelligence Operations
```bash
# Monitor trending topics with AI analysis
strategic-research-intelligence:trend-monitor topic="artificial intelligence" timeframe="24h" format="summary"

# Comprehensive multi-source research
strategic-research-intelligence:research-assist topic="quantum computing applications" depth="standard" output="full_analysis"

# Strategic competitive intelligence
strategic-research-intelligence:competitive-analysis competitors="competitor.com" focus="content" timeframe="month"
```

### Advanced Investigation Workflows
```bash
# Autonomous AI-powered research
strategic-research-intelligence:ai-research-agent objective="Analyze SaaS competition" depth="comprehensive"

# Real-time competitive monitoring
strategic-research-intelligence:intelligence-monitor targets="competitor1.com,competitor2.com" frequency="daily"

# Complex browser-based investigation
strategic-research-intelligence:interactive-investigation target="https://protected-content.com" workflow="login_and_extract"
```

## Configuration

### API Setup
Configure your Firecrawl API credentials:

```bash
export FIRECRAWL_API_KEY="your_api_key_here"
```

### Usage Limits
Be mindful of API usage limits:
- **Basic Plan**: 1,000 requests/month
- **Professional Plan**: 10,000 requests/month
- **Enterprise Plan**: Custom limits

### Rate Limiting
Built-in rate limiting respects Firecrawl API constraints:
- Maximum 10 concurrent requests
- Automatic backoff on rate limit responses
- Intelligent request batching for efficiency

## Advanced Features

### Multi-Source Research
Combine insights from multiple sources:
- News outlets (Reuters, AP, BBC)
- Technical publications (Ars Technica, Wired)
- Academic sources (arXiv, research institutions)
- Industry reports and expert analysis

### Smart Source Filtering
Intelligent source credibility assessment:
- Government and institutional sources (highest priority)
- Established media outlets (high priority)
- Expert blogs and analysis (medium priority)
- Community sources (lower priority)

### Historical Tracking
Monitor changes over time:
- Trend momentum and lifecycle tracking
- Competitive strategy evolution
- Content theme development
- Market positioning shifts

## Integration Patterns

### With Scheduled Tasks
Perfect for automated research workflows:

```yaml
# Morning trend monitoring
Cron: 8 AM daily
Task: firecrawl-research:trend-monitor + social-media-manager:create-for-x

# Weekly competitive analysis
Cron: Monday 9 AM
Task: firecrawl-research:competitive-analysis + strategy review

# Research for long-form content
Cron: Sunday 2 PM
Task: firecrawl-research:research-assist + social-media-manager:post-to-substack
```

### With Content Streams
Enhance your content strategy:

**Stream 1 (Long-form Content)**
- Use `research-assist` for comprehensive article research
- Use `competitive-analysis` for differentiation insights

**Stream 3 (Reactive Content)**
- Use `trend-monitor` for breaking news and trending topics
- Use `research-assist` for quick fact-checking

**Stream 5 (Outbound)**
- Use `competitive-analysis` for partner content discovery
- Use `trend-monitor` for industry conversation monitoring

## Best Practices

### Efficient Research
1. **Start broad, then narrow**: Use trend monitoring to identify topics, then deep research
2. **Source diversity**: Combine news, academic, and expert sources
3. **Fact verification**: Cross-reference claims across multiple sources
4. **Recency awareness**: Consider information freshness for your use case

### Competitive Intelligence
1. **Regular monitoring**: Set up systematic competitor tracking
2. **Focus areas**: Don't try to monitor everything - pick key areas
3. **Historical context**: Track changes over time for trend identification
4. **Actionable insights**: Focus on intelligence you can act on

### API Optimization
1. **Batch requests**: Group similar queries together
2. **Cache results**: Store frequently accessed research
3. **Strategic timing**: Use during off-peak hours when possible
4. **Result reuse**: Leverage research across multiple content pieces

## Troubleshooting

### Common Issues

**API Authentication Errors**
- Verify FIRECRAWL_API_KEY is set correctly
- Check API key permissions and limits
- Confirm key is active and not expired

**Rate Limiting**
- Reduce concurrent request volume
- Implement longer delays between requests
- Consider upgrading API plan

**Content Extraction Failures**
- Verify target sites allow crawling
- Check if sites have changed structure
- Try alternative sources for same information

**Poor Research Results**
- Refine search terms and parameters
- Adjust source type priorities
- Extend research timeframe or depth

### Support
For technical issues:
1. Check Firecrawl API status
2. Verify plugin installation
3. Review API usage and limits
4. Check integration logs

## Examples and Use Cases

### Startup Competitive Intelligence
Monitor competitor fundraising, product launches, and strategic moves for timely competitive responses.

### Content Creator Research
Comprehensive topic research with source validation for authoritative content creation.

### Crisis Response Monitoring
Real-time monitoring of breaking news and trending topics for rapid crisis response.

### Market Research
Industry trend analysis and competitive landscape mapping for strategic planning.

## Changelog

### Version 1.0.0
- Initial release as part of Mysios Labs Professional Intelligence Suite
- 6 strategic intelligence skills: trend-monitor, research-assist, competitive-analysis, ai-research-agent, interactive-investigation, intelligence-monitor
- Integration with official Firecrawl plugin
- Career Intelligence plugin integration workflows
- Autonomous AI-powered research capabilities

## License

MIT License - see LICENSE file for details.

## 🏢 About Mysios Labs

Building the future of AI-powered professional intelligence tools.

**Professional Intelligence Suite:**
- [Career Intelligence Plugin](../career-intelligence-plugin) - Job search and career advancement
- **Strategic Research Intelligence Plugin** - Market and competitive analysis
- Integrated professional workflows

**Connect with Mysios Labs:**
- **Website:** [mysioslabs.com](https://mysioslabs.com)
- **Support:** hello@mysioslabs.com
- **GitHub:** [@Mysios-Labs-inc](https://github.com/Mysios-Labs-inc)
- **Marketplace:** [Mysios Professional Plugins](../mysios-professional-plugins-marketplace)

## Roadmap

### Version 1.1.0 (Planned)
- Business framework integration (Porter's Five Forces, SWOT analysis)
- Enhanced Career Intelligence integration workflows
- Advanced competitive monitoring alerts
- Patent and financial intelligence modules

### Version 1.2.0 (Planned)
- Predictive competitive modeling
- Social media automation integration
- Custom strategic framework builders
- Enterprise team collaboration features

---

*Professional Intelligence Suite: Transform your career and business strategy with AI-powered automation* 🎯✨