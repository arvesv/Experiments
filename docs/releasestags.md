# My way of doing releases on Git/GitHub

These are my ~current~ beliefs about gow a software project should be organized and tagges in Git/Docker etc. This will probably change :smiley:

* You should do [Trunk Based Development](https://trunkbaseddevelopment.com/). My main reason is that a living branch requires extra work (in testing, merge resolution, context switching) so we should have as few as possible. The principles are:
    1. The trunk branch should always working and be in a releaseable state
    2. Use feature flags to hide things under development
    3. You can do automatically validated pull requests, but no long blocking for pushing to trunk.
* A release should be a tag
    1. You can trigger workflows on tags and reuse the tag on Docker images.
    2. Tags are more immutable(!) than branches
    