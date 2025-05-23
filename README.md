# Leptos code snippets for VSCode

Useful snippets for [Leptos] framework development in VSCode.

## Installation

Install through VS Code extensions. Search for `Leptos Snippets`.

Can also be installed in VS Code. Launch VS Code Quick Open (Ctrl+P),
paste the following command, and press enter.

```sh
ext install mondeja.leptos-snippets
```

## Snippets

### `#[component]` expansion

1. Start typing `comp` in a Rust file and you should see the snippet
   `#[component] Leptos component`. Press <kbd>Enter</kbd> to insert it.
1. Write the name of the component and press <kbd>Tab</kbd>.
1. Write its documentation and press <kbd>Tab</kbd>.
1. Write the `view!` body and press <kbd>Tab</kbd>.
1. Write its code and press <kbd>Tab</kbd>.

<p align="center">
  <img alt ="#[component] expansion" src="https://raw.githubusercontent.com/mondeja/vscode-leptos-snippets/master/assets/component.gif">
</p>

[Leptos]: https://leptos.dev
