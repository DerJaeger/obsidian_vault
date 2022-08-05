# Users
0 root
1001 warp
1010 nico
1011 lennart
1012 silva
1013 tina
# Groups
1000 family
1001 admin
1002 nico
1003 server

# Commands
src: https://docs.fedoraproject.org/en-US/fedora/latest/system-administrators-guide/basic-system-configuration/Managing_Users_and_Groups/
```Shell
groupadd -g 1003 server
```

``` Shell
useradd -d <home_directory> -g <group_name> -G <group_list>
```

| command example | Description |
| -------------------- | --- |
| `-c` '_comment_' | _comment_ can be replaced with any string. This option is generally used to specify the full name of a user. |
| `-d` _home_directory_ | Home directory to be used instead of default `/home/_username_/`. |
| `-e` _date_ | Date for the account to be disabled in the format YYYY-MM-DD. |
| `-f` _days_ | Number of days after the password expires until the account is disabled. If `0` is specified, the account is disabled immediately after the password expires. If `-1` is specified, the account is not disabled after the password expires. |
| `-g` _group_name_ | Group name or group number for the user’s default (primary) group. The group must exist prior to being specified here. |
| `-G` _group_list_ | List of additional (supplementary, other than default) group names or group numbers, separated by commas, of which the user is a member. The groups must exist prior to being specified here. |
| `-m` | Create the home directory if it does not exist. |
| `-M` | Do not create the home directory. |
| `-N` | Do not create a user private group for the user. |
| `-p` _password_ | The password encrypted with crypt. |
| `-r` | Create a system account with a UID less than 1000 and without a home directory. |
| `-s` | User’s login shell, which defaults to /bin/bash. |
| `-u` _uid_ | User ID for the user, which must be unique and greater than 999. |


