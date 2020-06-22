# Terminus Quicksilver Plugin

[![Terminus v2.x Compatible](https://img.shields.io/badge/terminus-v2.x-green.svg)](https://github.com/pantheon-systems/terminus-quicksilver-plugin/tree/1.x)
[![Terminus v1.x Compatible](https://img.shields.io/badge/terminus-v1.x-green.svg)](https://github.com/pantheon-systems/terminus-quicksilver-plugin/tree/1.x)
[![Terminus v0.x Compatible](https://img.shields.io/badge/terminus-v0.x-green.svg)](https://github.com/pantheon-systems/terminus-quicksilver-plugin/tree/0.x)

Terminus Plugin that allows for installation of Quicksilver webhooks from the Quicksilver examples, or a personal collection, on [Pantheon](https://www.pantheon.io) sites.

Adds a command 'quicksilver' to Terminus which you can use to initialize a starting pantheon.yml file, or add a quicksilver web hook from the examples respository or a personal collection. For a version that works with Terminus 0.x, see the [0.x branch](https://github.com/pantheon-systems/terminus-secrets-plugin/tree/0.x).

Use as directed by Quicksilver examples.

## Configuration
This plugin will allow the user to quickly install Quicksilver webhooks pulled from either the Pantheon Quicksilver examples project, or from a personal collection of commonly-used webhooks.

To provide your own repository containing example webhooks that can be installed with the `terminus quicksilver install` command, set up a configuration file in your home directory, as shown below:
```
mkdir ~/.quicksilver
cp example-user-config.yml ~/.quicksilver/quicksilver.yml
```
See contents of this file for customization instructions.

## Examples

### Init pantheon.yml File
```
cd /path/to/local/pantheon/site
terminus quicksilver:init
```
Writes a simple pantheon.yml file to get you started with Quicksilver.

### Install a Quicksilver Webhook
```
cd /path/to/local/pantheon/site
terminus quicksilver:install debug
```
Installs one of the example projects from quicksilver-examples, and updates the site's pantheon.yml file.  Searches for a project whose name contains the provided string; in the example above, the debugging_example will be installed.

Once the sample has been installed, read its README file and customize the pantheon.yml file as needed.

### Install a Predefined Set of Quicksilver Webhooks
```
cd /path/to/local/pantheon/site
terminus quicksilver:profile development
```

## Installation
For help installing, see [Manage Plugins](https://pantheon.io/docs/terminus/plugins/)
```
mkdir -p ~/.terminus/plugins
composer create-project -d ~/.terminus/plugins pantheon-systems/terminus-quicksilver-plugin:~1
```

## Help

Run `terminus list quicksilver` for a complete list of available commands. Use `terminus help <command>` to get help on one command.
