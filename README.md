# not-sync-cli

Disable synchronization for some files in cloud storage such as Dropbox, iCloudDrive or OneDrive. Detects cloud storage provider.

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->

- [Synopsis](#synopsis)
- [Details](#details)
  - [not-sync](#not-sync)
  - [resync](#resync)
- [Related](#related)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

# Synopsis

Disable synchronization for `node_modules`, `dist`, `coverage`.

```sh
$ not-sync node_modules dist coverage
```

Re-enable synchronization for `node_modules`, `dist`, `coverage`.

```sh
$ resync node_modules dist coverage
```

# Details

Please see [not-sync](https://github.com/ozum/not-sync) for details.

## not-sync

```sh
       USAGE

  $ not-sync [options] <path>...

     ARGUMENTS

  <path>... Path or list of paths (separate with space) to disable syncronization for.

      OPTIONS

     --cwd                           Set current working directory for relative paths.
  -i --ignoreConfigs                 (CSV) List of ignore files to update (e.g. .gitignore, .prettierignore).
     --dry                           Prevent changes to be written to disk. Executes a dry run.
  -v --verbose                       Output extra information.
  -l --linkSameDir   (Default: true) Move files near original file for iCloudDrive. For example 'dist' is moved 'dist.nosync' in same directory.
     --help                          Show help.
     --version                       Show version.

      EXAMPLES

  $ not-sync --i .gitignore node_modules dist coverage
```

## resync

```sh
       USAGE

  $ resync [options] <path>...

     ARGUMENTS

  <path>... Path or list of paths (separate with space) to re-enable syncronization for.

      OPTIONS

     --cwd            Set current working directory for relative paths.
  -i --ignoreConfigs  (CSV) List of ignore files to update (e.g. .gitignore, .prettierignore).
     --dry            Prevent changes to be written to disk. Executes a dry run.
  -v --verbose        Output extra information.
     --help           Show help.
     --version        Show version.

      EXAMPLES

  $ resync --i .gitignore node_modules dist coverage
```

# Related

[not-sync](https://github.com/ozum/not-sync): API for this CLI.

<!-- usage -->

<!-- commands -->
