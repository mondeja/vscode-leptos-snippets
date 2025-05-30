# Leptos code snippets for VSCode

Useful code snippets for [Leptos] framework development in VSCode.

## Installation

Install through VS Code extensions. Search for `Leptos Snippets`.

Can also be installed in VS Code. Launch VS Code Quick Open
(<kbd>Ctrl</kbd>+<kbd>P</kbd>), paste the following command,
and press <kbd>Enter</kbd>.

```sh
ext install mondeja.leptos-snippets
```

## Code snippets

### `#[component]`

- Start typing `comp` in a Rust file and you will see the snippet
  `#[component] Leptos component`.
- Select it and press <kbd>Enter</kbd> to start writing.
- Write the name of the component and press <kbd>Tab</kbd>.
- Write its documentation and press <kbd>Tab</kbd>.
- Write the `view!` body and press <kbd>Tab</kbd>.
- Write its code and press <kbd>Tab</kbd>.

<p align="center">
  <img alt ="#[component] expansion" src="https://raw.githubusercontent.com/mondeja/vscode-leptos-snippets/master/assets/component.gif">
</p>

### `#[server]`

- Start typing `serv` in a Rust file and you will see the snippet
  `#[server] Leptos server function`.
- Select it and press <kbd>Enter</kbd> to start writing.
- Write the name of the function and press <kbd>Tab</kbd>.
- Write its documentation and press <kbd>Tab</kbd>.
- Write the final match statement and press <kbd>Tab</kbd>.
- Write the function body and press <kbd>Tab</kbd>.

<p align="center">
  <img alt ="#[server] expansion" src="https://raw.githubusercontent.com/mondeja/vscode-leptos-snippets/master/assets/server.gif">
</p>

### `use leptos::prelude::*;`

Import the Leptos prelude. Expands to `use leptos::prelude::*;`.

### `shell()`

Generates a basic Leptos `shell` function. Expands to

```rust
pub fn shell(options: LeptosOptions) -> impl IntoView {
    view! {
        <!DOCTYPE html>
        <html lang="en">
            <head>
                <meta charset="utf-8"/>
                <meta name="viewport" content="width=device-width, initial-scale=1"/>
                <AutoReload options=options.clone() />
                <HydrationScripts options/>
                <MetaTags/>
            </head>
            <body>
                <App/>
            </body>
        </html>
    }
}
```

[Leptos]: https://leptos.dev
