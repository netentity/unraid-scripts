# Unraid Docker Scripts

Various bash scripts to be used in the User Scripts plugin in Unraid


## Appdata Backup Scripts

### backup_all_appdata

This script creates an individual tar file for each appdata directory found in your appdata path.  Furthermore, it stops and restarts each container before and after backup if the container was running at the time of the backup.

### backup_select_appdata

This script creates an invididual tar file for each appdata directory that you define (needs both container name and path to it's appdata).  Furthermore, it stops and restarts each container before and after backup if the container was running at the time of the backup.

### backup_plex_db

This script stops the plex container and copies the main plex db file to a backup location of your choosing before restarting the container.


## Usage

Create a new User script and paste script text in

### Example Cron Schedules

Cron schedule to run script every morning at 5:00am

```bash
0 5 * * *
```

Cron schedule to run script Monday morning at 5:00am

```bash
0 5 * * 1
```

Cron schedule to run script morning at 5:00am except Monday

```bash
0 5 * * 0,2-6
```
