# agent

Agent is a set of zshell scripts (`agent` and `agentc`) for interfacing with Mistral's [Codestral](https://mistral.ai/news/codestral-2501).

## Installation

After running the requirements, use the `Makefile`

    $ git clone https://github.com/keegnotrub/agent
    $ cd agent
    $ sudo make install

## Requirements

Login to Mistral's [La Plateforme](https://console.mistral.ai/codestral) and setup an API key from the "Codestral" page.

    $ open https://console.mistral.ai/codestral
    $ echo 'export CODESTRAL_API_KEY="your_api_key"' >> $HOME/.zprofile
    
Install the needed binaries in your package manager of choice.

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
    $ cat app/models/user.rb | agent rails improve

## Usage `agentc`
    
    $ agentc <cursor>

    Use cursor to provide the position for completion within text.

    Text should be piped to the agent for completion.
    $ cat app/models/user.rb | agentc 732
