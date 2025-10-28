# About

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

---

## General

### derivations

A derivation is a "blue print" to _realise_ a package
```sh
derivation ::
    { system   : String
    , name     : String
    , builder  : Path | Derivation
    , ?args    : [String]
    , ?outputs : [String]
    } -> Derivation
```

The string output of a derivation is always a Nix store path which includes an "input hash" computed from the inputs of the derivation.

```sh
/nix/store/          sglc12hc6pc68w5ppn2k56n6jcpaci16  my-package-1.0
1. Nix store prefix  2. Hash part                      3. Package name
```
