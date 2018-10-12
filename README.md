# Manifesto

What I would like to see in a company that I work for.

### Git
- [ ] 1 commit per change, do squash
- [ ] do not create massive pull requests, they are hard to review, split your work
- [ ] rebase instead of merge
- [ ] pull request must have 2+ approvals
- [ ] master is read-only, it's a rule. always. no exceptions.
- [ ] delete branches after a merge
- [ ] use release tags
- [ ] no global history changes
- [ ] commit message format - use commitizen or something similar
- [ ] use git LFS or mercurial for large files
- [ ] run tests before pushing 
  - be careful with git hooks

### CI
- [ ] auto-revert on failure
- [ ] run at any commit
- [ ] CI plan in git
- [ ] warn about formatting verification
- [ ] warn about coverage illness
- [ ] track test failures and flakiness
- [ ] store build logs for 3+ months
- [ ] locally reproducible builds
- [ ] automate builds using makefiles, gulp etc.

### Code health
- [ ] document your code
- [ ] docs are generated from the code
- [ ] use linters and code analysis all the time
- [ ] fork instead of hack
- [ ] touch legacy, often - it becomes non-legacy faster
- [ ] remove old code
- [ ] do not keep commented out code
- [ ] use TODO, BUG, XXX in code - jumping to the issue tracker can be minimised
- [ ] no experiments in the master
- [ ] allow to change log-level on the fly - this will simplify production's debug routine
- [ ] limit your log file, 'cause it might grow unlimited
- [ ] store your config in /etc/myapp and logs in /var/log/myapp
- [ ] all modules must have the same structure
- [ ] if you can’t show a bottleneck, don’t start to optimise it - it might be interesting and challenging, but useless

### Database
- [ ] keep models normalized
- [ ] think about your data - don't use SQL/NoSQL without a reason
- [ ] use timestamp to store a date/time
- [ ] log slow queries
- [ ] don't put business logic into db or at least make it loosely coupled

### Dependencies
- [ ] add with care, only when you're using *most* of the features
- [ ] bump libs on a permanent basis
- [ ] have a local cache-server with deps
- [ ] pin your dependencies to a specific version
- [ ] prefer mature technology, rather then hyped one

### Tests
- [ ] use one test framework - a similar environment is better
- [ ] show results, not just stack traces - some failures are obvious with visible result
- [ ] isolate tests
- [ ] parallelize tests
- [ ] TDD
- [ ] measure code coverage
- [ ] test your backups

### Team
- [ ] pair programming
- [ ] high-level stand-ups, time bounded
  - less info about irrelevant stuff
- [ ] 2-3 week sprints
  - have an achievable sprint goal
- [ ] per sprint roles
- [ ] only urgent topics are face-to-face
- [ ] friendly atmosphere
  - no insulting jokes, no trolling, respectful environment
- [ ] 'coding rockstar' - it is a demotivation, not an inspiration
- [ ] if you're on vacations - specify date range
  - it'll be easier to find someone else or postpone the question
- [ ] FAQ for newcomers
  - 30-day plan with all stuff that they should accomplish
- [ ] all features must be protected by feature flag
  - in case of accident it will(might) be enough to turn it off

### Meetings
- [ ] I can skip if I'm out of scope
  - do not waste team and own time
- [ ] if you're organising a meeting - prepare an agenda
  - to have a way how to drive a meeting
- [ ] action points after the meeting
  - who does what and when
- [ ] avoid bus factor as much as possible
  - moving/cancelling unimportant meeting because of 1 person is a bad sign

### Communication
- [ ] use the best apps
  - fast, flexible, pleasurable
- [ ] outcomes of important discussions should be saved - better visibility for decisions
- [ ] only important notifications
  - @all should be rare for irrelevant updates
- [ ] easy access to any team room
- [ ] do not delete personal chats with inactive users
- [ ] closed ticket must contain a link to the changes
  - every change must be easy accessible and visible for others

### Permissions
- [ ] Git, CI, SSH read-access to everything
  - reading server logs cannot cause troubles
- [ ] SSO to anything
  - better organisation of credentials
- [ ] each office should have global admin
  - different timezones are a bottleneck
- [ ] ability to start/stop a job on CI
  - waiting for an approval to make this action is a horrible bottleneck

### Space
- [ ] engineers apart from non-engineers
  - fire & ice
- [ ] quiet open-space
  - someone might be sensitive to a noise...
- [ ] quiet zones
  - ...really sensitive
- [ ] the kitchen isn't for chill-out
  - the play room is a thing
- [ ] nothing smelly near working area
  - even coffee/cinnamon/mowed grass might irritate

### Network
- [ ] VPN access from home
  - work from home is a cool thing
- [ ] Wifi must work all the time
  - obvious
- [ ] LAN must be even more stable
  - uber-obvious

### Life
- [ ] how often should my salary be reviewed?
  - worth asking
- [ ] work from home is a must have
  - family, health, even weather might be a reason
- [ ] educational budget to anything related to dev stuff
  - I would like to learn new technologies, why not?
- [ ] allow committing to the open-source
  - company_karma++
- [ ] skipping team events must be acceptable
  - well...obvious
- [ ] 20% time is a vacation like time
  - creating anything that might help someone is awesome
- [ ] brown bags sessions must be rewarded
  - sharing knowledge is the best way to inspire
- [ ] monthly geek swag <3
  - t-shirts, hoodies and all other stuff
- [ ] health food in the kitchen
  - candies are cool, but I would like to live longer
