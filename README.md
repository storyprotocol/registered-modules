# Story Registered Modules

Welcome to the repository for Story's registered modules. This repository serves as a comprehensive list of both `core-modules` and `hook-modules` that are verified and safe for use within the Story ecosystem. We encourage contributions and invite module developers to submit their modules for registration.

- **Core Modules** can be found [here](https://github.com/storyprotocol/protocol-core-v1/tree/main/contracts/modules).
- **Hook Modules** can be found [here](https://github.com/storyprotocol/protocol-periphery-v1/tree/main/contracts/hooks).

## Steps to Register Your Hook/Module

To get your hook/module verified and listed in this repository, please follow these steps:

1. **Develop your Hook**: You may fork [this template repository](https://github.com/storyprotocol/hook-dev-template) to bootstrap your development. It includes an example hook with tests against our Aeneid protocol, but using it is optional.

   👉 See [license-caller-whitelist-hook](https://github.com/jacob-tucker/license-caller-whitelist-hook) as an example that was used to develop the `LicenseCallerWhitelistHook.sol` hook.

2. **Fork this Repository**: Fork this `registered-modules` repository to your own GitHub account.

3. **Update the Module List**: Add your module's details to the appropriate JSON file according to module types in the repository. Make sure to **deploy & verify on block explorer** your hook on both aeneid and mainnet. Ensure that you adhere to the following JSON structure:

   ```json
   {
     "name": "YourModuleName",
     "aeneid": {
       "address": "YourModuleAddress",
       "blockExplorerLink": "YourModuleBlockExplorerLink"
     },
     "mainnet": {
       "address": "YourModuleAddress",
       "blockExplorerLink": "YourModuleBlockExplorerLink"
     }
   }
   ```

   Replace `YourModuleName`, `YourModuleAddress`, and `YourModuleBlockExplorerLink` with your module's name, its address, and the link to its block explorer page, respectively.

   Example:

   ```json
   {
     "name": "LicenseCallerWhitelistHook",
     "aeneid": {
       "address": "0x37be56d9fb06d885cda3cb010096c94c28b4d658",
       "blockExplorerLink": "https://aeneid.storyscan.io/address/0x37be56d9fb06d885cda3cb010096c94c28b4d658?tab=contract"
     },
     "mainnet": {
       "address": "0x6d9d51a444c8318e8840e75dab7ed81b5a714610",
       "blockExplorerLink": "https://www.storyscan.io/address/0x6d9d51a444c8318e8840e75dab7ed81b5a714610?tab=contract"
     }
   }
   ```

4. **Create a Pull Request (PR)**: Once you have added your module, create a pull request against this repository. In your PR's description, add the following information:

   ```md
   ## Register my module

   - Module type: `hook`
   - Module name: `LicenseCallerWhitelistHook`
   - Aeneid Module address: `0x37be56d9fb06d885cda3cb010096c94c28b4d658`
   - Mainnet Module address: `0x6d9d51a444c8318e8840e75dab7ed81b5a714610`
   - My module is immutable: yes
   - My module is using an upgradeable proxy: no
   - My module has been verified on the block explorer (required): yes
   - Summary of my module: Hook for allowing a licensor to gate which addresses can mint a license. The licensor can add/remove an address at any time.
   - GitHub repository with source code and tests: https://github.com/jacob-tucker/license-caller-whitelist-hook
   ```

5. **Await Verification**: After your PR is submitted, it will be reviewed. Once a security audit has been performed and completed, and the module whitelisted into the protocol, the PR will be merged. At this point your module will be officially registered and recognized as safe for use within the Story community.

We look forward to seeing your contributions and expanding the Story module ecosystem!
