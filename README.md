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

### `App`

Expands to a basic Leptos `App` component. It only includes the component structure,
not the imports. For imports, see [`use App`](#use-app) below.

```rust
#[component]
pub fn App() -> impl IntoView {
    provide_meta_context();

    view! {
        <Title text="Welcome to Leptos"/>

        <Router>
            <main>
                <Routes fallback=|| "Page not found.".into_view()>
                    <Route path=StaticSegment("") view=HomePage/>
                </Routes>
            </main>
        </Router>
    }
}
```

### `use App`

Expands to the necessary imports for using the [`App`](#app) code snippet.

```rust
use leptos::prelude::*;
use leptos_meta::{provide_meta_context, Title};
use leptos_router::{
    components::{Route, Router, Routes},
    StaticSegment,
};
```

### `shell()`

Expands to a basic Leptos `shell` function.

```rust
pub fn shell(options: LeptosOptions) -> impl IntoView {
    use leptos_meta::MetaTags;

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

### `Router`

Expands to a basic Leptos `Router` setup. It includes only a simple router
structure, not including the imports. For imports, see [`use Router`](#use-router)
below.

```rust
<Router>
    <main>
        <Routes fallback=|| "Page not found.".into_view()>
            <Route path=StaticSegment("") view=HomePage/>
        </Routes>
    </main>
</Router>
```

### `use Router`

Expands to the necessary imports for using the [`Router`](#router) code snippet.

```rust
use leptos_router::{
    components::{Route, Router, Routes},
    StaticSegment,
};
```

[Leptos]: https://leptos.dev
