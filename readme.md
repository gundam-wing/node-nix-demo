Just a little simple node js example nix devshell.

run `direnv allow` to "trust" the envrc and use the nix flake when cd-ing into the directory.

To setup and enable "direnv"

1. install
```sh
nix profile install nixpkgs#direnv
```

2. add to ~/.config/fish/config.fish

```sh
direnv hook fish | source
```

