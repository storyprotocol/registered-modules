# Story Registered Modules

Welcome to the repository for Story's registered modules. This repository serves as a comprehensive list of both `core-modules` and `hook-modules` that are verified and safe for use within the Story ecosystem. We encourage contributions and invite module developers to submit their modules for registration.

- **Core Modules** can be found [here](https://github.com/storyprotocol/protocol-core-v1/tree/main/contracts/modules).
- **Hook Modules** can be found [here](https://github.com/storyprotocol/protocol-periphery-v1/tree/main/contracts/hooks).

## Steps to Register Your Module

To get your module verified and listed in this repository, please follow these steps:

1. **Fork this Repository**: Begin by forking this repository to your own GitHub account.

2. **Update the Module List**: Add your module's details to the appropriate JSON file according to module types in the repository. Ensure that you adhere to the following JSON structure:

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
     "name": "TotalLicenseTokenLimitHook",
     "aeneid": {
       "address": "0xaBAD364Bfa41230272b08f171E0Ca939bD600478",
       "blockExplorerLink": "https://aeneid.storyscan.io/address/0xaBAD364Bfa41230272b08f171E0Ca939bD600478?tab=contract"
     },
     "mainnet": {
       "address": "0xB72C9812114a0Fc74D49e01385bd266A75960Cda",
       "blockExplorerLink": "https://www.storyscan.io/address/0xB72C9812114a0Fc74D49e01385bd266A75960Cda?tab=contract"
     }
   }
   ```

3. **Create a Pull Request (PR)**: Once you have added your module, create a pull request against this repository. Utilize the provided PR template to ensure all necessary information is included.

4. **Await Verification**: After your PR is submitted, it will be reviewed. Once a security audit has been performed and completed, and the module whitelisted into the protocol, the PR will be merged. At this point your module will be officially registered and recognized as safe for use within the Story community.

We look forward to seeing your contributions and expanding the Story module ecosystem!
