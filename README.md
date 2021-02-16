# yask for Sitecore
**a sitecore docker starterkit** - _yet-another-starterkit_

This starter-kit generates a preconfigured local docker environment based on selected Sitecore topology and module.

It uses a "layering" technique to build up a folder structure by following a similar concept to how Docker images are commonly built.

**This is work-in-progress**  
_a ton of clean-up and refactoring is coming._

The concept and initial commit originate from a quick boilerplate made for the Sitecore Hackathon participants to use in the Sitecore 2021 Hackathon. 

A goal now is to extract a clean Powershell module that fetch files from a separate repo. Solution and msbuild setup will be removed from the starter-kit so it is only used to generate the docker environment files based on the selected Sitecore topology, variant and optional modules.


## Basic concept

The sitecore topology is selected through a fancy colorful console that builds up a string similar, but not identical, to sitecore image tags.

F. ex. sitecore-xp0-jss

This will copy in the folders in the given order
- sitecore
- sitecore-xp0
- sitecore-xp0-jss

sitecore being the base setup. Each higher level folder only contain the delta between the desired topology/variant and the base.

After the folders has been merged into a new .\docker folder the fancy console ui prompts for all required environment values that is then stored in .env 

When the wizard is done, the docker environment is ready to spin up with no further changes needed. Deployment from Visual Studio to shared volume folders etc. can be bootstrapped from other templates, such as [VS Helix templates extension](https://github.com/LaubPlusCo/Helix-Templates) or other.


_Final note; this starter-kit may or may not evolve any further. Please help by contributing if you like the concept_ 

# Some credits and references

- [Original Hackathon boilerplate repo](https://github.com/Sitecore-Hackathon/Boilerplate/tree/feature/2021)
- [Sitecore Community docker images](https://github.com/Sitecore/docker-images)
- [Sitecore Docker tools](https://github.com/Sitecore/docker-tools)
- Some inspiration [Konabos docker-examples](https://github.com/konabos/docker-examples)
