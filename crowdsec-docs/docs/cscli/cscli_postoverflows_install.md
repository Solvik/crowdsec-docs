---
id: cscli_postoverflows_install
title: cscli postoverflows install
---
## cscli postoverflows install

Install given postoverflow(s)

### Synopsis

Fetch and install one or more postoverflows from the hub

```
cscli postoverflows install [item]... [flags]
```

### Examples

```
# Install some postoverflows.
cscli postoverflows install crowdsecurity/cdn-whitelist crowdsecurity/rdns

# Show the execution plan without changing anything - compact output sorted by type and name.
cscli postoverflows install crowdsecurity/cdn-whitelist crowdsecurity/rdns --dry-run

# Show the execution plan without changing anything - verbose output sorted by execution order.
cscli postoverflows install crowdsecurity/cdn-whitelist crowdsecurity/rdns --dry-run -o raw

# Download only, to be installed later.
cscli postoverflows install crowdsecurity/cdn-whitelist crowdsecurity/rdns --download-only

# Install over tainted items. Can be used to restore or repair after local modifications or missing dependencies.
cscli postoverflows install crowdsecurity/cdn-whitelist crowdsecurity/rdns --force

# Prompt for confirmation if running in an interactive terminal; otherwise, the option is ignored.
cscli postoverflows install crowdsecurity/cdn-whitelist crowdsecurity/rdns -i
cscli postoverflows install crowdsecurity/cdn-whitelist crowdsecurity/rdns --interactive
```

### Options

```
  -d, --download-only   Only download packages, don't enable
      --dry-run         Don't install or remove anything; print the execution plan
      --force           Force install: overwrite tainted and outdated files
  -h, --help            help for install
      --ignore          Ignore errors when installing multiple postoverflows
  -i, --interactive     Ask for confirmation before proceeding
```

### Options inherited from parent commands

```
      --color string    Output color: yes, no, auto (default "auto")
  -c, --config string   path to crowdsec config file (default "/etc/crowdsec/config.yaml")
      --debug           Set logging to debug
      --error           Set logging to error
      --info            Set logging to info
  -o, --output string   Output format: human, json, raw
      --trace           Set logging to trace
      --warning         Set logging to warning
```

### SEE ALSO

* [cscli postoverflows](/cscli/cscli_postoverflows.md)	 - Manage hub postoverflows

