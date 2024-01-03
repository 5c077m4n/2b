- `fish_user_key_bindings`: this is called *after* the shell's keybindings are set
example function:
```shell
# ga.fish

function ga --description 'Stages files'
    git add $argv
end
```
This allows to run `ga` as `git add` in the terminal
