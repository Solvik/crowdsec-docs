---
id: cscli_appsec-configs_remove
title: cscli appsec-configs remove
---
## cscli appsec-configs remove

Remove given appsec-config(s)

### Synopsis

Remove one or more appsec-configs

```
cscli appsec-configs remove [item]... [flags]
```

### Examples

```
# Uninstall some appsec-configs.
cscli appsec-configs remove crowdsecurity/virtual-patching

# Show the execution plan without changing anything - compact output sorted by type and name.
cscli appsec-configs remove crowdsecurity/virtual-patching --dry-run

# Show the execution plan without changing anything - verbose output sorted by execution order.
cscli appsec-configs remove crowdsecurity/virtual-patching --dry-run -o raw

# Uninstall and also remove the downloaded files.
cscli appsec-configs remove crowdsecurity/virtual-patching --purge

# Remove tainted items.
cscli appsec-configs remove crowdsecurity/virtual-patching --force

# Prompt for confirmation if running in an interactive terminal; otherwise, the option is ignored.
cscli appsec-configs remove crowdsecurity/virtual-patching -i
cscli appsec-configs remove crowdsecurity/virtual-patching --interactive
```

### Options

```
      --all           Remove all the appsec-configs
      --dry-run       Don't install or remove anything; print the execution plan
      --force         Force remove: remove tainted and outdated files
  -h, --help          help for remove
  -i, --interactive   Ask for confirmation before proceeding
      --purge         Delete source file too
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

* [cscli appsec-configs](/cscli/cscli_appsec-configs.md)	 - Manage hub appsec-configs

