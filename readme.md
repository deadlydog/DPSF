# DPSF (Dynamic Particle System Framework)

This repository is for DPSF v3, which aims to be a graphics engine agnostic library that will allow DPSF to be used across many more development technologies than [the XNA-dependent DPSF v1 and v2][DpsfXnaRepository].

DPSF is open source and pull requests are welcomed!

## Hopes and thoughts for DPSF v3

* The old repository was very bloated, so we created this new one. We can still make reference to the original repo though so people know where to look if they want to see past history. Ideally DPSF v3 will be able to run all of the same code / particle systems as v2, although the classes may need to be modified a bit first.
* Remove DPSF's dependency on XNA.
  * Have the root DPSF assembly not have any graphics dependency. Essentially, only capable of doing NoDisplay particle systems. This is desirable because DPSF can be used for much more than just particle systems (should maybe consider a name change.....any suggestions?), such as an easy way to add scripting or simple AI to an app.
  * Have a separate project for each game engine to support (e.g. MonoGame) that implements the graphics dependent code. If somebody were using this for a video game, this is the nuget package they would import into their project and build off of.
  * Demos and Tutorials can be moved to a new repository perhaps? Or maybe just a separate directory with their own solution files.
* Get rid of the installer and distribute code solely through NuGet packages. This will remove much of the work around releasing new versions.
* Probably get rid of the .chm help file. Would be nice to just convert it into markdown and have it in the GitHub wiki as it's own repository. So just have online help, no offline help. Again this will reduce the amount of work needed to publish a new version.

[DpsfXnaRepository]: https://github.com/deadlydog/DPSF-XNA