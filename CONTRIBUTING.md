# Contributing to DecimalAnnex

Thank you for your interest in contributing to this implementation of decimal floating-point arithmetic!

## Reporting bugs

Have you observed unexpected behavior or obtained an incorrect result?
Reporting what you've found by [opening an issue][github-issue] on GitHub is a great way to help improve this project.

You may wish to check if someone else has already reported the same issue to decrease the chance of a duplicate.
When reporting your issue, be sure to give a concise description,
including the behavior you expected to observe and what you actually observed,
and a reproducible test case that demonstrates the problem (preferably reduced to as little code as required).
Where relevant, include information about the platform, compiler version, and deployment target.

[github-issue]: https://github.com/xwu/DecimalAnnex/issues

## Contributing code

It's recommended that you have some familiarity with the [IEEE 754][ieee-754] floating-point arithmetic standard
and with the Swift standard library, particularly its [`FloatingPoint`][floating-point-protocol] requirements
and concrete binary floating-point types, before contributing new code to the project.

Most guidelines for contributing to the Swift project itself can be assumed relevant to this project.
Do note that code in the core package doesn't rely on any unsupported language features.
For now, the `DecimalAnnex` façade uses a single `@_exported` import;
it's not anticipated that the project will expand its use of unsupported features any further than that.

Focused pull requests against the `main` branch that make a specific, bounded set of changes
without commingling unrelated edits will be easier to review and promptly accept.
Please ensure that any new code you contribute adheres to the prevailing code style in this project,
which generally aligns with the standard library's.

[ieee-754]: https://ieeexplore.ieee.org/document/8766229
[floating-point-protocol]: https://docs.swift.org/latest/documentation/swift/floatingpoint

### LLM usage policy

Your personal use of AI to understand, analyze, verify, and review code is permitted and even encouraged.
Numerous bugs that are subtle for the human eye are easily caught and remediated with a modern LLM.

In no case should such tools be used as substitutes or ghostwriters for human review and comment:
that is, when replying to a discussion or reviewing others' code, it is not acceptable to take on the role
of an intermediary between someone else and your own tooling.

This project maintains the essential expectation that named authors maintain line-by-line authorial control
over any code they contribute. In some sense, it is immaterial what tooling was used to write that code:
merely mechanical transformations, for example, are neither intrinsically better nor worse if performed by a regex engine
using a well-crafted expression than if performed by an LLM using a clear natural language prompt.

It is non-optional, however, for human contributors to have a full understanding of what their code does
*and* how it does those things. AI tools are uniquely suited for prototyping alternative approaches
and for constructing test or benchmark harnesses; however, verbatim adoption of generated artifacts into the project
without human revision would likely be inconsistent with the essential expectation outlined above.
