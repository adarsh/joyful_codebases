"How to Make Your Codebase a Joyful Place"
6/7/2016

Outline
========

Introduction
------------
* My goals for today:
  - I'm going to talk about best practices, why they are important, how to agree on them as a team, and then how to automate them.
  - Throughout the talk I will spice things up with polarizing style guide opinions.
* Are we happy at work?
  - Do we love what we do? Yes! Being a developer is great. But... it can drive you nuts.
  - Do we love the codebases that we work in? Why or why not?
* What makes a codebase less enjoyable to work in?
  - "The code is bad."
  - "It's inconsistent."
  - "People don't care."
  - "No one wrote down anything."
  - "Whoever wrote this is an idiot. (don't say this!)"


How to Agree on Team Norms
--------------------------
* Step 0 - Agree they are important
  - Determine which best practices are valuable for our team.
      "Well, Code Review is important but TDD is not..."
      "'best' practices are relative to your team, _maybe_ your community."
  - What kind of culture do we want? Hostile? Passive? Proud?
  - Talk about why this is hard: Pride/arrogance, feeling dumb, history, business problems, individuality, Ruby.
  - We want to be better at our jobs. Continuous Improvement is the Toyota Way.
  - The process is more important than the result. Knowledge transfer, increased team awareness, Finding alternative solutions. Resource: [Derek Prior's talk on implementing a code review culture][1].
  - Draw a picture of where we want to go as an organization.
  - You must have leadership buy-in, which may mean adopting their style (to start).
  - Adopt an experimental, "let's try it out!" attitude.

* Figure out how to discuss and agree on norms.
  - Document everything, ideally in GitHub.
  - Make them public!
  - Agree on a democratic approach, with a tiebreaker.

* Start with one thing, then slowly build.
  - Find one thing that everyone already agrees on, and codify it.
  - Find one thing no one agrees on, and open a PR.

* When you agree on something, automate it
  - (next section)

[1]: https://www.youtube.com/watch?v=PJjmw9TRB7s


How to Automate Team Norms
--------------------------
* I'm going to ignore monitoring things (uptime, errors, ops-y stuff)

* Git Hooks
  - overcommit gem! (https://github.com/brigade/overcommit)
* Code Quality
  - This is _not_ really a subjective thing, but you can pretend it is to make things better.
  - Automations (OSS): [flog][3], [flay][2], [reek][4]
  - Automations (paid): [CodeClimate][3], [Scrutinizer][2], [SensioLabs Insight][4] Codacy (https://www.codacy.com/)
* Testing
  - Assuming you are writing tests, they should be green.
  - Automations (OSS): SimpleCov
  - Automations (paid): Circle, Travis
* Style Guides
  - Silicon Valley Gif.
  - Hound, Codacy, RuboCopkkkk
* Updating your Gems
  - https://www.deppbot.com/
* Security
  - Brakeman, bundler-audit

[2]: https://scrutinizer-ci.com/
[3]: https://codeclimate.com/
[4]: https://insight.sensiolabs.com/


Polarizing Style Opinions
-------------------------
Groan if you hate this, snap if you like it.

* Spaces are better than tabs (for Ruby, we use a lot of editors)
* Keyword arguments should always be used.
* Private `attr_readers` are awesome.
* One line methods are preferrable
* Trailing conditionals are terrible surprises.
