# Daily Backup and Backup Restore
This project consists of two Bash scripts that allow for a daily backup of a directory and to recover a backup if necessary.

## Installation
To install the project, you must first clone the repository, and then install the dependencies. To do this, you must execute the following commands:
```bash
git clone https://github.com/AG-9571/daily-backup.git
cd daily-backup
```

## Usage
Before using the scripts, you must give them execution permissions. To do this, run the following command in the terminal
```bash
chmod +x daily-backup.sh backup-restore.sh
```
### dailyBackup.sh
This script performs a daily backup of a specified directory and saves it in a compressed tar.gz format file in a backups directory.

To use it, run the following command in the terminal:
```bash
daily-backup.sh
```
The script will ask you for the directory to be backed up, and the directory where the backups will be saved. If the directory does not exist, it will be created.

#### Cron service
To automate the backup process, you can use the cron service. To do this, you must execute the following command in the terminal:
```bash
crontab -e
```
This will open the cron configuration file. You must add the following line to the end of the file:
```bash
0 12 * * * ./daily-backup.sh
```

### backupRestore.sh
This script allows restoring a backup of a specified directory.
```bash
backup-restore.sh <aaaammdd> ./
```
The first parameter is the date of the backup to be restored, and the second parameter is the directory where the backup will be restored.

## Contributing
To contribute to the project, you must first fork the repository, and then clone it. To do this, you must execute the following commands:
```bash
git clone https://github.com/AG-9571/daily-backup.git
cd daily-backup
```
Push your changes to your fork, and then create a pull request.
```bash
git add .
git commit -m "<message>"
git remote add origin https://github.com/AG-9571/daily-backup.git
git push origin <branch>
```
## Credits
The project has been developed by the following people:

* [Ángel Ortega](https://github.com/AG-9571)

## Licencia

This project is under the MIT License. See the LICENSE file for more details.