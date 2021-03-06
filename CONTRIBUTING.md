# Contributing to Athens

Not convinced you want to learn Clojure? Read this developer's [first month experience report](https://www.notion.so/athensresearch/Why-you-should-learn-Clojure-my-first-month-as-a-Clojurian-87e265099b1140d5b64ea503efab861c).

No Clojure or programming experience? No worries. Read this [guide](https://www.notion.so/athensresearch/Onboarding-for-New-Clojurians-b34b38f30902448cae68afffa02425c1), join our Discord, and we'll find you a Clojure learning partner.

Issues tagged "[good first issue](https://github.com/athensresearch/athens/issues?q=is%3Aopen+is%3Aissue+label%3A%22good+first+issue%22)" are... good first issues.

# Development Environment

These dependencies are needed to get Athens up and running. Follow the instructions in the links.

1. [java 11 and lein](https://purelyfunctional.tv/guide/how-to-install-clojure/) (lein installs Clojure)
1. [node 12](https://nodejs.org/en/download/) and [yarn](https://classic.yarnpkg.com/en/docs/install/#mac-stable)

After you've got these dependencies, clone the git repository to your harddrive:
```
git clone https://github.com/athensresearch/athens.git
```
Then `cd athens/` and run the following commands.

Pull javascript dependencies:
```
yarn
```

Pull java dependencies and build with:
```
lein dev
```

When these scripts are done, your terminal will read `build complete`. Athens can be accessed by pointing a browser to `localhost:3000` on UNIX or `127.0.0.1:3000` on Windows.

# Clojure Style Guide

We are linting Clojure code using [clj-kondo](https://github.com/borkdude/clj-kondo). Our clj-kondo configuration is in [`.clj-kondo/config.edn`](.clj-kondo/config.edn).

For this linting to work, you will need to install `clj-kondo`. Instructions are in [`clj-kondo`’s installation guide](https://github.com/borkdude/clj-kondo/blob/master/doc/install.md) ([permalink](https://github.com/borkdude/clj-kondo/blob/7e7190b0bf673a6778c3b2cbf7c61f42cd57ee03/doc/install.md)).

To see the problems reported by clj-kondo, run `script/lint`. Your editor may also be able to integrate with clj-kondo’s output. For example, if you use [Calva](https://marketplace.visualstudio.com/items?itemName=betterthantomorrow.calva) for VS Code, then clj-kondo’s messages are reported in the Problems panel.

# Git Style Guide

## Commits

Follow guidelines from [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/). Specifically, begin each commit with one of the following types:


```
build:
ci:
chore:
docs:
feat:
fix:
perf:
refactor:
revert:
style:
test:
```

After you specify the type, write a declarative statement in the present tense explaining what you did. Add additional detail in bullets below the header. Example:

```
feat: implement new right side bar

- see issue for details on CSS library
- TODO: fix padding
```

## Issues

Do not just write an issue because you have a question/problem. If you think you are missing some information, ask in the #engineering or #learning channel of the Discord.

On the other hand, if you believe there is an issue with source code, please write an actionable issue with this [template](https://github.com/athensresearch/athens/issues/new?title=Descriptive+issue+title&body=%23%23%23%23+Description%0AA+clear+and+concise+description+of+what+the+issue+is+about.%0A%0A%23%23%23%23+Screenshots%0A!%5BShaq+Kitty+Wiggle%5D(https://media.giphy.com/media/13CoXDiaCcCoyk/giphy.gif)%0A%0A%23%23%23%23+Files%0AA+list+of+relevant+files+for+this+issue.+This+will+help+people+navigate+the+project+and+offer+some+clues+of+where+to+start.%0A%0A%23%23%23%23+To+Reproduce%0AIf+this+issue+is+describing+a+bug,+include+some+steps+to+reproduce+the+behavior.%0A%0A%23%23%23%23+Tasks%0AInclude+specific+tasks+in+the+order+they+need+to+be+done+in.+Include+links+to+specific+lines+of+code+where+the+task+should+happen+at.%0A-+%5B+%5D+Task+1%0A-+%5B+%5D+Task+2%0A-+%5B+%5D+Task+3%0A%0ARemember+to+use+labels.).

Better yet, submit a pull request.

## Pull Requests

If your PR is related to other issue(s), reference it by issue number. You can close issues smoothly with [Github keywords](https://help.github.com/en/enterprise/2.16/user/github/managing-your-work-on-github/closing-issues-using-keywords):

```
close #1
fix #2
resolve #2
```

Those with merge permissions should "Squash and Merge" as a general rule of thumb. This makes reverts easier if they are needed.
