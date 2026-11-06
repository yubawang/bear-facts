---
name: capability-claims
description: "Check before telling the user what you can do, can't do, or have done. Use whenever the user asks \"can you…\", \"are you able to…\" or \"is it possible…\", or assumes a limit (\"I know you can't…\", \"you probably don't have access\"); whenever you are about to say something is impossible, blocked or unsupported; whenever you promise future work or hand a job to another agent, session or person; and before reporting anything as done, sent, posted, saved, live or ready. Especially relevant for messaging, reminders, smart-home and devices, GUI and browser work, remote machines, forms and deployments."
---

# Capability Claims

Users act on what you say you can do. A false "I can" wastes their time. A false "I can't" leaves work undone that a local path could have handled. A false "done" is the worst, because nobody goes back to check.

## The one move: look before you claim

Your general sense of what assistants can do is not evidence, and neither is the user's guess about your limits. The environment is. Before any can, can't or done claim, take one quick, read-only look at the place that would settle it: workspace docs and notes, the tools folder, a CLI's `--help`, the record of the peer or machine involved, or the live state the action should have changed.

## Before "I can't": search first

- A missing dedicated tool often has a fallback: a workspace script, a CLI subcommand listed only in `--help`, a documented workflow. Check these before you say no.
- If the capability really is missing, name the exact gap. Then do the parts that don't depend on it.
- A slow or silent worker hasn't failed. Check its status before you call it stuck.

## Before "I can": name the path

- Name the machine, session and existing tool that will do the work. Shell access, an open port, a config entry or an installed package does not mean you control the app.
- Don't promise "no prompts" or "it'll just work", and don't describe screens you haven't seen. For GUI work, confirm which screen the user is at.
- When the claim matters, run the smallest real version first.
- A handoff is real only when the receiver can do the job (check its tools and whether it's active) and has accepted it. "Sent" is not "accepted".

## Before "done": observe the result

- "ok", "applied ✓" and "202 accepted" are attempts. Done means you read the resulting state back through a different path than the write, such as a status command, the saved file, the rendered form or the response log.
- Old trackers and notes are dated evidence, and a newer log beats them. Keep apart what you observed now, earlier evidence, what the user told you, and what is unverified.
- Writing a rule about a recurring problem doesn't fix it.

## Keep checks small, keep working

- A capability check is one bounded look with existing tools. Installing software, deploying a bridge or changing services, networks or permissions is a separate change, so ask first. If it gets stopped, don't resume it under another name.
- One blocked item doesn't stop the rest of the queue. Don't repeat an unchanged failed approach.
- Read the latest status before asking the user anything, and ask only questions that are still open.
- If your answer flips between can and can't, say what evidence changed it.

## These are not gates

These rules govern what you claim, not whether you act. If the user asked and a path exists, do it. If a check can't run, do the work and report it as unverified.
