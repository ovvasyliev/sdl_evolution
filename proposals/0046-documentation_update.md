# Continious Integration documentation update

* Proposal: [SDL-0046](0046-ci_documentation_update.md)
* Author: [Alexander Vasilyev](https://github.com/ovvasyliev)
* Status: **Awaiting review**
* Impacted Platforms: [CI]

## Introduction

Software development requiers fast and bugs free code creation. It can be achived only by using some kind of Continious Integration system which guarantee the same workflow and build environment for every build from every developer. It gets even more valuable in open source projects - every contributor must be sure his commit will not broke entire product. OpenSDL project using Continious Integration system based on Jenkins. CI allows to execute builds in fast and simultaneous environment. And to perform all required checks on every pull request, commit to a branch, etc, provide clear and visible status reports. 
Each system should be supported and keeping in working condition. To make support proccess easier - documentation should be created.

## Motivation

Most common problem for complicated systems is missconfiguration in case of disaster recovery process. Also major problem is lost knowledge - if system working fine for descent amount of time, maintainer can lost some specific steps of it's configuration. Full and comprehencive documentation solves these problems. As well as CI maintainer change problem. All knowledge stored in one place and everyone can setup own and/or maintain existing system.

## Proposed solution

Create full and comprehencive documentation for existing CI system. Table of content can be found below.

CI Purpose
Glossary
CI Installation
	Environment preparation
	Jenkins setup and run
	Support conteiners starting
	Jenkins required plugins listing
	Jenkins global variables and plugins setup
	Jenkins jobs setup
		Generic branch builds structure
		Generic OpenSDL job
		Generic ATF job
		On demand jobs
		Support scripts list
	CI backup&restore procedure
	Jenkins version upgrade procedure
CI generic workflow
Tools
	Unit Tests
	ATF
Build Artifacts
	OpenSDL binaries
	Junit reports
	ATF HTML report
	Job logs
	Error logs
	OpenSDL logs
	ATF Logs
	Static code analysis report
	Coverage reports
	Jobs Description
	Jobs Listing
	CI Jobs details
User Scenarios
	New job request

## Potential downsides

No major downsides for this activity. Except of one - this documentation will be platform dependent for some steps. And this piont should be taken in consideration if similar system should be required to be deployed somwhere else.

## Impact on existing code

No impact for existing code.

## Alternatives considered

As alternate approach - some of cloud CI system can be used (i.e. TravisCI). But this is not valid approach due to lack of configuration options and low flexibility of this systems.  

