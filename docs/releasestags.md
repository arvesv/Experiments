# My way of doing releases on Git/GitHub

These are my *current* beliefs about how a software project should be organized and tagged in Git/Docker etc - This will change :smiley:

* We should do [Trunk Based Development](https://trunkbaseddevelopment.com/). The main reason is that a living branch requires work (in testing, merge resolution, context switching) so we should have as few as possible.
    1. The trunk branch should always working and be in a releasable state
    2. Use feature flags to hide things under development
    3. You can do automatically validated pull requests, but no long blocking for pushing to trunk.
* A release should be a tag
    1. You can trigger workflows on tags and reuse the tag on Docker images.
    2. The tag and the commit sha should be embedded in the artifacts so you can check what version you are running on.

