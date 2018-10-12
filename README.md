# Manifesto

What I would like to see in a company that I work for.

### Git
- [x] 1 commit per change, do squash
- [x] do not create massive pull requests, they are hard to review, split your work
`We try to keep the PR small. There has been cases where we got large PR's which got raised in the retro's`
- [x] rebase instead of merge
`We squash and merge our PR, on Feature branches we merge from production, since the PR gets squash our PR's`
- [x] pull request must have 2+ approvals
`Only one approval is enforced`
- [x] master is read-only, it's a rule. always. no exceptions.
`Yes, its protected`
- [ ] delete branches after a merge
`We do delete them`
- [ ] use release tags
`No, we have continuos delivery setup and we don't use release tags`
- [x] no global history changes
`No force push allowed as the branch is protected`
- [x] commit message format - use commitizen or something similar
`We have a format defined, but not enforced.`
- [ ] use git LFS or mercurial for large files
`Did not face this yet`
- [x] run tests before pushing 
`We have git commit hooks setup`
  - be careful with git hooks
`What wrong here -- git precommit hook is only used`
### CI
- [ ] auto-revert on failure
`We don;t have this setup, its manual`
- [x] run at any commit
`Yes`
- [x] CI plan in git
`Yes -- we use Shippable and looking to move to CircleCI`
- [x] warn about formatting verification
`Yes - we fail our build if linting rule is not respected`
- [ ] warn about coverage illness
`Yes, more recently setup`
- [x] track test failures and flakiness
`Yes, but its manual. No smart tool setup that analyses test outputs`
- [x] store build logs for 3+ months
`Yes, all in shippable`
- [x] locally reproducible builds
`Yes -- we use docker`
- [x] automate builds using makefiles, gulp etc.
`Yes -- we use basic npm`

### Code health
- [ ] document your code
`We write code that is readable, so no need to extra documentation`
- [ ] docs are generated from the code
`No, we want to build our api documentation`
- [x] use linters and code analysis all the time
`yes -- we follow airbnb linting`
- [x] fork instead of hack
`we avoid hacks, but sometime have to`
- [x] touch legacy, often - it becomes non-legacy faster
`yes, the idea is that code should not look the same in 3~6 months`
- [x] remove old code
`try to, many times`
- [x] do not keep commented out code
`our linting rules checks that`
- [ ] use TODO, BUG, XXX in code - jumping to the issue tracker can be minimised
`no, we dont write comments in our code, but do use a issue tracker`
- [x] no experiments in the master
`why not, its good to have 
- [ ] allow to change log-level on the fly - this will simplify production's debug routine
`something we need to do`
- [x] limit your log file, 'cause it might grow unlimited
`yes`
- [x] store your config in /etc/myapp and logs in /var/log/myapp
`all logs are aggregated, but don;t know the location of the folder. Its actually local to the app and not outside of the app`
- [x] all modules must have the same structure
`yes`
- [x] if you can’t show a bottleneck, don’t start to optimise it - it might be interesting and challenging, but useless
`no pre-mature optimizations, we dont have that much time`

### Database
- [x] keep models normalized
- [x] think about your data - don't use SQL/NoSQL without a reason
`We mostly use sql, but have used json based fields in mysql`
- [x] use timestamp to store a date/time
- [x] log slow queries
- [x] don't put business logic into db or at least make it loosely coupled

### Dependencies
- [x] add with care, only when you're using *most* of the features
- [x] bump libs on a permanent basis
- [ ] have a local cache-server with deps
`It happens automatically by yarn`
- [x] pin your dependencies to a specific version
- [ ] prefer mature technology, rather then hyped one
`Its subjective, some say nodejs is hyped compared to c# etc.`

### Tests
- [x] use one test framework - a similar environment is better
- [x] show results, not just stack traces - some failures are obvious with visible result
- [x] isolate tests
- [ ] parallelize tests
`looking to do`
- [x] TDD
`we do write tests, but prefer writing api level tests`
- [x] measure code coverage
`only as an indicative`
- [x] test your backups

### Team
- [ ] pair programming
`no, we dont do pair programming, but do peer reviews`
- [x] high-level stand-ups, time bounded
`yes`
  - less info about irrelevant stuff
- [x] 2-3 week sprints
`one week sprints`
- [x] have an achievable sprint goal
`yes`
- [x] per sprint roles
- [x] only urgent topics are face-to-face
- [x] friendly atmosphere
  - no insulting jokes, no trolling, respectful environment
- [ ] 'coding rockstar' - it is a demotivation, not an inspiration
`no hero culture, so agreed`
- [x] if you're on vacations - specify date range
  - it'll be easier to find someone else or postpone the question
- [x] FAQ for newcomers
  - 30-day plan with all stuff that they should accomplish
 `our onboarding plan is not that mature, we do have a quick start guide`
- [ ] all features must be protected by feature flag
  - in case of accident it will(might) be enough to turn it off
`We don;t do feature by abstraction as a practice`
### Meetings
- [x] I can skip if I'm out of scope
  - do not waste team and own time
- [x] if you're organising a meeting - prepare an agenda
  - to have a way how to drive a meeting
- [x] action points after the meeting
  - who does what and when
- [x] avoid bus factor as much as possible
  - moving/cancelling unimportant meeting because of 1 person is a bad sign

### Communication
- [x] use the best apps
  - fast, flexible, pleasurable
- [x] outcomes of important discussions should be saved - better visibility for decisions
- [x] only important notifications
  - @all should be rare for irrelevant updates
- [x] easy access to any team room
- [] do not delete personal chats with inactive users
`we delete the account, so if it deletes the chat maybe too`
- [x] closed ticket must contain a link to the changes
  - every change must be easy accessible and visible for others

### Permissions
- [x] Git, CI, SSH read-access to everything
  - reading server logs cannot cause troubles
- [x] SSO to anything
  - better organisation of credentials
- [x] each office should have global admin
  - different timezones are a bottleneck
- [x] ability to start/stop a job on CI
  - waiting for an approval to make this action is a horrible bottleneck

### Space
- [x] engineers apart from non-engineers
  - fire & ice
- [] quiet open-space
  - someone might be sensitive to a noise...
`our office spaces are open plans and it sometimes gets noisy`
- [x] quiet zones
  - ...really sensitive
- [ ] the kitchen isn't for chill-out
  - the play room is a thing
 `We dont have a play room, but people find space for chilling out`
- [x] nothing smelly near working area
  - even coffee/cinnamon/mowed grass might irritate

### Network
- [ ] VPN access from home
  - work from home is a cool thing
- [x] Wifi must work all the time
  - obvious
- [x] LAN must be even more stable
  - uber-obvious

### Life
- [x] how often should my salary be reviewed?
  - worth asking
 `bi - annually typically`
- [x] work from home is a must have
  - family, health, even weather might be a reason
- [ ] educational budget to anything related to dev stuff
  - I would like to learn new technologies, why not?
`still looking to setup a training budget`
- [x] allow committing to the open-source
  - company_karma++
- [x] skipping team events must be acceptable
  - well...obvious
- [ ] 20% time is a vacation like time
  - creating anything that might help someone is awesome
 `no, we dont have that kind of policy. `
- [x] brown bags sessions must be rewarded
  - sharing knowledge is the best way to inspire
- [ ] monthly geek swag <3
  - t-shirts, hoodies and all other stuff
  `no, we have swags for events etc`
- [x] health food in the kitchen
  - candies are cool, but I would like to live longer
