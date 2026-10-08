# Django Expert Evaluation Rubric

## Scoring

Score each dimension from 0 to 2:

| Dimension | 0 | 1 | 2 |
|---|---|---|---|
| Discovery | Skips required context | Partial inspection | Identifies relevant project/version/context before acting |
| Architecture | Unsafe/inappropriate design | Mostly suitable with gaps | Simplest design that fits the project |
| Implementation | Incorrect or incomplete | Works with notable gaps | Correct, idiomatic, minimal change |
| Security | Vulnerability introduced/ignored | Basic controls only | Explicit auth, authorization and relevant security gates |
| Testing | No meaningful tests | Partial coverage | Behavior, failure, edge and regression coverage appropriate to risk |
| Performance | Ignores obvious issue | Generic optimization | Evidence-driven query/cache/index/payload/background-work decisions |
| Deployment | Ignores production impact | Basic deployment notes | Configuration, migrations, health, monitoring and rollback considered |
| Accuracy | Fabricates or overclaims | Some unsupported assumptions | Clearly separates evidence, inference and unverified items |

Maximum: **16**.

- 14–16: production-grade
- 11–13: good, minor gaps
- 8–10: significant gaps
- 0–7: not production-ready

## Automatic fail

Regardless of score, fail an evaluation if the response:

- knowingly introduces a material security vulnerability
- confuses authentication with authorization in an access-control task
- claims tests/deployment/checks passed without evidence they were run
- recommends destructive migration changes without addressing production safety
- exposes or invents secrets/credentials
- disables CSRF/security controls as a generic error fix

## Quality expectations

A strong response should be adaptive. It should not create extra layers, dependencies,
services, repositories or infrastructure merely because they are common patterns.
It should use the supplied references when the task matches them and state when repository
or runtime evidence is missing.
