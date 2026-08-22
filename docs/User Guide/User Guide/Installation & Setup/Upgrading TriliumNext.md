# Upgrading Notely
This document outlines the steps required to upgrade Notely to a new release version.

## How to Upgrade

Notely does not support built-in automatic upgrades; all updates must be performed manually. The upgrade process varies depending on the installation method:

*   [**Docker Server Installation**](Server%20Installation/1.%20Installing%20the%20server/Using%20Docker.md): Pull the new image and restart the container.
*   **Other Installations**: Download the latest version from the [release page](https://github.com/TriliumNext/Trilium/releases/latest) and replace the existing application files.

## Database Compatibility and Migration

Upon startup, Notely will automatically migrate the [database](../Advanced%20Usage/Database.md) to the new version. Note that after migration, older versions of Notely will be unable to read the database. If you need to revert to a previous version of Notely and its database, you can restore the [backup](Backup.md) that is created prior to migration.

## Sync Compatibility

The [synchronization](Synchronization.md) protocol used by Notely is versioned, requiring all members of the sync cluster to use the same protocol version. Therefore, when upgrading to a new version, you may need to upgrade all instances in the sync cluster. Changes to the sync protocol version are typically indicated on the release page.