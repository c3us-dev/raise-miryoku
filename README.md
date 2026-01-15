# raise-miryoku
A slightly modified miryoku qwerty layout for use with the dygma raise. Shooting for the balance between the ergonomic customization provided by sensible virtual layers and "someone could use my keyboard at work real quick if they had to" accessibility with a familiar row-staggered base QWERTY layout.

## helpers
To keep the JSON config easy to read/parse with `git diff`, a pre-commit hook was added so the `pretty-format-json` formatter will rewrite the single-line JSON output Bazecor will write-out by default.

**to set it up:**
```bash
uv tool run pre-commit install
```

**to run manually for all repo .json files:**
```bash
uv tool run pre-commit run --all-files
```