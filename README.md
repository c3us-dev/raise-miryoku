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

## additional notes
To save space on the neuron, macro, layer, and superkey names aren't saved so cross platform/device use of the `raise.json` main export file with Bazecor will not preserve labels and certain config parameters. 

In order for this to be captured, the Bazecor level `config.json` has to be transferred and updated as well. I will try and smooth out this process with a script/hook, but for now the locations are typically as follows:

- On Linux:
>`/home/<user_name>/.config/Bazecor/config.json`
- On Windows:
>`C:\Users\<user_name>\AppData\Roaming\Bazecor\config.json`