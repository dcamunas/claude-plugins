# claude-plugins

The `dcamunas` marketplace for Claude Code: `.claude-plugin/marketplace.json` lists each plugin, pinned to a release
of its own repository. Public on GitHub (MIT).

## Rules for any session in this repo

1. **Everything is in English and public**: catalogue, README, commits. No personal data, no names of employers or
   clients, no paths of this machine.
2. **A pin moves only to a published release**: `ref` is the plugin's tag and `sha` the commit that tag points to
   (`git -C ../<plugin> rev-list -n 1 <tag>`), both changed in the same commit, titled `Pin <plugin> v<x.y.z>`. Never
   a branch: a push to a plugin's `main` must not reach anyone's machine by itself.
3. **The README table follows the catalogue**: a plugin added, removed or redescribed changes both in one commit.
4. **Check before pushing**: the JSON parses (`python3 -m json.tool .claude-plugin/marketplace.json`) and the tag
   resolves to that commit on GitHub (`gh api repos/dcamunas/<plugin>/commits/<tag> -q .sha`).
