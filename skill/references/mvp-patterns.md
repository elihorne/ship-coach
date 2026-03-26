# MVP Patterns

What makes a good MVP, common anti-patterns, and how to scope ruthlessly.

## What an MVP Actually Is

An MVP is the smallest thing you can build to test your core hypothesis. It is not:

- A feature-complete v1
- A prototype you're embarrassed by
- A landing page (unless your hypothesis is about demand)
- A fully polished product minus some features

An MVP is the minimum product that lets you learn whether your core value proposition works.

## Good MVP Patterns

### Pattern 1: Single Player Mode First

Build for one user doing one thing. Ignore multiplayer, collaboration, teams, sharing.

**Examples:**

- Notion started as personal notes, not team wikis
- Dropbox started as file sync, not collaboration
- Figma started as design tool, not design system management

**When to apply:** Almost always. Teams features are scope magnifiers.

**The test:** Can one person get value from this alone?

### Pattern 2: Manual Backend, Automated Frontend

Automate what users see. Do everything else manually.

**Examples:**

- Zapier team manually connected integrations before building the platform
- Food delivery apps had founders delivering food
- Concierge services before scheduling algorithms

**When to apply:** When you're not sure the core value proposition works yet.

**The test:** Can you deliver the value to 10 users manually?

### Pattern 3: Wizard of Oz

The user thinks it's automated, but you're doing it behind the scenes.

**Examples:**

- AI features powered by humans initially
- Recommendations curated manually
- "Smart" features that are actually rule-based

**When to apply:** When automation is expensive and uncertain.

**The test:** Would you rather spend 2 weeks building automation or 2 weeks testing the hypothesis?

### Pattern 4: Existing Platform Wedge

Build on top of something that already has users.

**Examples:**

- Slack apps before standalone products
- Shopify apps before e-commerce platforms
- Chrome extensions before web apps

**When to apply:** When distribution is your biggest risk.

**The test:** Where are your users already spending time?

### Pattern 5: Painful but Valuable

Solve one painful problem extremely well. Ignore adjacent problems.

**Examples:**

- Stripe: payments only. No invoicing, no subscriptions initially.
- Twilio: SMS only. No voice, no video initially.
- Linear: issues only. No docs, no wikis.

**When to apply:** When you've identified a sharp pain point.

**The test:** Do users say "I would pay for this one thing"?

## Anti-Patterns to Avoid

### Anti-Pattern 1: The Platform Trap

Building a platform before you have users. Creating "flexibility" nobody asked for.

**Symptoms:**

- Configurable everything
- Plugin architecture with no plugins
- "It can do anything" positioning
- API-first when you have no API consumers

**The fix:** Build the specific thing. Generalize after you have 10 customers using it.

### Anti-Pattern 2: The Auth Obsession

Building user authentication, roles, permissions, teams before the core feature works.

**Symptoms:**

- Multiple user roles in the spec
- Team management in v1
- SSO requirements
- "Enterprise-ready" from day one

**The fix:** Magic links. One user type. Add complexity when customers demand it (and pay for it).

### Anti-Pattern 3: The Dashboard Syndrome

Building analytics and admin dashboards before there's data worth analyzing.

**Symptoms:**

- Charts and graphs in v1
- Admin panels before users
- Metrics dashboards before metrics

**The fix:** Use SQL or Metabase. Build dashboards when you have 1000 users.

### Anti-Pattern 4: The Settings Page

Extensive configuration before you know what the right defaults are.

**Symptoms:**

- Multiple themes
- Customizable everything
- User preferences for everything
- "Let the user decide"

**The fix:** Pick good defaults. Add settings when users ask repeatedly for something different.

### Anti-Pattern 5: The Integration Spiral

Building integrations before proving core value.

**Symptoms:**

- Zapier integration in v1
- Multiple data sources before one works
- Import/export before users have data

**The fix:** Manual import via CSV. One integration after 10 users ask.

### Anti-Pattern 6: The Mobile Tax

Building mobile apps when a responsive web app would work.

**Symptoms:**

- iOS and Android in v1
- Native apps for content that doesn't need them
- App store presence as a goal

**The fix:** PWA or responsive web. Native mobile after web has PMF.

## Scoping Techniques

### The "Launch Tomorrow" Exercise

Ask: If you had to launch tomorrow, what would you keep?

Everything else is candidate for cut or defer.

### The 80/20 Feature Cut

List all features. Ask: Which 20% deliver 80% of the value?

Build only those. Be honest about what's core vs. nice.

### The Single User Story

Write one user story. The most important one.

Everything in the MVP should support that story. Everything that doesn't is scope creep.

### The "What's Embarrassing" Test

If you launched today, what would embarrass you?

Only fix the truly embarrassing things. "Not polished" is not embarrassing. "Doesn't work" is embarrassing.

### The Week Constraint

What could you ship in one week?

If a feature can't fit in that constraint, it's either too big or should be deferred.
