# Audit Report – Linux File Permissions

## Purpose
Ensure project files and directories follow the principle of least privilege.

## Summary of Changes
- Removed write permissions from 'others' on `project_k.txt`
- Secured `.project_x.txt` by removing write from user and group
- Restricted `drafts/` directory access to `researcher2`

## Risk Mitigated
Unauthorized data modification or leakage.
