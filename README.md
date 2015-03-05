# Best Practices


# Hosting
## Heroku
It doesn't run docker (yet), but fits my needs the best.
My current development procedure is this:

1. Create branch for feature and push to it
2. Create a PR for branch
3. Travis tests 
4. If travis passes, Heroku creates a new app for that branch and deploys my code

This last part is [in beta](https://devcenter.heroku.com/articles/github-integration-pull-request-deploys)
at heroku.

When I merge to master, i have it set up to deploy to my dev app.

Then when I finally wanna push to production, I use
[heroku pipeline](https://devcenter.heroku.com/articles/labs-pipelines)

# Development

## Docker
Obviously, use Docker. For everything.

## Docker-machine
Turns our there is this super nifty thing that is in
beta called docker-machine. It allows you to create and
switch between docker hosts very easily. For examples,
I can have one host in a virtual machine on my own computer
and another on digital ocean.

