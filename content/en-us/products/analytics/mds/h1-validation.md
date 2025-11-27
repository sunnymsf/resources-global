# Analytics heading

## Description

Analytics tracking is essential for understanding user behavior and improving product experiences. This guide covers common analytics patterns that can be reused across different documentation sections.

## Common Analytics Patterns

### Page View Tracking

Track when users view specific documentation pages:

```javascript
// Basic page view tracking
analytics.track("page_viewed", {
  page_title: "Analytics Guide",
  page_url: window.location.href,
  section: "overview",
});
```

![Salesforce Docs](../../../../media/salesforcedocs.png)
