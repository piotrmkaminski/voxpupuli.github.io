---
layout: post
title: Announcing puppet-openvoxdb
date: 2026-03-25
github_username: d1nuc0m
--- 

Today we launched [puppet/openvoxdb](https://forge.puppet.com/modules/puppet/openvoxdb/readme), a Puppet module to install OpenVoxDB!

## What is OpenVoxDB?

OpenVoxDB is the OpenVox fork of [PuppetDB](https://github.com/puppetlabs/puppetdb).
It collects OpenVox agent run reports, that can then be queried using [PQL (Puppet Query Language)](https://help.puppet.com/pdb/current/topics/pql.htm).

Collected data can also be visualized in a web dashboard like [Puppetboard](https://github.com/voxpupuli/puppetboard) or [OpenVox Gui](https://github.com/voxpupuli/openvoxview). There also are web dashboards outside of VoxPupuli, like [OpenVox Gui](https://github.com/cvquesty/openvox-gui) and [Pabawi](https://github.com/example42/pabawi).

## What is puppet-openvoxdb?

It is a fork of [puppetlabs/puppetdb](https://forge.puppet.com/modules/puppetlabs/puppetdb) adapted for OpenVoxDB: the main changes are the installed packages and parameters type validation.
If you want to try OpenVoxDB or where already using PuppetDB and want to migrate - this module is for you.
It automates OpenVoxDB install, PostgreSQL setup and OpenVox Server configuration so that clients interact with OpenVoxDB.

### Migration from PuppetDB and/or puppetlabs-openvoxdb

In a test environment you can just rename the classes from puppetdb to openvoxdb, type check the parameters, add the VoxPupuli repositories and it should work.
However in production environments you are advised to migrate manually - and don't forget a backup.

### Caveats

* EL10 is not supported yet, due to lack of support in `puppetlabs/postgresql`
* Migration from PuppetDB < 8.x is not supported yet.
  You should migrate first to PuppetDB < 8.x to PuppetDB 8.x, and from there to OpenVoxDB 8.x

## Contribute

There is still a lot of work to do for cleanup and optimization - you can find [voxpupuli/puppet-openvoxdb on GitHub](https://github.com/voxpupuli/puppet-openvoxdb/).
Issues and PRs are welcome!