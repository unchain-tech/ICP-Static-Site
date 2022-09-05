# About The Project

A personal website hosted on the blockchain.

The URL to deploy to is here: https://n5znu-6iaaa-aaaag-aatoa-cai.ic0.app

<img width="1440" alt="home" src="https://user-images.githubusercontent.com/60546319/188449469-0e19a47c-eaff-4d08-a59c-6693cbfd74b6.png">

<img width="1440" alt="aboutme" src="https://user-images.githubusercontent.com/60546319/188449518-2f91a97d-285e-4f1e-a13f-c14dcb591f8e.png">

<img width="1440" alt="port" src="https://user-images.githubusercontent.com/60546319/188449547-2caedfe0-b492-44fd-84ac-ec7350f0aa48.png">

# Chain deployed to: `IC`

# Description

## Stack description

- JavaScript

- Svelte

  Tools for building UI.

- tailwind CSS

  CSS Frameworks.

- dfx

  Tools to create, deploy and manage Dapps to be developed on IC.

## Directory structure

- `src/`

  - `assets/`

    Contains images used for the website

  - `lib/`

    Contains the components that make up the website.

    - `About.svelte`: Compose the profile section.
    - `Footer.svelte`: Compose the footer.
    - `Home.svelte`: Compose the home.
    - `Nav.svelte`: Compose the navigation bar. Contains in-page links to HOME, ABOUT ME, and PORTFOLO.
    - `Portfolio.svelte`: Compose the portfolio. URL to the official UNCHAIN site is used as a dummy.

  - `App.svelte`

    The main component of the application. This file imports the svelte file in the `lib/`.

  - `main.js`

    Files to be loaded directly into `index.html`. Import `App.svelte` and `app.css`.

- `canister_ids.json`

  A configuration file mapping the name and ID of deployed canisters. Generated when the command `dfx deploy` is executed.

- `dfx.json`

  Configuration file for building a project for the Internet Computer Blockchain.

- `postcss.config.cjs`, `tailwind.config.cjs`

  tailwind CSS configuration file

## Code walk-through

### Canister setup

Describe in a `dfx.json` file.

```json
{
  "canisters": {
    "website": {
      "type": "assets",
      "source": ["dist"]
    }
  }
}
```

- `"website"` is the name you give to the canister.

  ex) When looking up the ID of a canister

  ```bash
  dfx canister --network ic id website
  ```

- `"type":` specifies the type of canister.
- `"source":` specifies the directory to be used for static assets.

# References

Internet Computer

- [Hosting a Static Website on the Internet Computer](https://internetcomputer.org/docs/current/samples/host-a-website)
- [Deploy a "Hello World" Dapp in 10 Minutes](https://internetcomputer.org/docs/current/developer-docs/quickstart/hello10mins)
- [Network deployment](https://internetcomputer.org/docs/current/developer-docs/quickstart/network-quickstart)

Svelte

- [docs](https://svelte.dev/docs)
