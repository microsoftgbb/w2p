# W2P — Whiteboard to Prototype

Go from idea to working prototype. Fast.

```
idea → hypothesis → scope → build → learn
```

No docs. No planning decks. Just structured thinking and code.

---

## How to use

1. Fill in `whiteboard/idea.md` — what's the problem?
2. Pick an approach in `whiteboard/hypothesis.md`
3. Lock scope in `whiteboard/scope.md` — this is the most important step
4. Sketch the shape in `whiteboard/architecture.md`
5. Run experiments. Log everything in `whiteboard/log.md`
6. Write up `whiteboard/findings.md` when done

Use `prompts/` to accelerate with an LLM.

---

## Example

**Idea:** Latency spikes in our API at p99. Root cause unknown.

**Hypothesis:** DB connection pool exhaustion under bursty load.

**Scope:** Prove pool exhaustion happens. Not: fix it, not: rewrite the pool.

**Experiment:** Simulate 200 concurrent requests, monitor pool metrics.

**Finding:** Pool maxes at 10 connections. Queue backs up. Confirmed.

---

Less writing. More building.
