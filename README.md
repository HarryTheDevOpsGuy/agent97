

### Getting Start with Agent97.
```bash
# Download Agent97
curl -sL https://github.com/HarryTheDevOpsGuy/agent97/raw/master/x86_64/agent97 -o /usr/bin/agent97
chmod +x /usr/bin/agent97

# To check version
agent97 -v

# To view help page
agent97 -h

# To run Agent97
agent97 -r
```

#### Default Init Config to load arguments.

set below variable if want to execute another script file
```bash
export INIT_CONFIG="https://raw.githubusercontent.com/harry41/test/main/LinuxScript.sh"

agent97 -r
```

#### Input variables and configs.

When above script will run this variable file will load in the system.

https://raw.githubusercontent.com/harry41/test/main/LinuxScript.sh


#### Required Agent remote Variables
```bash
#!/bin/bash

#INIT_ENVARS+="https://raw.githubusercontent.com/harry41/test/main/LinuxScript.sh|123hello45|3|e"
INIT_VARS+=("https://raw.githubusercontent.com/harry41/test/main/scripts/init-vars.sh")

CENTOS_PKGS+=(jq nginx)
UBUNTU_PKGS+=(jq nginx)

#CURL_PKGS+=( 'https://github.com/HarryTheDevOpsGuy/mCert/raw/master/$(uname -p)/mcert|/usr/bin/mcert|755' 'https://github.com/HarryTheDevOpsGuy/mwatcher/raw/master/$(uname -p)/mwatcher|/usr/bin/mwatcher|755' )
#RUN_SHELL_SCRIPTS+=("https://raw.githubusercontent.com/harry41/test/main/ShellScript.sh" "https://raw.githubusercontent.com/harry41/test/main/ShellScript2.sh")
RUN_SHELL_SCRIPTS+=(https://raw.githubusercontent.com/harry41/test/main/scripts/RunScript.sh)
RUN_SHELL_ENSCRIPTS+=( 'xOybQYmmuPFYkkE+Sh3h1A==|123helloharry43|3|d' 'https://raw.githubusercontent.com/harry41/test/main/scripts/EncShell.sh|GYgoUJkrjzFtl8LyJ9oRu|5|d' )

MYARRAY=(file file2 file3)


curl -L "https://github.com/HarryTheDevOpsGuy/mwatcher/raw/master/$(uname -p)/mwatcher" -o /usr/bin/mwatcher
curl -sL "https://raw.githubusercontent.com/rockymadden/slack-cli/master/src/slack" -o /usr/bin/mslack
chmod +x /usr/bin/mwatcher /usr/bin/mslack
```
