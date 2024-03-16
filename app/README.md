# Quick Install

Documented by [The Model.earth Project Team](/io)
[Earthscape](../) is a fork of [Chatbot UI](https://github.com/mckaywrigley/chatbot-ui) by [Nick Wrigley](https://twitter.com/mckaywrigley).  

## Local Setup

[Install Docker](https://docs.docker.com/get-docker/) if you don't have it on your computer yet.

Fork and clone our repo from [github.com/modelearth/earthscape](https://github.com/modelearth/earthscape/)

In your webroot run:

	git clone https://github.com/modelearth/earthscape.git earthscape &&
	cd earthscape

Start a virtual environment

	python3 -m venv .env.local &&
	source .env.local/bin/activate

NOTE: We're using .env.local since it's aready ignored in .gitignore.
Also, using .env resulted in: failed to load .env: read .env: is a directory.


TO DO: Try running without virtual evironment if other install steps fail.


## Run update

	npm run update

If you run a hosted instance you'll also need to run: 
TO DO: Add link on "hosted instance" to provide clarity.

	npm run db-push


Mac cmd. For Windows [see detailed steps](../)

	brew install supabase/tap/supabase

Start superbase and fill secrets:

	supabase start &&
	cp .env.local.example .env.local &&
	supabase status


Add some global API Keys in the file: .env.local.example
NOTE: [Hosted site](https://www.chatbotui.com) seems to only work with a ChatGPT key.

## Run NextJS on Github

Next, add steps for hosting NextJS


## Current Errors

Errors are occurring because Docker was not yet configured.
Please add Docker setup info above.

npm run update
failed to connect to postgres: failed to connect to host=127.0.0.1 user=postgres database=postgres: dial error (dial tcp 127.0.0.1:54322: connect: connection refused)

supabase start
failed to start docker container: Error response from daemon: Mounts denied: approving /Users/helix/Library/Data/earthscape/supabase/functions: file does not exist

supabase status
Error response from daemon: No such container: supabase_db_chatbotui