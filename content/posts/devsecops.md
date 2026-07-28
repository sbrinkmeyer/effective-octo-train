+++
title = 'The State of DevSecOps in 2026'
date = 2026-07-28T09:00:00-05:00
draft = false
tags = ['DevSecOps', 'CI/CD', 'Supply Chain']
+++

Two years ago I'd have told you the whole game was shifting security left. Get the scans
into the pipeline, catch things before they ship, done.

That wasn't wrong, exactly. But the industry spent a decade pushing security, testing, and
deployment onto developers, and somewhere in there it stopped scaling. The pushback that
surfaced in 2025 even has a name now — people are calling it shifting *down* instead of
left — and the complaint underneath it is simple: [developers didn't sign up to be YAML
engineers](https://dev.to/meena_nukala/devops-in-2026-what-it-really-means-now-and-where-its-heading-fast-2jkg).

That's the most interesting change, and it's a correction rather than a reversal. Early is
still right. What we got wrong was assuming early meant *somebody else's problem now*.

## What actually changed

**Security stopped being a best practice and became a filing deadline.**

The EU Cyber Resilience Act takes effect in September 2026, with real vulnerability
reporting obligations and SBOM requirements attached
([overview](https://cloudsmith.com/blog/the-2026-guide-to-software-supply-chain-security-from-static-sboms-to-agentic-governance)).
That drags this conversation out of engineering and onto a compliance calendar. If you sell
software into Europe, "we're planning to get to SBOMs" stops being an acceptable answer
this year.

The SBOM question itself moved, too. Nobody serious asks whether you can generate one — the
tooling does that. The question is whether you can *act* on it when something lands: can
you tell me today which deployed environments contain the bad version, and how fast can you
get them off it? [Generating an artifact nobody reads is
theater](http://sdtimes.com/software-supply-chain-security/).

**AI became a dependency you can't scan.**

This is the genuinely new one. A model in your stack is a third-party dependency, but not
one your existing scanners can read — no lockfile to parse, no CVE feed to diff against.
Hence the [ML-BOM and AI-BOM ideas making the
rounds](https://xygeni.io/blog/owasp-global-appsec-eu-2026-vienna-key-takeaways-on-secure-software-supply-chain-mcp-security-an-the-ai-bom/):
an inventory of models, where the training data came from, and what the thing is allowed to
touch.

The attack surface moved to match. Agents commit code. MCP servers execute tool calls on
someone's behalf. Malicious packages are being written to target the AI tooling rather than
the humans using it.

I don't think anybody has this solved, mine included. What I'd say is that the shape is
familiar even when the contents aren't: an under-reviewed thing, holding credentials, doing
work inside your pipeline. We've met that problem before.

## What didn't change

The durable parts are boring. That's why they're durable.

**Automate it, or it didn't really happen.** A control that depends on somebody remembering
is a control you don't have. That was true before this tooling cycle and it'll be true
after it.

**Build the secure path early, not as a retrofit.** Security bolted on at the end just
becomes the thing everyone routes around. The correction above doesn't undo this — it means
the secure path has to be the *easy* path. Otherwise you've built a speed bump and called
it a guardrail.

**Repeatable beats documented.** A pipeline that does the thing beats a runbook describing
the thing. I deliver into customer environments that are all a little different, and the
only approach that survives that is making delivery itself repeatable instead of
accumulating tribal knowledge about each one.

## Where I'd put the effort

If a team is behind and can only fix one thing: make your inventory real. Not the SBOM
artifact — the actual ability to answer *where is this version running right now.*

Most of the pain during a supply chain incident isn't the patch. It's not knowing where to
apply it. Everything else gets easier once you can answer that question in minutes instead
of days.
