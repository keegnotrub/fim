# fim

fim is a zshell script (`fim`) for interfacing with Mistral's [Codestral](https://mistral.ai/news/codestral-2501) for FIM completion.

## Installation

After running the requirements, use the `Makefile`

    $ git clone https://github.com/keegnotrub/fim
    $ cd fim
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

## Usage `fim`
    
    $ fim <cursor>

    Use cursor to provide the position for completion within text.

    Text should be piped to fim for completion.
    $ cat app/models/user.rb | fim 732
