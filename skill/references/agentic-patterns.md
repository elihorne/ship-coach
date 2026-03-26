# Agentic Build Patterns

How AI-assisted development changes the scope creep problem -- and creates new ones.

## The Core Shift

Before agentic tools, the constraint was **can**.

Can I build this? Can I learn this stack? Can my team move fast enough? These were real limits. They forced prioritization by default.

Agentic tools have largely removed that constraint. You describe something and it gets built. Claude Code, Cursor, and similar tools can scaffold a feature in minutes that used to take days.

This creates a new and more dangerous constraint: **should**.

Should I build this? Should I build it now? Should I build it at all?

The "can" constraint forced discipline by friction. The "should" constraint requires it by choice. Most builders aren't used to this. They mistake velocity for progress.

**When to invoke:** Whenever someone is building in an agentic environment and hasn't explicitly asked whether a feature belongs in the MVP. Assume the risk is present; confirm the discipline is too.

---

## New Failure Modes in Agentic Development

### 1. Agent-Generated Scope Creep

The agent interprets a broad prompt and returns more than you asked for. You accept it because it's already written. Now it's in your codebase.

**How it happens:**
- "Add a settings page" → agent builds themes, notifications, account management, and billing preferences
- "Make this shareable" → agent adds share links, permissions, copy-to-clipboard, social previews, and embed codes
- "Improve onboarding" → agent rewrites the entire flow, adds tooltips, creates a welcome email sequence

**How to catch it:** Before accepting a large diff, ask: which of these did I actually request? What's the minimum version of what I asked for?

**Challenge phrase:** "Which parts of this output serve the core user right now? Which parts came from the agent's assumptions?"

### 2. Implied Feature Creep

You describe a user story. The agent infers supporting features that seem logical but weren't requested.

**Examples:**
- Describing a "user profile" and getting avatar upload, bio, social links, and a public profile URL
- Asking for "email notifications" and getting notification preferences, frequency settings, and an unsubscribe flow
- Building "search" and getting filters, sort options, saved searches, and recent history

These additions aren't wrong -- they're just premature. Each one is a decision you didn't make consciously.

**How to catch it:** After each build session, list every feature that exists. Ask which ones you explicitly decided to include.

**Challenge phrase:** "Did you decide to build this, or did the agent decide for you?"

### 3. The Productivity Illusion

Agentic development feels like progress because output is constant. Code is being written. Features appear. The product grows.

But shipping ten features you don't need is not progress. It's technical debt with a user interface.

The feeling of momentum can suppress the instinct to stop and validate. When building was slow, you were forced to decide carefully. When building is instant, the discipline has to come from somewhere else.

**How to catch it:** Measure by learning, not by commits. What did you validate this week? Not: what did you build?

**Challenge phrase:** "What did you learn about your users this week? What did you ship that generated that learning?"

### 4. The Infinite Iteration Trap

Agents make iteration so cheap that you never have to ship. You can always improve. The product is always almost ready.

This is the new version of waiting for "one more feature." Except now the one more feature takes 20 minutes, so there's always a reason to do it.

**How to catch it:** If you've been iterating for more than two weeks without shipping to a real user, you're in this trap.

**Challenge phrase:** "Who has used this? What did they do? If the answer is no one, stop building and start shipping."

### 5. Refactor Spiral

Agentic tools are good at refactoring. So the codebase is always improvable. Clean code is always available, a few prompts away.

This is a distraction. Clean code that doesn't ship is worthless. Messy code in production is better than perfect code in development.

**How to catch it:** If refactoring has happened before any users exist, it's premature.

**Challenge phrase:** "How many users are affected by this refactor? If the answer is zero, defer it."

---

## Agentic Anti-Patterns

### The Scaffolding Trap

Agents are very good at generating boilerplate: auth systems, admin panels, CRUD interfaces, settings pages. These feel like progress because they look like a real product.

But scaffolding isn't product. Scaffolding is the shape of a product without the core value.

A real product does one job for one user better than anything else. Scaffolding does many jobs adequately.

**Red flag:** If your product looks complete but hasn't solved anyone's problem yet, you've built scaffolding.

### Over-Engineered for Scale

Agents will happily build for scale you don't have. Queues, workers, caching layers, database indexes, microservices.

You don't need any of this before you have users. Scale problems are good problems to have.

**Red flag:** Infrastructure complexity before user complexity.

### Multi-Tenant Too Early

Agents default to building for teams because most SaaS is multi-tenant. But teams features are a scope multiplier -- they add permissions, roles, invites, billing per seat, and audit logs.

Build for one user first. Add teams when a paying user asks for them.

**Red flag:** "Workspace," "organization," or "team" in your data model before you have a single paying user.

---

## The Agentic Discipline Framework

When building with agents, apply these checks at each session start:

### Before You Prompt

1. What is the one thing I'm building today?
2. Which user does this serve?
3. What's the minimum version of this that proves the hypothesis?
4. What am I explicitly not building today?

Writing down what you're not building is as important as writing down what you are.

### After You Receive Output

1. Is everything here something I asked for?
2. Is everything here something my core user needs right now?
3. What can I delete from this diff without losing core value?
4. Does accepting this make the product harder to ship?

### End of Session

1. What can a user do today that they couldn't do yesterday?
2. What did I add that I didn't explicitly decide to add?
3. Am I closer to shipping or further away?

---

## The Solo Builder Context

Agentic tools particularly benefit solo builders. One person can now build what previously required a team.

But this creates a new trap: the surface area of what you can build vastly exceeds the surface area of what you should build.

A team has natural forcing functions -- meetings, sprint planning, engineers asking "why are we building this." A solo builder with an agent has none of these. The agent doesn't push back. It just builds.

You have to be your own forcing function. Ship Coach exists to be that voice.

**The solo builder rule:** If you can't explain in one sentence why a feature is in the MVP, it isn't.

---

## References

- Paul Graham: "Do Things That Don't Scale" -- manual first, automate after validation
- YC: Launch early, iterate publicly -- users in production beats users in your head
- a16z: PMF first, scale second -- don't build for a scale you haven't earned
