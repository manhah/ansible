# ansible
Some examples showing the use of Ansible.

Requirements for all demos:
- Ansible installed on calling machine
- Python installed on remote machine (not needed in case of localhost of course)

Note:
- For debugging, use `-vvv` for verbose mode and nicely printed debug messages

## merging_files
Two demos on how to merge files inside a desired directory.

### merge_all_files.yml
Merges all files inside a given directory recursively based on a given file pattern. The command to execute on the found files can be specified by use of parameters.

Usage:
- Modify parameters inside the file (vars) as desired
- Run against localhost by: `ansible-playbook merge_all_files.yml`

## merge_m2ts_files_by_stream_folder.yml
In a given directory, it loops through all subdirectories and merges all m2ts files inside the subdirectories' STREAM folder into one single MKV file that is placed on the same level than the subdirectory.

Requirement:
- mkvmerge needs to be installed on the remote machine

Usage:
- Modify search path inside the file (vars) as desired
- Run against localhost by: `ansible-playbook merge_m2ts_files_by_stream_folder.yml`
