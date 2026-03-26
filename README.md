# Ship Coach

A Claude Code skill that coaches you on shipping. It helps you build less, ship faster, and validate sooner.

## The problem

AI tools have removed the constraint of "can I build this?" You describe something and it gets built. That's powerful, but it creates a new problem: nothing forces you to ask "should I build this?"

Agents don't push back. They just build. Ship Coach is the pushback.

It watches for scope creep, premature optimization, features nobody asked for, and the dozen other ways builders avoid shipping. When it spots a pattern, it names it and challenges you to cut.

## How it works

Ship Coach activates contextually. You don't invoke it manually. It triggers when you're discussing feature prioritization, scope decisions, MVP planning, or "should I build X" questions. It also triggers when you're about to accept a large diff, when you're iterating without shipping, or when scaffolding appears before core value is proven.

When it activates, it applies a shipping framework: understand the current state, evaluate against shipping criteria, challenge scope creep, and make a clear recommendation (ship it, cut X and ship, defer X, or rethink).

## What's in the references

The skill pulls from established startup thinking to back up its advice:

- **Paul Graham** on launching fast, doing things that don't scale, and why embarrassment is a feature
- **PMF and growth** on product-market fit signals, when to launch, pivots, and doing hard things
- **YC wisdom** on default alive, 10x products, talking to users, MVPs, and retention
- **Indie hacker** on shipping fast, charging early, staying small, and building in public
- **Shape Up** on fixed time/variable scope, shaping, circuit breakers, and bets not backlogs
- **MVP patterns** on what makes a good MVP, common anti-patterns like the platform trap and the auth obsession
- **Agentic patterns** on new failure modes specific to AI-assisted development: agent-generated scope creep, the productivity illusion, the infinite iteration trap
- **Scope check** with detailed evaluation questions for any feature

## Install

```bash
npx add-skill elihorne/ship-coach
```

That's it. Ship Coach will activate automatically when relevant.

## Source files

The raw source for the skill is in the `skill/` directory if you want to browse or fork it. The `.skill` file is just a zip of that directory.

## Philosophy

Ship something real to real users. Everything else is rationalization. The goal is not a perfect product. The goal is learning whether anyone cares. You learn by shipping, not by planning.
