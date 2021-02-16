# yask for Sitecore
## a sitecore docker starterkit
yet-another-starterkit (yask) for Sitecore 

This starter-kit generates a preconfigured local docker environment based on selected Sitecore topology and module.

It uses a "layering" technique to build up a folder structure by following a similar concept to how Docker images are commonly built.

** This is work-in-progress **
_tons of refactoring is coming_

The concept and initial commit originate from a quick boilerplate made for the Sitecore Hackathon participants to use in the Sitecore 2021 Hackathon. 

A goal now is to extract a clean Powershell module that fetch files from a separate repo. Solution and msbuild setup will be removed from the starter-kit so it is only used to generate the docker environment files based on the selected Sitecore topology, variant and optional modules.

The sitecore topology is selected through a fancy colorful console which results in a string similar but not identical to sitecore image tags.

F. ex. sitecore-xp0-jss

This will copy in the folders in the given order
> sitecore
> sitecore-xp0
> sitecore-xp0-jss

sitecore being the base setup. Each higher level folder only contain the delta between the desired topology/variant and the base.


Do note that this starter-kit may or may not evolve any further. 

# Some credits and references

- [Original Hackathon boilerplate repo]()
- [Sitecore Community docker images](https://github.com/Sitecore/docker-images)
- [Sitecore Docker tools](https://github.com/Sitecore/docker-tools)
- Inspiration and few concepts from [Konabos docker-examples](https://github.com/konabos/docker-examples)
