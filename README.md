# mind

A way of thinking for coding agents. It teaches the model to doubt the task before it
works on it.

Most agents are eager: ask for "make this faster" and they make the thing faster, even if
the thing should not exist. `mind` makes them stop and run one order of operations first:

**Question → Delete → Simplify → Accelerate → Automate**

1. **Question.** Every requirement has a person behind it. "Security wants it", "we always
   did it" are claims until someone, a number, or a source backs them. Convention is
   deletable; physics and law are not.
2. **Delete.** The best part is no part. If nothing had to come back, you did not delete
   enough.
3. **Simplify.** Only what survived, and by hand first.
4. **Accelerate.** Only now, and against the physical limit, not against last quarter.
5. **Automate.** Last. Automating a step you never proved necessary just makes a wrong
   process faster.

Then it loops: after step 5, back to step 1.

## What changes

Ask "this endpoint is slow, speed it up". A default agent adds a cache, tunes the query,
adds an index. With `mind` it first asks who calls the endpoint and why, and sometimes the
answer is that the caller throws the result away, so the fix is deleting the call.

It also changes how the agent talks: it opens with what is going on and the call it
recommends, one cause instead of ten findings, numbers or an honest "unknown".

## Not only for code

It works wherever something can be questioned: architecture decisions, a messy process,
a pricing page, a brainstorm that keeps adding ideas instead of cutting them. Language-
and framework-agnostic.

## Install

```bash
npx skills add locoholy/mind -g
```

Works with Claude Code, Codex, Cursor, Gemini CLI, OpenCode and any agent that reads the
Agent Skills format. Update with `npx skills update -g`.

No Node? Copy `skills/mind/` into your agent's skills folder (`~/.claude/skills/` for
Claude Code, `~/.agents/skills/` for Codex and most others) and restart the agent.

Use it by running `/mind`, or just say "refactor this", "simplify", "why is this slow".

## Part of a larger set

I keep every skill I use in [locoholy/agent-skills](https://github.com/locoholy/agent-skills).

## License

MIT
