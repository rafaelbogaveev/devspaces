# SLI Library Assembler Development with DF Devspaces

## Install DF Devspaces

1. Download and install devspaces client from this link https://devspaces.io/devspaces/download.

2. Here is some details about DF Devspaces https://devspaces.io/devspaces/help

Here follows the main commands used in Devspaces cli. 

|action   |Description                                                                                   |
|---------|----------------------------------------------------------------------------------------------|
|`devspaces --help`                    |Check the available command names.                               |
|`devspaces create [options]`          |Creates a DevSpace using your local DevSpaces configuration file |
|`devspaces start <devSpace>`          |Starts the DevSpace named \[devSpace\]                           |
|`devspaces bind <devSpace>`           |Syncs the DevSpace with the current directory                    |
|`devspaces info <devSpace> [options]` |Displays configuration info about the DevSpace.                  |

Use `devspaces --help` to know about updated commands.


### Start Devspaces 

It is assumed that terminal is opened in `devspaces` folder of the repository.

1.  Create DevSpaces.

```bash
devspaces create
```

2. Start your devspaces.
```bash
devspaces start assembler
```

3. Start devspace synchronization
Open terminal on folder you want to sync with devspaces and run:

```bash
cd ..
devspaces bind assembler
```
4. Grab some devspace info

```bash
devspaces info assembler
```

Retrieve published DNS, endpoints using this command and 

5. Connect to devspace

```bash
devspaces exec assembler
```

6. Make sure the source code is synced and install dependencies

```bash
npm install -g npm
npm install -g jspm
npm install -g gulp
npm install
jspm install

```

7. Run tests

```bash
gulp test
gulp cover
gulp e2e
```

8. Run the project
```bash
gulp watch
```

Open exposed url for port 9000 and 3001.