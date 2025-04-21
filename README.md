# agent

Agent is a set of zshell scripts (`agent` and `agentc`) for interfacing with Mistral's [Codestral](https://mistral.ai/news/codestral-2501).

## Installation

After running the requirements, use the `Makefile`

    $ git clone https://github.com/keegnotrub/agent
    $ cd agent
    $ sudo make install

## Requirements
    
    # Macports
    $ sudo port install jq

    # Homebrew
    $ brew install jq

## Usage `agent`

    $ agent <skill> <command>
    
    These are the available agent skills:
    rails     Ruby on Rails
    react     React
    web       Web

    These are the agent commands used in various situations:
    ask       Ask anything
    debug     Debug an error
    explain   Explain code
    improve   Improve code

    Text should be piped to the agent for context.
    $ cat app/models/user.rb | agent rails check

## Usage `agentc`
    
    $ agentc <cursor>

    Use cursor to provide the position for completion within text.

    Text should be piped to the agent for completion.
    $ cat file.txt | agentc 732
