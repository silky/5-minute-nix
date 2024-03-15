---
title: Nix in 5 minutes!
author: Noon
patat:
  theme:
    codeBlock: [onDullWhite]
    emph:      [italic]
    strong:    [bold]
  incrementalLists: true
  margins:
    left: 10
    right: 10
    top: 3
  images:
    backend: auto
---

Hello! :)


---

# Let's try and cover Nix in 5 minutes

- Nix - <https://nixos.org>
    - Package manager,
    - Build tool,
    - Operating system!
- Let's go!

---

# ~1st minute: Package manager

- Want to use Python?

    ```
    > nix-shell -p python310
    > nix-shell -p python311
    ```

- JavaScript?

    ```
    > nix-shell -p nodejs
    ```

- qgis?

    ```
    > nix-shell -p qgis
    ```

- Python + Jupyter + Pandas

    ```
    > nix-shell -p "python311.withPackages ( ps: [ ps.jupyter ps.pandas ] )"
    ```

- Suggestion?

- nixpkgs: <https://search.nixos.org>

---

# ~2nd minute: Build tool

- To do development you need many things
    - Python packages
    - System-level libraries
    - Linters, Formatters, ...
    - Not necessarily in the same language

- *devShells*: Set up a shell with all of that
    - **Dream**: Compatible with existing language package-management
    tooling: poetry, pyproject, npm, cargo, bundler (ruby), ...
    - **Reality**: Often requires manual hacking

- Can be extremely convenient

    ```
    > nix run github:ERGO-Code/HiGHS/latest
    ```

- And powerful?

    ```
    > nix run github:matthewcroughan/NixThePlanet#win98
    ```

---

# Final minutes: Pros/Cons

- Cons:
    - Often requires a bit of overhead
    - Errors can take some getting used to
    - Documentation moderately poor
- Pros:
    - Makes explicit work that tends to be implicit
    - Large and growing ecosystem
    - "Probably" good support for what you want
    - _Can_ make up the difference by hacking
    -  "Basically" eliminates "Works On My Machine"
        - ... unless, your architecture isn't supported!
    - Very fast dev environment
    - High confidence of reproducibility
    - Caching, shared builds
    - Deployment
    - Ease of CI
    - ...
- Links
    - <https://nixos.org>
    - <https://2li.ch/blog/2024-03-10-how-we-replaced-vagrant-with-devenv>
    - <https://devenv.sh/>
    - <https://github.com/Gabriella439/nixos-in-production/>
    - <https://scrive.github.io/nix-workshop/>
    - I've learned a lot from GitHub searching 😅
- Thanks!

---
