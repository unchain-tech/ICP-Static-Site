# About The Project

A personal website hosted on the blockchain.

The URL to deploy to is here: https://n5znu-6iaaa-aaaag-aatoa-cai.ic0.app

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

    Contains images used for the website.

  - `lib/`

    Contains the components that make up the website.

  - `App.svelte`

    The main component of the application. This file imports the svelte file in the `lib/`.

- `canister_ids.json`

  A configuration file mapping the name and ID of deployed canisters. Generated when the command `dfx deploy` is executed.

- `dfx.json`

  Configuration file for building a project for the Internet Computer Blockchain.

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
- `"type":` specifies the type of canister.
- `"source":` specifies the directory to be used for static assets.

# References

Internet Computer

- [Hosting a Static Website on the Internet Computer](https://internetcomputer.org/docs/current/samples/host-a-website)
- [Deploy a "Hello World" Dapp in 10 Minutes](https://internetcomputer.org/docs/current/developer-docs/quickstart/hello10mins)
- [Network deployment](https://internetcomputer.org/docs/current/developer-docs/quickstart/network-quickstart)

Svelte

- [docs](https://svelte.dev/docs)
