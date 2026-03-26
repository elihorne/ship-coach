# Scope Check

Detailed questions for evaluating whether a feature belongs in the MVP.

## The Quick Check

Run every feature through these five questions first:

1. **Does the core user need this to get value?** If no → cut
2. **Have real users asked for this?** If no → defer
3. **Can you build it in under a week?** If no → scope down or defer
4. **Would you be embarrassed without it?** If no → defer
5. **Does it move your key metric?** If no → defer

A feature that fails 2+ questions should be cut or deferred. Don't negotiate.

## Deep Evaluation Questions

When the quick check isn't clear, go deeper.

### User Value Questions

- Who specifically benefits from this feature?
- What job does this help them do?
- How are they solving this problem today?
- How painful is the current solution (1-10)?
- Would they pay for this feature alone?
- Have they said they need this, or are you assuming?

**Red flag answers:**

- "Everyone could use this" → too vague
- "It would be nice" → not painful enough
- "Competitors have it" → not user-driven
- "I think users would want" → assumption, not evidence

### Build Cost Questions

- How many days/weeks to build?
- What new technical complexity does this introduce?
- Does this require new infrastructure?
- Does this add ongoing maintenance burden?
- Can this be done manually instead?
- What's the simplest version of this feature?

**Red flag answers:**

- "It depends" → scope is unclear, needs breaking down
- "Just a few changes" → usually underestimated
- "We need to build X first" → hidden dependencies
- "It's simple" → famous last words

### Strategic Questions

- Does this reinforce our core value prop or dilute it?
- If this works, what does it unlock?
- If this fails, what did we learn?
- Is this feature defensible or easily copied?
- Does this move us toward PMF or away from it?

**Red flag answers:**

- "It's table stakes" → often not actually required
- "We need feature parity" → competitor-driven, not user-driven
- "Investors want to see" → wrong audience

### Timing Questions

- Why now? Why not after launch?
- What do we learn by building this before launch?
- What's the cost of adding this post-launch?
- Can we validate the need without building it?
- What would we do if we learned this was wrong after building?

**Red flag answers:**

- "It's easier to do now" → convenience, not necessity
- "Users expect it" → unvalidated assumption
- "It'll be harder later" → often false, and you'll learn more later

## Feature Disposition Matrix

After evaluation, assign each feature to one category:

| Category | Criteria | Action |
|----------|----------|--------|
| **Must Have** | Core value prop fails without it | Build it |
| **Should Have** | Users explicitly asked, high pain | Build if < 1 week |
| **Nice to Have** | Would improve experience | Defer to v2 |
| **Won't Have** | Speculative, low pain, or complex | Cut entirely |

Be ruthless. Most features are Nice to Have or Won't Have.

## Common Scope Creep Triggers

Watch for these phrases. They often precede scope creep.

### "While we're in there..."

Translation: I noticed something adjacent and want to fix it.

Response: Is this on the critical path? If not, note it and move on.

### "It would only take..."

Translation: I'm underestimating because I want to build it.

Response: Is this in the Must Have category? If not, defer it regardless of estimate.

### "Users will expect..."

Translation: I'm guessing what users want.

Response: Which users said this? If none, it's speculation.

### "It's not that hard..."

Translation: I'm excited about this and want to justify it.

Response: Hard or not, does it belong in the MVP?

### "Competitors have..."

Translation: I'm worried about comparison.

Response: Are users choosing competitors because of this specific feature?

### "This is important for..."

Translation: I'm about to give a reason that may not be valid.

Response: Important for whom? The core user doing the core job?

### "We might as well..."

Translation: I want to bundle something in.

Response: Is this a must-have? If not, we shouldn't "might as well."

## The Final Test

Before including any feature, answer this:

**"If we didn't build this, could we still launch and learn whether our core hypothesis is correct?"**

If yes → don't build it yet.

If no → build the simplest version that lets you launch.
