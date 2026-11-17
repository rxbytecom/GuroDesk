# Backup and recovery

## Create a backup

Sign in as Super Admin, open **Backup & Restore**, and choose **Choose location & back up**. Save the `.ssbackup` file to a protected folder or separate drive. Each file includes a consistent SQLite snapshot, format version, timestamp, and SHA-256 checksum. Attachments are in the database and included.

When enabled in Settings, automatic backups run at startup and every four hours while the application is running. They are stored in the local data directory's `backups` folder. There is no automatic rotation or off-computer replication; manage retention and copy important backups to another device.

Backups are not encrypted. They contain school records and password hashes. Store them with access restrictions. The checksum detects corruption, not an attacker who can replace both data and checksum.

## Restore

1. Sign in as Super Admin.
2. Open Restore, type `RESTORE`, and choose the backup file.
3. Confirm the native replacement prompt.
4. The app checks file format, checksum, SQLite integrity, foreign keys, migration version, table columns, unsupported triggers/views, and presence of an active administrator.
5. It creates a pre-restore backup and a rollback copy before replacing the database.
6. Sign in using an account contained in the restored backup.

The current database is not deleted before backup validation. Corrupt or mismatched-schema backups are rejected. If replacement fails, the rollback copy is restored. Restore expects the same application migration schema; an older-version backup should first be opened/migrated with the matching version in a separate test data directory.

## Emergency recovery

Keep the application closed while copying database files. The data directory may contain `.pre-migration-*.bak` and `.rollback-*` copies. Preserve these and the current database before attempting recovery. Do not overwrite the only recoverable copy. Test restores periodically on a separate installation/data directory.
