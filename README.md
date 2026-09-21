## Test & CI assurance for AI-generated codebases

Your build is green. I measure whether that green means anything.

A gate that does not bite is not a gate. What I look for are checks that report success
without having checked anything: a step that goes green on a `404`, a suite that crashes
before it writes a result, a mutant that no test kills.

### Evidence rather than claims

- A release step in a Rust project could go green on a `404` and record the SHA of the error response. I reported it; the maintainer wrote and merged a fix within three days — [unhappychoice/gitlogue#236](https://github.com/unhappychoice/gitlogue/issues/236)

- My own CI once ran 58 test scenarios, crashed before writing any result, and the step still reported success, because `continue-on-error` hides more than you expect — [Do not trust the green checkmark](https://dev.to/onurkesim/do-not-trust-the-green-checkmark-48i5)

- The mutants I use to check whether my own gates bite are public, not described — [hafiza-kur/faz0](https://github.com/onur-kesim/hafiza-kur/tree/main/faz0)

- A documentation patch of mine is in drift's develop branch, committed by the maintainer — [simolus3/drift@d9f88e5](https://github.com/simolus3/drift/commit/d9f88e5b27531cfcfcd198e0e440963198175801)

### What I am building

- **[hafiza-kur](https://github.com/onur-kesim/hafiza-kur)** — a portable project-memory gate system for AI agents. Ships with its own mutants, so the gates can be shown to bite.
- **[Momentum](https://github.com/onur-kesim/Momentum)** — offline-first task management, ASP.NET Core and Flutter, with sync and conflict resolution.
- **[epson-l3251-usb-reset](https://github.com/onur-kesim/epson-l3251-usb-reset)** — reading, backing up and resetting a printer's waste-ink counter over IEEE 1284.

### Caveats

23 years in technical acceptance and maintenance of high-tech systems, including auditing a
quality management system, but months, not years, in software. My code is mostly written by AI
(Claude Code); the design, the checks and the verdicts are mine. I have not worked inside a team
codebase or run a live system with real users. What I offer is a measurement, not seniority.

### Reach me

Erzurum, Turkey (UTC+3) · remote only · part-time (10–20 hrs/week), or a fixed-scope audit of a
test suite and its CI gates.

[Writing](https://dev.to/onurkesim) · onurkesimbjk@gmail.com
