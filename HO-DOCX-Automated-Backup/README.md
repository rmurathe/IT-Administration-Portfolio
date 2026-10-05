Automated Network File Backup System
Project Overview

This project documents the implementation of an automated Windows-based backup solution for business documents stored on a network computer.

The solution uses Robocopy and Windows Task Scheduler to automatically copy important company documents to a separate backup drive and maintain a backup log for verification.

Objectives
Automate regular backup of business documents
Protect important company files against accidental loss
Maintain a separate backup copy
Reduce the need for manual backups
Maintain backup logs for monitoring and verification
Provide a simple and reliable backup process
Environment

Source computer: Front Office computer
Source folder:

\\FRONTOFFICE2\HO DOCX

Backup destination:

G:\HO DOCX Backup

Operating system: Windows

Backup technology:

Robocopy
Windows Task Scheduler
PowerShell
Backup Schedule

The backup task is configured to run automatically:

Schedule: Monday
Start time: 10:00 AM

The task can be monitored through Windows Task Scheduler and the Robocopy backup log.

Robocopy Configuration

The backup process uses Robocopy with options including:

/E
/Z
/FFT
/R:3
/W:5
/COPY:DAT
/DCOPY:T
/LOG+
/NP
Purpose of the options
Option	Purpose
/E	Copies subdirectories, including empty directories
/Z	Uses restartable mode
/FFT	Uses FAT file-time compatibility
/R:3	Retries failed copies three times
/W:5	Waits five seconds between retries
/COPY:DAT	Copies data, attributes and timestamps
/DCOPY:T	Preserves directory timestamps
/LOG+	Appends results to the backup log
/NP	Does not display progress percentage
Verification

Backup results are verified using the Robocopy log and Windows Task Scheduler.

Example verification commands:

Get-ScheduledTaskInfo -TaskName "HO DOCX Daily Backup"

and:

Get-Content "G:\HO DOCX Backup\backup.log" -Tail 25
Verified Backup — 5 October 2026

The backup was successfully executed on 5 October 2026.

Backup statistics
Metric	Result
Start time	10:00 AM
End time	10:04:19 AM
Directories processed	2,221
Files processed	34,232
Files copied	144
Data copied	749.72 MB
Failed directories	0
Failed files	0
Mismatches	0
Extras detected	17

The Robocopy report showed 0 failed files and 0 failed directories, confirming that the backup completed successfully.

Skills Demonstrated

This project demonstrates practical experience with:

Windows administration
Network file sharing
Robocopy
PowerShell
Windows Task Scheduler
Automated backups
Backup verification
Log monitoring
Data protection
Basic disaster recovery
IT documentation
Lessons Learned

The project demonstrates that an effective backup system should not only copy files automatically but should also provide a way to verify that the backup completed successfully.

Monitoring the Task Scheduler result together with the Robocopy log provides two useful methods of confirming backup status.

Future Improvements

Possible improvements include:

Automated backup-status notifications
Multiple backup destinations
Off-site/cloud backup
Backup retention policies
Automated integrity checks
Backup monitoring dashboard
Disaster-recovery testing
Author

Reginald Murathe

IT Support | Systems Administration | Network Administration | IT Infrastructure

Kenya
