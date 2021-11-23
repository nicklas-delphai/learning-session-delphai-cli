
-> ⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢀⣀⡀⠀ <-
-> ⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⣢⣿⣿⣿⣹ <-
-> ⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠆⠿⣿⡿⠕ <-
-> ⠀⠀⠀⢀⣀⣨⣨⣨⣀⠀⢀⣨⣨⣨⡀ <-
-> ⠀⢀⣺⣿⣿⣿⣿⣿⣿⣿⣾⣿⣿⣿⡙ <-
-> ⢠⣿⣿⣿⣿⠟⠅⠅⠇⠷⣿⣿⣿⣿⡙ <-
-> ⢦⣿⣿⣿⡙⠀⠀⠀⠀⠀⢧⣿⣿⣿⡙ <-
-> ⢦⣿⣿⣿⡙⠀⠀⠀⠀⠀⢦⣿⣿⣿⡙ <-
-> ⠆⣿⣿⣿⣿⣨⣀⣀⣀⣪⣿⣿⣿⣿⡙ <-
-> ⠀⠆⢿⣿⣿⣿⣿⣿⣿⣿⢿⣿⣿⣿⡙ <-
-> ⠀⠀⠀⠄⠇⠗⠗⠗⠕⠁⠆⠗⠗⠗⠑ <-

-> # delphai-cli <-

-------------------------------------

# What is it?

* It provides utilities for common tasks
* It's written in typescript

-------------------------------------

# Agenda

* Demo on how to install
* Demo what some of the commands do
* Brief overview over the implementation

-------------------------------------

# How to install

1. Install pre-requisits
2. Configure access to private npm registry
3. Install it using yarn

-------------------------------------

# Dependencies

1. [yarn](https://yarnpkg.com/)
2. [azure-cli (az)](https://docs.microsoft.com/en-us/cli/azure/)
3. [poetry](https://python-poetry.org/docs/)
4. [kubectl](https://kubernetes.io/docs/tasks/tools/)
5. [kubectx](https://github.com/ahmetb/kubectx)

## For Arch

`yay -S yarn python-poetry azure-cli kubectl kubectx`

-------------------------------------

# Access to private npm registry

https://wiki.delphai.dev/wiki/Private_npm_registry

-------------------------------------

# Install delphai-cli

`yarn global add @delphai/delphai-cli`

-------------------------------------

# Init command

Initialize new repositories for python and react projects.

`delphai init -l=python [NAME]`

-------------------------------------

# Ctx command

Control the kubernetes and azure context global to your machine.

## Pre-requisits

`az login` -> authenticate your machine with Azure

## Common

`delphai ctx` -> list all subscriptions
`delphai ctx \[SUBSCRIPTION\]` -> change context to a subscription
`delphai ctx --login \[SUBSCRIPTION\]` -> Change context and update kubeconfig

-------------------------------------

# Secrets command

Get kubernetes secrets for your currently set context.

`delphai secrets` -> get secrets for default namespace
`delphai secrets --namespace=[NAMESPACE]` -> get secrets for a particular namespace

-------------------------------------

# Implementation

https://github.com/delphai/delphai-cli

* [oclif](https://github.com/oclif/oclif): CLI framework for nodejs
* [plop](https://github.com/plopjs/plop): Ties together user prompts, execution steps and file templating

-------------------------------------

# Make it better

* An [epic](https://atomleap.atlassian.net/browse/V1-4544) exists to gather all open tickets
* Can you think of anything you would like to see in delphai-cli?
  -> Create a ticket.
  -> Plan the ticket and implement it.

-------------------------------------

-> # Questions <-
