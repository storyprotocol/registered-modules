# StoryProtocol Registered Modules

Welcome to the repository for StoryProtocol's registered modules. This repository serves as a comprehensive list of both `default modules` and `hook modules` that are verified and safe for use within the StoryProtocol ecosystem. We encourage contributions and invite module developers to submit their modules for registration.

## Steps to Register Your Module

To get your module verified and listed in this repository, please follow these steps:

1. **Fork this Repository**: Begin by forking this repository to your own GitHub account.

2. **Update the Module List**: Add your module's details to the appropriate JSON file according to module types in the repository. Ensure that you adhere to the following JSON structure:

   ```json
   {
     "name": "YourModuleName",
     "address": "YourModuleAddress",
     "blockExplorerLink": "YourModuleBlockExplorerLink"
   }
   ```
   Replace `YourModuleName`, `YourModuleAddress`, and `YourModuleBlockExplorerLink` with your module's name, its address, and the link to its block explorer page, respectively.

   Example:
   ```json
   {
     "name": "SimpleDefaultModule",
     "address": "0x01469702E71F5C8199A15a97e8147D002C60a0B9",
     "blockExplorerLink": "https://sepolia.etherscan.io/address/0x01469702E71F5C8199A15a97e8147D002C60a0B9#code"
   }
   ```

3. **Create a Pull Request (PR)**: Once you have added your module, create a pull request against this repository. Utilize the provided PR template to ensure all necessary information is included.

4. **Await Verification**: After your PR is submitted, it will be reviewed. Upon approval and merging of your PR, your module will be officially registered and recognized as safe for use within the StoryProtocol community.

We look forward to seeing your contributions and expanding the StoryProtocol module ecosystem!
