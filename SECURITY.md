# Security policy

This policy covers every open-source repository of
[Roundly Consulting](https://roundly-consulting.com), unless a repository ships its own `SECURITY.md`.

## Supported versions

Only the **latest release** of each package receives security fixes. Fixes ship as a new release;
older releases are not patched, so upgrade to the newest version to get them.

## Reporting a vulnerability

**Please do not report security issues through public issues, pull requests or discussions.**

Report them privately through GitHub:

1. Open the affected repository on GitHub.
2. Go to the **Security** tab and click **Report a vulnerability**.
3. Fill in the form and submit it. Only the maintainers can see it.

Please include as much of the following as you can:

- the package and the version (or commit) you tested;
- the type of issue (for example SQL injection, authentication bypass, information disclosure);
- the affected file(s), class(es) or endpoint(s);
- step-by-step instructions or a proof of concept to reproduce it;
- the impact: what an attacker could do with it.

## What happens next

We are a small team and handle reports on a **best-effort** basis — we will reply as soon as we
can. We will confirm the issue, keep you updated in the private report, and coordinate the fix and
its disclosure with you. When the fix is released we publish a GitHub security advisory and, if you
wish, credit you for the discovery.
