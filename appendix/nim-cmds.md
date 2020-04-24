# Commands
* [`nim action:create ACTIONNAME [ACTIONPATH]`](#nim-actioncreate-actionname-actionpath)
* [`nim action:delete ACTIONNAME`](#nim-actiondelete-actionname)
* [`nim action:get ACTIONNAME`](#nim-actionget-actionname)
* [`nim action:invoke ACTIONNAME`](#nim-actioninvoke-actionname)
* [`nim action:list [PACKAGE]`](#nim-actionlist-package)
* [`nim action:update ACTIONNAME [ACTIONPATH]`](#nim-actionupdate-actionname-actionpath)
* [`nim activation:get [ACTIVATIONID]`](#nim-activationget-activationid)
* [`nim activation:list [ACTIVATIONID]`](#nim-activationlist-activationid)
* [`nim activation:logs [ACTIVATIONID]`](#nim-activationlogs-activationid)
* [`nim activation:result [ACTIVATIONID]`](#nim-activationresult-activationid)
* [`nim auth:current`](#nim-authcurrent)
* [`nim auth:github`](#nim-authgithub)
* [`nim auth:list`](#nim-authlist)
* [`nim auth:login [TOKEN]`](#nim-authlogin-token)
* [`nim auth:logout NAMESPACE`](#nim-authlogout-namespace)
* [`nim auth:switch NAMESPACE`](#nim-authswitch-namespace)
* [`nim autocomplete [SHELL]`](#nim-autocomplete-shell)
* [`nim doc`](#nim-doc)
* [`nim help [COMMAND]`](#nim-help-command)
* [`nim info`](#nim-info)
* [`nim key-value:del [NAMESPACE]`](#nim-key-valuedel-namespace)
* [`nim key-value:flush [NAMESPACE]`](#nim-key-valueflush-namespace)
* [`nim key-value:get [NAMESPACE]`](#nim-key-valueget-namespace)
* [`nim key-value:getMany [NAMESPACE]`](#nim-key-valuegetmany-namespace)
* [`nim key-value:list [NAMESPACE]`](#nim-key-valuelist-namespace)
* [`nim key-value:llen [NAMESPACE]`](#nim-key-valuellen-namespace)
* [`nim key-value:lrange [NAMESPACE]`](#nim-key-valuelrange-namespace)
* [`nim key-value:rpush [NAMESPACE]`](#nim-key-valuerpush-namespace)
* [`nim key-value:set [NAMESPACE]`](#nim-key-valueset-namespace)
* [`nim key-value:setMany [NAMESPACE]`](#nim-key-valuesetmany-namespace)
* [`nim namespace:clean [NAMESPACE]`](#nim-namespaceclean-namespace)
* [`nim namespace:get`](#nim-namespaceget)
* [`nim objects:list [NAMESPACE]`](#nim-objectslist-namespace)
* [`nim package:bind PACKAGENAME BINDPACKAGENAME`](#nim-packagebind-packagename-bindpackagename)
* [`nim package:create PACKAGENAME`](#nim-packagecreate-packagename)
* [`nim package:delete PACKAGENAME`](#nim-packagedelete-packagename)
* [`nim package:get PACKAGENAME`](#nim-packageget-packagename)
* [`nim package:list [NAMESPACE]`](#nim-packagelist-namespace)
* [`nim package:update PACKAGENAME`](#nim-packageupdate-packagename)
* [`nim project:create [PROJECT]`](#nim-projectcreate-project)
* [`nim project:deploy [PROJECTS]`](#nim-projectdeploy-projects)
* [`nim project:watch [PROJECTS]`](#nim-projectwatch-projects)
* [`nim route:create BASEPATH RELPATH APIVERB ACTION`](#nim-routecreate-basepath-relpath-apiverb-action)
* [`nim route:delete BASEPATHORAPINAME [RELPATH] [APIVERB]`](#nim-routedelete-basepathorapiname-relpath-apiverb)
* [`nim route:get BASEPATHORAPINAME`](#nim-routeget-basepathorapiname)
* [`nim route:list [BASEPATH] [RELPATH] [APIVERB]`](#nim-routelist-basepath-relpath-apiverb)
* [`nim rule:create NAME TRIGGER ACTION`](#nim-rulecreate-name-trigger-action)
* [`nim rule:delete NAME`](#nim-ruledelete-name)
* [`nim rule:disable NAME`](#nim-ruledisable-name)
* [`nim rule:enable NAME`](#nim-ruleenable-name)
* [`nim rule:get NAME`](#nim-ruleget-name)
* [`nim rule:list`](#nim-rulelist)
* [`nim rule:status NAME`](#nim-rulestatus-name)
* [`nim rule:update NAME TRIGGER ACTION`](#nim-ruleupdate-name-trigger-action)
* [`nim trigger:create TRIGGERNAME`](#nim-triggercreate-triggername)
* [`nim trigger:delete TRIGGERPATH`](#nim-triggerdelete-triggerpath)
* [`nim trigger:fire TRIGGERNAME`](#nim-triggerfire-triggername)
* [`nim trigger:get TRIGGERPATH`](#nim-triggerget-triggerpath)
* [`nim trigger:list`](#nim-triggerlist)
* [`nim trigger:update TRIGGERNAME`](#nim-triggerupdate-triggername)
* [`nim update [CHANNEL]`](#nim-update-channel)
* [`nim web:list [NAMESPACE]`](#nim-weblist-namespace)

## `nim action:create ACTIONNAME [ACTIONPATH]`

Creates an Action

```
USAGE
  $ nim action:create ACTIONNAME [ACTIONPATH]

OPTIONS
  -A, --annotation-file=annotation-file  FILE containing annotation values in JSON format
  -E, --env-file=env-file                FILE containing environment variables in JSON format
  -P, --param-file=param-file            FILE containing parameter values in JSON format
  -a, --annotation=annotation            annotation values in KEY VALUE format
  -e, --env=env                          environment values in KEY VALUE format
  -i, --insecure                         bypass certificate check
  -l, --logsize=logsize                  the maximum log size LIMIT in MB for the action (default 10)
  -m, --memory=memory                    the maximum memory LIMIT in MB for the action (default 256)
  -p, --param=param                      parameter values in KEY VALUE format
  -t, --timeout=timeout                  the timeout LIMIT in milliseconds after which the action is terminated (default 60000)
  -u, --auth=auth                        whisk auth
  -v, --verbose                          Verbose output
  --apihost=apihost                      whisk API host
  --apiversion=apiversion                whisk API version
  --binary                               treat code artifact as binary
  --cert=cert                            client cert
  --debug=debug                          Debug level output
  --docker=docker                        use provided Docker image (a path on DockerHub) to run the action
  --help                                 Show help
  --json                                 output raw json
  --key=key                              client key
  --kind=kind                            the KIND of the action runtime (example: swift:default, nodejs:default)
  --main=main                            the name of the action entry point (function or fully-qualified method name when applicable)
  --sequence=sequence                    treat ACTION as comma separated sequence of actions to invoke
  --version                              Show version
  --web=true|yes|false|no|raw            treat ACTION as a web action or as a raw HTTP web action
```

_See code: [src/commands/action/create.ts](https://github.com//nimbella-corp/nimbella-cli/blob/v0.1.15/src/commands/action/create.ts)_

## `nim action:delete ACTIONNAME`

Deletes an Action

```
USAGE
  $ nim action:delete ACTIONNAME

OPTIONS
  -i, --insecure           bypass certificate check
  -u, --auth=auth          whisk auth
  -v, --verbose            Verbose output
  --apihost=apihost        whisk API host
  --apiversion=apiversion  whisk API version
  --cert=cert              client cert
  --debug=debug            Debug level output
  --help                   Show help
  --json                   output raw json
  --key=key                client key
  --version                Show version
```

_See code: [src/commands/action/delete.ts](https://github.com//nimbella-corp/nimbella-cli/blob/v0.1.15/src/commands/action/delete.ts)_

## `nim action:get ACTIONNAME`

Retrieves an Action

```
USAGE
  $ nim action:get ACTIONNAME

OPTIONS
  -i, --insecure           bypass certificate check
  -r, --url                get action url
  -u, --auth=auth          whisk auth
  -v, --verbose            Verbose output
  --apihost=apihost        whisk API host
  --apiversion=apiversion  whisk API version
  --cert=cert              client cert
  --debug=debug            Debug level output
  --help                   Show help
  --key=key                client key
  --save                   save action code to file corresponding with action name
  --save-as=save-as        file to save action code to
  --version                Show version
```

_See code: [src/commands/action/get.ts](https://github.com//nimbella-corp/nimbella-cli/blob/v0.1.15/src/commands/action/get.ts)_

## `nim action:invoke ACTIONNAME`

Invokes an Action

```
USAGE
  $ nim action:invoke ACTIONNAME

OPTIONS
  -P, --param-file=param-file  FILE containing parameter values in JSON format
  -b, --blocking               blocking invoke
  -i, --insecure               bypass certificate check
  -p, --param=param            parameter values in KEY VALUE format
  -r, --result                 blocking invoke; show only activation result (unless there is a failure)
  -u, --auth=auth              whisk auth
  -v, --verbose                Verbose output
  --apihost=apihost            whisk API host
  --apiversion=apiversion      whisk API version
  --cert=cert                  client cert
  --debug=debug                Debug level output
  --help                       Show help
  --key=key                    client key
  --version                    Show version
```

_See code: [src/commands/action/invoke.ts](https://github.com//nimbella-corp/nimbella-cli/blob/v0.1.15/src/commands/action/invoke.ts)_

## `nim action:list [PACKAGE]`

Lists all the Actions

```
USAGE
  $ nim action:list [PACKAGE]

OPTIONS
  -i, --insecure           bypass certificate check
  -l, --limit=limit        only return LIMIT number of actions from the collection (default 30)
  -n, --name               sort results by name
  -s, --skip=skip          exclude the first SKIP number of actions from the result
  -u, --auth=auth          whisk auth
  -v, --verbose            Verbose output
  --apihost=apihost        whisk API host
  --apiversion=apiversion  whisk API version
  --cert=cert              client cert
  --debug=debug            Debug level output
  --help                   Show help
  --json                   output raw json
  --key=key                client key
  --name-sort              sort results by name
  --version                Show version
```

_See code: [src/commands/action/list.ts](https://github.com//nimbella-corp/nimbella-cli/blob/v0.1.15/src/commands/action/list.ts)_

## `nim action:update ACTIONNAME [ACTIONPATH]`

Updates an Action

```
USAGE
  $ nim action:update ACTIONNAME [ACTIONPATH]

OPTIONS
  -A, --annotation-file=annotation-file  FILE containing annotation values in JSON format
  -E, --env-file=env-file                FILE containing environment variables in JSON format
  -P, --param-file=param-file            FILE containing parameter values in JSON format
  -a, --annotation=annotation            annotation values in KEY VALUE format
  -e, --env=env                          environment values in KEY VALUE format
  -i, --insecure                         bypass certificate check
  -l, --logsize=logsize                  the maximum log size LIMIT in MB for the action (default 10)
  -m, --memory=memory                    the maximum memory LIMIT in MB for the action (default 256)
  -p, --param=param                      parameter values in KEY VALUE format
  -t, --timeout=timeout                  the timeout LIMIT in milliseconds after which the action is terminated (default 60000)
  -u, --auth=auth                        whisk auth
  -v, --verbose                          Verbose output
  --apihost=apihost                      whisk API host
  --apiversion=apiversion                whisk API version
  --binary                               treat code artifact as binary
  --cert=cert                            client cert
  --debug=debug                          Debug level output
  --docker=docker                        use provided Docker image (a path on DockerHub) to run the action
  --help                                 Show help
  --json                                 output raw json
  --key=key                              client key
  --kind=kind                            the KIND of the action runtime (example: swift:default, nodejs:default)
  --main=main                            the name of the action entry point (function or fully-qualified method name when applicable)
  --sequence=sequence                    treat ACTION as comma separated sequence of actions to invoke
  --version                              Show version
  --web=true|yes|false|no|raw            treat ACTION as a web action or as a raw HTTP web action
```

_See code: [src/commands/action/update.ts](https://github.com//nimbella-corp/nimbella-cli/blob/v0.1.15/src/commands/action/update.ts)_

## `nim activation:get [ACTIVATIONID]`

Retrieves an Activation

```
USAGE
  $ nim activation:get [ACTIVATIONID]

OPTIONS
  -g, --logs               emit only the logs, stripped of time stamps and stream identifier
  -i, --insecure           bypass certificate check
  -l, --last               retrieves the most recent activation
  -u, --auth=auth          whisk auth
  -v, --verbose            Verbose output
  --apihost=apihost        whisk API host
  --apiversion=apiversion  whisk API version
  --cert=cert              client cert
  --debug=debug            Debug level output
  --help                   Show help
  --key=key                client key
  --version                Show version
```

_See code: [src/commands/activation/get.ts](https://github.com//nimbella-corp/nimbella-cli/blob/v0.1.15/src/commands/activation/get.ts)_

## `nim activation:list [ACTIVATIONID]`

Lists all the Activations

```
USAGE
  $ nim activation:list [ACTIVATIONID]

OPTIONS
  -f, --full               include full activation description
  -i, --insecure           bypass certificate check
  -l, --limit=limit        only return LIMIT number of activations from the collection with a maximum LIMIT of 200 activations (default 30)
  -s, --skip=skip          exclude the first SKIP number of activations from the result
  -u, --auth=auth          whisk auth
  -v, --verbose            Verbose output
  --apihost=apihost        whisk API host
  --apiversion=apiversion  whisk API version
  --cert=cert              client cert
  --debug=debug            Debug level output
  --help                   Show help
  --json                   output raw json
  --key=key                client key
  --since=since            return activations with timestamps later than SINCE; measured in milliseconds since Th, 01, Jan 1970
  --upto=upto              return activations with timestamps earlier than UPTO; measured in milliseconds since Th, 01, Jan 1970
  --version                Show version
```

_See code: [src/commands/activation/list.ts](https://github.com//nimbella-corp/nimbella-cli/blob/v0.1.15/src/commands/activation/list.ts)_

## `nim activation:logs [ACTIVATIONID]`

Retrieves the Logs for an Activation

```
USAGE
  $ nim activation:logs [ACTIVATIONID]

OPTIONS
  -c, --count=count        [default: 1] used with --last, return the last `count` activation logs. Max 5
  -i, --insecure           bypass certificate check
  -l, --last               retrieves the most recent activation logs
  -r, --strip              strip timestamp information and output first line only
  -u, --auth=auth          whisk auth
  -v, --verbose            Verbose output
  --apihost=apihost        whisk API host
  --apiversion=apiversion  whisk API version
  --cert=cert              client cert
  --debug=debug            Debug level output
  --help                   Show help
  --key=key                client key
  --version                Show version
```

_See code: [src/commands/activation/logs.ts](https://github.com//nimbella-corp/nimbella-cli/blob/v0.1.15/src/commands/activation/logs.ts)_

## `nim activation:result [ACTIVATIONID]`

Retrieves the Results for an Activation

```
USAGE
  $ nim activation:result [ACTIVATIONID]

OPTIONS
  -i, --insecure           bypass certificate check
  -l, --last               retrieves the most recent activation result
  -u, --auth=auth          whisk auth
  -v, --verbose            Verbose output
  --apihost=apihost        whisk API host
  --apiversion=apiversion  whisk API version
  --cert=cert              client cert
  --debug=debug            Debug level output
  --help                   Show help
  --key=key                client key
  --version                Show version
```

_See code: [src/commands/activation/result.ts](https://github.com//nimbella-corp/nimbella-cli/blob/v0.1.15/src/commands/activation/result.ts)_

## `nim auth:current`

Get current namespace with optional details

```
USAGE
  $ nim auth:current

OPTIONS
  -v, --verbose  Greater detail in error messages
  --all          Show all fields
  --apihost      Show API host
  --auth         Show API key
  --help         Show help
  --name         Show namespace name
  --redis        Show redis status
  --storage      Show storage status
```

_See code: [src/commands/auth/current.ts](https://github.com//nimbella-corp/nimbella-cli/blob/v0.1.15/src/commands/auth/current.ts)_

## `nim auth:github`

manage github accounts

```
USAGE
  $ nim auth:github

OPTIONS
  -a, --add            add another github account with a different user name
  -d, --delete=delete  forget a previously added github account
  -i, --initial        add your github account if you didn't specify it earlier
  -l, --list           list previously added github accounts
  -s, --switch=switch  switch to using a particular previously added github account
  -v, --verbose        Greater detail in error messages
  --help               Show help
  --show=show          show the access token currently associated with a username
```

_See code: [src/commands/auth/github.ts](https://github.com//nimbella-corp/nimbella-cli/blob/v0.1.15/src/commands/auth/github.ts)_

## `nim auth:list`

List all your Nimbella namespaces

```
USAGE
  $ nim auth:list

OPTIONS
  -v, --verbose  Greater detail in error messages
  --help         Show help
```

_See code: [src/commands/auth/list.ts](https://github.com//nimbella-corp/nimbella-cli/blob/v0.1.15/src/commands/auth/list.ts)_

## `nim auth:login [TOKEN]`

Gain access to a Nimbella namespace

```
USAGE
  $ nim auth:login [TOKEN]

ARGUMENTS
  TOKEN  string provided by Nimbella Corp

OPTIONS
  -u, --auth=auth    API key to use for authentication
  -v, --verbose      Greater detail in error messages
  --apihost=apihost  API host to use for authentication
  --help             Show help
```

_See code: [src/commands/auth/login.ts](https://github.com//nimbella-corp/nimbella-cli/blob/v0.1.15/src/commands/auth/login.ts)_

## `nim auth:logout NAMESPACE`

Drop access to a Nimbella namespace

```
USAGE
  $ nim auth:logout NAMESPACE

ARGUMENTS
  NAMESPACE  the namespace you are dropping

OPTIONS
  -v, --verbose      Greater detail in error messages
  --apihost=apihost  API host serving the namespace
  --help             Show help
```

_See code: [src/commands/auth/logout.ts](https://github.com//nimbella-corp/nimbella-cli/blob/v0.1.15/src/commands/auth/logout.ts)_

## `nim auth:switch NAMESPACE`

Switch to a different Nimbella namespace

```
USAGE
  $ nim auth:switch NAMESPACE

ARGUMENTS
  NAMESPACE  the namespace you are switching to

OPTIONS
  -v, --verbose      Greater detail in error messages
  --apihost=apihost  API host serving the target namespace
  --help             Show help
```

_See code: [src/commands/auth/switch.ts](https://github.com//nimbella-corp/nimbella-cli/blob/v0.1.15/src/commands/auth/switch.ts)_

## `nim autocomplete [SHELL]`

display autocomplete installation instructions

```
USAGE
  $ nim autocomplete [SHELL]

ARGUMENTS
  SHELL  shell type

OPTIONS
  -r, --refresh-cache  Refresh cache (ignores displaying instructions)

EXAMPLES
  $ nim autocomplete
  $ nim autocomplete bash
  $ nim autocomplete zsh
  $ nim autocomplete --refresh-cache
```

_See code: [@oclif/plugin-autocomplete](https://github.com/oclif/plugin-autocomplete/blob/v0.1.5/src/commands/autocomplete/index.ts)_

## `nim doc`

display the full documentation of this CLI

```
USAGE
  $ nim doc

OPTIONS
  -v, --verbose  Greater detail in error messages
  --help         Show help

ALIASES
  $ nim docs
```

_See code: [src/commands/doc.ts](https://github.com//nimbella-corp/nimbella-cli/blob/v0.1.15/src/commands/doc.ts)_

## `nim help [COMMAND]`

display help for nim

```
USAGE
  $ nim help [COMMAND]

ARGUMENTS
  COMMAND  command to show help for

OPTIONS
  --all  see all commands in CLI
```

_See code: [@oclif/plugin-help](https://github.com/oclif/plugin-help/blob/v2.2.3/src/commands/help.ts)_

## `nim info`

show information about this version of 'nim'

```
USAGE
  $ nim info

OPTIONS
  -v, --verbose  Greater detail in error messages
  --changes      Display the change history
  --help         Show help
  --license      Display the license
```

_See code: [src/commands/info.ts](https://github.com//nimbella-corp/nimbella-cli/blob/v0.1.15/src/commands/info.ts)_

## `nim key-value:del [NAMESPACE]`

Removes the specified keys and returns number of keys that were removed. A key is ignored if it does not exist.

```
USAGE
  $ nim key-value:del [NAMESPACE]

ARGUMENTS
  NAMESPACE  the namespace to perform operation in (current namespace if omitted)

OPTIONS
  -k, --key=key      the key to be deleted
  -v, --verbose      Greater detail in error messages
  --apihost=apihost  the API host of the namespace
  --help             Show help

ALIASES
  $ nim kv:del
```

_See code: [src/commands/key-value/del.ts](https://github.com//nimbella-corp/nimbella-cli/blob/v0.1.15/src/commands/key-value/del.ts)_

## `nim key-value:flush [NAMESPACE]`

Clears the Key Value Store, be cautious!

```
USAGE
  $ nim key-value:flush [NAMESPACE]

ARGUMENTS
  NAMESPACE  the namespace to perform operation in (current namespace if omitted)

OPTIONS
  -f, --force        just do it, omitting confirmatory prompt
  -v, --verbose      Greater detail in error messages
  --apihost=apihost  the API host of the namespace
  --help             Show help

ALIASES
  $ nim kv:flush
```

_See code: [src/commands/key-value/flush.ts](https://github.com//nimbella-corp/nimbella-cli/blob/v0.1.15/src/commands/key-value/flush.ts)_

## `nim key-value:get [NAMESPACE]`

Get Value for a Key

```
USAGE
  $ nim key-value:get [NAMESPACE]

ARGUMENTS
  NAMESPACE  the namespace to perform operation in (current namespace if omitted)

OPTIONS
  -k, --key=key      the key for which value is to be retrieved
  -v, --verbose      Greater detail in error messages
  --apihost=apihost  the API host of the namespace to list keys from
  --help             Show help

ALIASES
  $ nim kv:get
```

_See code: [src/commands/key-value/get.ts](https://github.com//nimbella-corp/nimbella-cli/blob/v0.1.15/src/commands/key-value/get.ts)_

## `nim key-value:getMany [NAMESPACE]`

Gets values for given Keys

```
USAGE
  $ nim key-value:getMany [NAMESPACE]

ARGUMENTS
  NAMESPACE  the namespace to perform operation in (current namespace if omitted)

OPTIONS
  -c, --count=count  the count to run to from start
  -k, --key=key      the key for which value is to be retrieved
  -s, --start=start  the index to start at
  -v, --verbose      Greater detail in error messages
  --apihost=apihost  the API host of the namespace to list keys from
  --help             Show help

ALIASES
  $ nim kv:getMany
```

_See code: [src/commands/key-value/getMany.ts](https://github.com//nimbella-corp/nimbella-cli/blob/v0.1.15/src/commands/key-value/getMany.ts)_

## `nim key-value:list [NAMESPACE]`

Lists Keys from Key Value Store

```
USAGE
  $ nim key-value:list [NAMESPACE]

ARGUMENTS
  NAMESPACE  the namespace to list keys from (current namespace if omitted)

OPTIONS
  -p, --pattern=pattern  the string pattern to match keys against
  -v, --verbose          Greater detail in error messages
  --apihost=apihost      the API host of the namespace to list keys from
  --help                 Show help

ALIASES
  $ nim kv:list
```

_See code: [src/commands/key-value/list.ts](https://github.com//nimbella-corp/nimbella-cli/blob/v0.1.15/src/commands/key-value/list.ts)_

## `nim key-value:llen [NAMESPACE]`

Returns the length of the list stored at key. If a key does not exist, it is interpreted as an empty list and 0 is returned. An error is returned when the value stored at key is not a list.

```
USAGE
  $ nim key-value:llen [NAMESPACE]

ARGUMENTS
  NAMESPACE  the namespace to perform operation in (current namespace if omitted)

OPTIONS
  -k, --key=key      the key to be queried for length
  -v, --verbose      Greater detail in error messages
  --apihost=apihost  the API host of the namespace
  --help             Show help

ALIASES
  $ nim kv:llen
```

_See code: [src/commands/key-value/llen.ts](https://github.com//nimbella-corp/nimbella-cli/blob/v0.1.15/src/commands/key-value/llen.ts)_

## `nim key-value:lrange [NAMESPACE]`

Returns the specified elements of the list stored at key. The offsets start and stop are zero-based indexes, with 0 being the first element of the list, 1 being the next element and so on.

```
USAGE
  $ nim key-value:lrange [NAMESPACE]

ARGUMENTS
  NAMESPACE  the namespace to perform operation in (current namespace if omitted)

OPTIONS
  -e, --end=end      the index to stop
  -k, --key=key      the key to be queried
  -s, --start=start  the index to start
  -v, --verbose      Greater detail in error messages
  --apihost=apihost  the API host of the namespace to list keys from
  --help             Show help

ALIASES
  $ nim kv:lrange
```

_See code: [src/commands/key-value/lrange.ts](https://github.com//nimbella-corp/nimbella-cli/blob/v0.1.15/src/commands/key-value/lrange.ts)_

## `nim key-value:rpush [NAMESPACE]`

Insert all the specified values at the tail of the list stored at key. It is created as an empty list before performing the push operation if the key does not exist. An error is returned when key holds such a value that is not a list

```
USAGE
  $ nim key-value:rpush [NAMESPACE]

ARGUMENTS
  NAMESPACE  the namespace to perform operation in (current namespace if omitted)

OPTIONS
  -k, --key=key      the key to be added at
  -v, --verbose      Greater detail in error messages
  --apihost=apihost  the API host of the namespace
  --help             Show help
  --value=value      the value to be added

ALIASES
  $ nim kv:rpush
```

_See code: [src/commands/key-value/rpush.ts](https://github.com//nimbella-corp/nimbella-cli/blob/v0.1.15/src/commands/key-value/rpush.ts)_

## `nim key-value:set [NAMESPACE]`

Sets the specified value at the specified key

```
USAGE
  $ nim key-value:set [NAMESPACE]

ARGUMENTS
  NAMESPACE  the namespace to perform operation in (current namespace if omitted)

OPTIONS
  -k, --key=key      the key to be added at
  -v, --verbose      Greater detail in error messages
  --apihost=apihost  the API host of the namespace
  --help             Show help
  --value=value      the value to be added

ALIASES
  $ nim kv:set
```

_See code: [src/commands/key-value/set.ts](https://github.com//nimbella-corp/nimbella-cli/blob/v0.1.15/src/commands/key-value/set.ts)_

## `nim key-value:setMany [NAMESPACE]`

Set Value for a Key

```
USAGE
  $ nim key-value:setMany [NAMESPACE]

ARGUMENTS
  NAMESPACE  the namespace to perform operation in (current namespace if omitted)

OPTIONS
  -c, --count=count  the count to run to from start
  -k, --key=key      the key to be set at
  -s, --start=start  the index to start at
  -v, --verbose      Greater detail in error messages
  --apihost=apihost  the API host of the namespace to list keys from
  --help             Show help
  --value=value      the value to be set

ALIASES
  $ nim kv:setMany
```

_See code: [src/commands/key-value/setMany.ts](https://github.com//nimbella-corp/nimbella-cli/blob/v0.1.15/src/commands/key-value/setMany.ts)_

## `nim namespace:clean [NAMESPACE]`

Remove content from a namespace

```
USAGE
  $ nim namespace:clean [NAMESPACE]

ARGUMENTS
  NAMESPACE  the namespace to clean (current namespace if omitted)

OPTIONS
  -u, --auth=auth    the API key for the namespace to be cleaned
  -v, --verbose      Greater detail in error messages
  --apihost=apihost  the API host of the namespace to be cleaned
  --force            just do it, omitting confirmatory prompt
  --help             Show help
  --justwhisk        Remove only OpenWhisk entities, leaving other content
```

_See code: [src/commands/namespace/clean.ts](https://github.com//nimbella-corp/nimbella-cli/blob/v0.1.15/src/commands/namespace/clean.ts)_

## `nim namespace:get`

Get triggers, actions, and rules in the registry for namespace

```
USAGE
  $ nim namespace:get

OPTIONS
  -i, --insecure           bypass certificate check
  -n, --name               sort results by name
  -u, --auth=auth          whisk auth
  -v, --verbose            Verbose output
  --apihost=apihost        whisk API host
  --apiversion=apiversion  whisk API version
  --cert=cert              client cert
  --debug=debug            Debug level output
  --help                   Show help
  --json                   output raw json
  --key=key                client key
  --name-sort              sort results by name
  --version                Show version
```

_See code: [src/commands/namespace/get.ts](https://github.com//nimbella-corp/nimbella-cli/blob/v0.1.15/src/commands/namespace/get.ts)_

## `nim objects:list [NAMESPACE]`

Lists Objects from Object Store

```
USAGE
  $ nim objects:list [NAMESPACE]

ARGUMENTS
  NAMESPACE  the namespace to list objects from (current namespace if omitted)

OPTIONS
  -l, --long         displays additional object info such as last update, owner and md5hash
  -v, --verbose      Greater detail in error messages
  --apihost=apihost  the API host of the namespace to list web content from
  --help             Show help
```

_See code: [src/commands/objects/list.ts](https://github.com//nimbella-corp/nimbella-cli/blob/v0.1.15/src/commands/objects/list.ts)_

## `nim package:bind PACKAGENAME BINDPACKAGENAME`

Bind parameters to a package

```
USAGE
  $ nim package:bind PACKAGENAME BINDPACKAGENAME

OPTIONS
  -A, --annotation-file=annotation-file  FILE containing annotation values in JSON format
  -P, --param-file=param-file            parameter to be passed to the package for json file
  -a, --annotation=annotation            annotation values in KEY VALUE format
  -i, --insecure                         bypass certificate check
  -p, --param=param                      parameters in key value pairs to be passed to the package
  -u, --auth=auth                        whisk auth
  -v, --verbose                          Verbose output
  --apihost=apihost                      whisk API host
  --apiversion=apiversion                whisk API version
  --cert=cert                            client cert
  --debug=debug                          Debug level output
  --help                                 Show help
  --json                                 output raw json
  --key=key                              client key
  --version                              Show version
```

_See code: [src/commands/package/bind.ts](https://github.com//nimbella-corp/nimbella-cli/blob/v0.1.15/src/commands/package/bind.ts)_

## `nim package:create PACKAGENAME`

Creates a Package

```
USAGE
  $ nim package:create PACKAGENAME

OPTIONS
  -A, --annotation-file=annotation-file  FILE containing annotation values in JSON format
  -P, --param-file=param-file            parameter to be passed to the package for json file
  -a, --annotation=annotation            annotation values in KEY VALUE format
  -i, --insecure                         bypass certificate check
  -p, --param=param                      parameters in key value pairs to be passed to the package
  -u, --auth=auth                        whisk auth
  -v, --verbose                          Verbose output
  --apihost=apihost                      whisk API host
  --apiversion=apiversion                whisk API version
  --cert=cert                            client cert
  --debug=debug                          Debug level output
  --help                                 Show help
  --json                                 output raw json
  --key=key                              client key
  --shared=true|yes|false|no             parameter to be passed to indicate whether package is shared or private
  --version                              Show version
```

_See code: [src/commands/package/create.ts](https://github.com//nimbella-corp/nimbella-cli/blob/v0.1.15/src/commands/package/create.ts)_

## `nim package:delete PACKAGENAME`

Deletes a Package

```
USAGE
  $ nim package:delete PACKAGENAME

OPTIONS
  -r, --recursive    delete the contained actions
  -u, --auth=auth    whisk auth
  --apihost=apihost  whisk API host
  --json             output raw json
```

_See code: [src/commands/package/delete.ts](https://github.com//nimbella-corp/nimbella-cli/blob/v0.1.15/src/commands/package/delete.ts)_

## `nim package:get PACKAGENAME`

Retrieves a Package

```
USAGE
  $ nim package:get PACKAGENAME

OPTIONS
  -i, --insecure           bypass certificate check
  -u, --auth=auth          whisk auth
  -v, --verbose            Verbose output
  --apihost=apihost        whisk API host
  --apiversion=apiversion  whisk API version
  --cert=cert              client cert
  --debug=debug            Debug level output
  --help                   Show help
  --key=key                client key
  --version                Show version
```

_See code: [src/commands/package/get.ts](https://github.com//nimbella-corp/nimbella-cli/blob/v0.1.15/src/commands/package/get.ts)_

## `nim package:list [NAMESPACE]`

Lists all the Packages

```
USAGE
  $ nim package:list [NAMESPACE]

OPTIONS
  -i, --insecure           bypass certificate check
  -l, --limit=limit        only return LIMIT number of packages from the collection (default 30)
  -n, --name               sort results by name
  -s, --skip=skip          exclude the first SKIP number of packages from the result
  -u, --auth=auth          whisk auth
  -v, --verbose            Verbose output
  --apihost=apihost        whisk API host
  --apiversion=apiversion  whisk API version
  --cert=cert              client cert
  --debug=debug            Debug level output
  --help                   Show help
  --json                   output raw json
  --key=key                client key
  --name-sort              sort results by name
  --version                Show version
```

_See code: [src/commands/package/list.ts](https://github.com//nimbella-corp/nimbella-cli/blob/v0.1.15/src/commands/package/list.ts)_

## `nim package:update PACKAGENAME`

Updates a Package

```
USAGE
  $ nim package:update PACKAGENAME

OPTIONS
  -A, --annotation-file=annotation-file  FILE containing annotation values in JSON format
  -P, --param-file=param-file            FILE containing parameter values in JSON format
  -a, --annotation=annotation            annotation values in KEY VALUE format
  -i, --insecure                         bypass certificate check
  -p, --param=param                      parameter values in KEY VALUE format
  -u, --auth=auth                        whisk auth
  -v, --verbose                          Verbose output
  --apihost=apihost                      whisk API host
  --apiversion=apiversion                whisk API version
  --cert=cert                            client cert
  --debug=debug                          Debug level output
  --help                                 Show help
  --json                                 output raw json
  --key=key                              client key
  --shared=true|yes|false|no             parameter to be passed to indicate whether package is shared or private
  --version                              Show version
```

_See code: [src/commands/package/update.ts](https://github.com//nimbella-corp/nimbella-cli/blob/v0.1.15/src/commands/package/update.ts)_

## `nim project:create [PROJECT]`

Create a Nimbella Project

```
USAGE
  $ nim project:create [PROJECT]

ARGUMENTS
  PROJECT  project path in the file system

OPTIONS
  -v, --verbose        Greater detail in error messages
  --[no-]clean         clean the namespace before every deploy
  --config             generate template config file
  --help               Show help
  --language=language  language for the sample (implies --sample
  --sample             start off with hello world (default language javascript)
  --target=target      target namespace for the project
```

_See code: [src/commands/project/create.ts](https://github.com//nimbella-corp/nimbella-cli/blob/v0.1.15/src/commands/project/create.ts)_

## `nim project:deploy [PROJECTS]`

Deploy Nimbella projects

```
USAGE
  $ nim project:deploy [PROJECTS]

ARGUMENTS
  PROJECTS  one or more paths to projects

OPTIONS
  -v, --verbose          Greater detail in error messages
  --apihost=apihost      API host to use
  --auth=auth            OpenWhisk auth token to use
  --env=env              path to environment file
  --exclude=exclude      project portions to exclude
  --help                 Show help
  --include=include      project portions to include
  --incremental          Deploy only changes since last deploy
  --insecure             Ignore SSL Certificates
  --target=target        the target namespace
  --verbose-build        Display build details
  --verbose-zip          Display start/end of zipping phase for each action
  --web-local=web-local  a local directory to receive web deploy, instead of uploading
  --yarn                 Use yarn instead of npm for node builds
```

_See code: [src/commands/project/deploy.ts](https://github.com//nimbella-corp/nimbella-cli/blob/v0.1.15/src/commands/project/deploy.ts)_

## `nim project:watch [PROJECTS]`

Watch Nimbella projects, deploying incrementally on change

```
USAGE
  $ nim project:watch [PROJECTS]

ARGUMENTS
  PROJECTS  one or more paths to projects

OPTIONS
  -v, --verbose          Greater detail in error messages
  --apihost=apihost      API host to use
  --auth=auth            OpenWhisk auth token to use
  --env=env              path to environment file
  --exclude=exclude      project portions to exclude
  --help                 Show help
  --include=include      project portions to include
  --insecure             Ignore SSL Certificates
  --target=target        the target namespace
  --verbose-build        Display build details
  --verbose-zip          Display start/end of zipping phase for each action
  --web-local=web-local  a local directory to receive web deploy, instead of uploading
  --yarn                 Use yarn instead of npm for node builds
```

_See code: [src/commands/project/watch.ts](https://github.com//nimbella-corp/nimbella-cli/blob/v0.1.15/src/commands/project/watch.ts)_

## `nim route:create BASEPATH RELPATH APIVERB ACTION`

create a new api route

```
USAGE
  $ nim route:create BASEPATH RELPATH APIVERB ACTION

ARGUMENTS
  BASEPATH  The base path of the api
  RELPATH   The path of the api relative to the base path
  APIVERB   (get|post|put|patch|delete|head|options) The http verb
  ACTION    The action to call

OPTIONS
  -i, --insecure                                    bypass certificate check
  -n, --apiname=apiname                             Friendly name of the API; ignored when CFG_FILE is specified (default BASE_PATH)
  -r, --response-type=html|http|json|text|svg|json  [default: json] Set the web action response TYPE.
  -u, --auth=auth                                   whisk auth
  -v, --verbose                                     Verbose output
  --apihost=apihost                                 whisk API host
  --apiversion=apiversion                           whisk API version
  --cert=cert                                       client cert
  --debug=debug                                     Debug level output
  --help                                            Show help
  --key=key                                         client key
  --version                                         Show version
```

_See code: [src/commands/route/create.ts](https://github.com//nimbella-corp/nimbella-cli/blob/v0.1.15/src/commands/route/create.ts)_

## `nim route:delete BASEPATHORAPINAME [RELPATH] [APIVERB]`

delete an API

```
USAGE
  $ nim route:delete BASEPATHORAPINAME [RELPATH] [APIVERB]

ARGUMENTS
  BASEPATHORAPINAME  The base path or api name
  RELPATH            The path of the api relative to the base path
  APIVERB            (get|post|put|patch|delete|head|options) The http verb

OPTIONS
  -i, --insecure           bypass certificate check
  -u, --auth=auth          whisk auth
  -v, --verbose            Verbose output
  --apihost=apihost        whisk API host
  --apiversion=apiversion  whisk API version
  --cert=cert              client cert
  --debug=debug            Debug level output
  --help                   Show help
  --key=key                client key
  --version                Show version
```

_See code: [src/commands/route/delete.ts](https://github.com//nimbella-corp/nimbella-cli/blob/v0.1.15/src/commands/route/delete.ts)_

## `nim route:get BASEPATHORAPINAME`

get API details

```
USAGE
  $ nim route:get BASEPATHORAPINAME

ARGUMENTS
  BASEPATHORAPINAME  The base path or api name

OPTIONS
  -i, --insecure           bypass certificate check
  -u, --auth=auth          whisk auth
  -v, --verbose            Verbose output
  --apihost=apihost        whisk API host
  --apiversion=apiversion  whisk API version
  --cert=cert              client cert
  --debug=debug            Debug level output
  --help                   Show help
  --key=key                client key
  --version                Show version
```

_See code: [src/commands/route/get.ts](https://github.com//nimbella-corp/nimbella-cli/blob/v0.1.15/src/commands/route/get.ts)_

## `nim route:list [BASEPATH] [RELPATH] [APIVERB]`

List routes/apis

```
USAGE
  $ nim route:list [BASEPATH] [RELPATH] [APIVERB]

ARGUMENTS
  BASEPATH  The base path of the api
  RELPATH   The path of the api relative to the base path
  APIVERB   (get|post|put|patch|delete|head|options) The http verb

OPTIONS
  -i, --insecure           bypass certificate check
  -l, --limit=limit        [default: 30] only return LIMIT number of triggers from the collection (default 30)
  -s, --skip=skip          exclude the first SKIP number of triggers from the result
  -u, --auth=auth          whisk auth
  -v, --verbose            Verbose output
  --apihost=apihost        whisk API host
  --apiversion=apiversion  whisk API version
  --cert=cert              client cert
  --debug=debug            Debug level output
  --help                   Show help
  --json                   output raw json
  --key=key                client key
  --version                Show version
```

_See code: [src/commands/route/list.ts](https://github.com//nimbella-corp/nimbella-cli/blob/v0.1.15/src/commands/route/list.ts)_

## `nim rule:create NAME TRIGGER ACTION`

Create a Rule

```
USAGE
  $ nim rule:create NAME TRIGGER ACTION

ARGUMENTS
  NAME     Name of the rule
  TRIGGER  Name of the trigger
  ACTION   Name of the action

OPTIONS
  -i, --insecure           bypass certificate check
  -u, --auth=auth          whisk auth
  -v, --verbose            Verbose output
  --apihost=apihost        whisk API host
  --apiversion=apiversion  whisk API version
  --cert=cert              client cert
  --debug=debug            Debug level output
  --help                   Show help
  --json                   output raw json
  --key=key                client key
  --version                Show version
```

_See code: [src/commands/rule/create.ts](https://github.com//nimbella-corp/nimbella-cli/blob/v0.1.15/src/commands/rule/create.ts)_

## `nim rule:delete NAME`

Delete a Rule

```
USAGE
  $ nim rule:delete NAME

ARGUMENTS
  NAME  Name of the rule

OPTIONS
  -i, --insecure           bypass certificate check
  -u, --auth=auth          whisk auth
  -v, --verbose            Verbose output
  --apihost=apihost        whisk API host
  --apiversion=apiversion  whisk API version
  --cert=cert              client cert
  --debug=debug            Debug level output
  --help                   Show help
  --json                   output raw json
  --key=key                client key
  --version                Show version
```

_See code: [src/commands/rule/delete.ts](https://github.com//nimbella-corp/nimbella-cli/blob/v0.1.15/src/commands/rule/delete.ts)_

## `nim rule:disable NAME`

Disable a Rule

```
USAGE
  $ nim rule:disable NAME

ARGUMENTS
  NAME  Name of the rule

OPTIONS
  -i, --insecure           bypass certificate check
  -u, --auth=auth          whisk auth
  -v, --verbose            Verbose output
  --apihost=apihost        whisk API host
  --apiversion=apiversion  whisk API version
  --cert=cert              client cert
  --debug=debug            Debug level output
  --help                   Show help
  --key=key                client key
  --version                Show version
```

_See code: [src/commands/rule/disable.ts](https://github.com//nimbella-corp/nimbella-cli/blob/v0.1.15/src/commands/rule/disable.ts)_

## `nim rule:enable NAME`

Enable a Rule

```
USAGE
  $ nim rule:enable NAME

ARGUMENTS
  NAME  Name of the rule

OPTIONS
  -i, --insecure           bypass certificate check
  -u, --auth=auth          whisk auth
  -v, --verbose            Verbose output
  --apihost=apihost        whisk API host
  --apiversion=apiversion  whisk API version
  --cert=cert              client cert
  --debug=debug            Debug level output
  --help                   Show help
  --key=key                client key
  --version                Show version
```

_See code: [src/commands/rule/enable.ts](https://github.com//nimbella-corp/nimbella-cli/blob/v0.1.15/src/commands/rule/enable.ts)_

## `nim rule:get NAME`

Retrieves a Rule

```
USAGE
  $ nim rule:get NAME

ARGUMENTS
  NAME  Name of the rule

OPTIONS
  -i, --insecure           bypass certificate check
  -u, --auth=auth          whisk auth
  -v, --verbose            Verbose output
  --apihost=apihost        whisk API host
  --apiversion=apiversion  whisk API version
  --cert=cert              client cert
  --debug=debug            Debug level output
  --help                   Show help
  --key=key                client key
  --version                Show version
```

_See code: [src/commands/rule/get.ts](https://github.com//nimbella-corp/nimbella-cli/blob/v0.1.15/src/commands/rule/get.ts)_

## `nim rule:list`

Retrieves a list of Rules

```
USAGE
  $ nim rule:list

OPTIONS
  -i, --insecure           bypass certificate check
  -l, --limit=limit        [default: 30] Limit number of rules returned. Default 30
  -n, --name               sort results by name
  -s, --skip=skip          Skip number of rules returned
  -u, --auth=auth          whisk auth
  -v, --verbose            Verbose output
  --apihost=apihost        whisk API host
  --apiversion=apiversion  whisk API version
  --cert=cert              client cert
  --debug=debug            Debug level output
  --help                   Show help
  --json                   output raw json
  --key=key                client key
  --name-sort              sort results by name
  --version                Show version
```

_See code: [src/commands/rule/list.ts](https://github.com//nimbella-corp/nimbella-cli/blob/v0.1.15/src/commands/rule/list.ts)_

## `nim rule:status NAME`

Gets the status of a rule

```
USAGE
  $ nim rule:status NAME

ARGUMENTS
  NAME  Name of the rule

OPTIONS
  -i, --insecure           bypass certificate check
  -u, --auth=auth          whisk auth
  -v, --verbose            Verbose output
  --apihost=apihost        whisk API host
  --apiversion=apiversion  whisk API version
  --cert=cert              client cert
  --debug=debug            Debug level output
  --help                   Show help
  --key=key                client key
  --version                Show version
```

_See code: [src/commands/rule/status.ts](https://github.com//nimbella-corp/nimbella-cli/blob/v0.1.15/src/commands/rule/status.ts)_

## `nim rule:update NAME TRIGGER ACTION`

Update a Rule

```
USAGE
  $ nim rule:update NAME TRIGGER ACTION

ARGUMENTS
  NAME     Name of the rule
  TRIGGER  Name of the trigger
  ACTION   Name of the action

OPTIONS
  -i, --insecure           bypass certificate check
  -u, --auth=auth          whisk auth
  -v, --verbose            Verbose output
  --apihost=apihost        whisk API host
  --apiversion=apiversion  whisk API version
  --cert=cert              client cert
  --debug=debug            Debug level output
  --help                   Show help
  --json                   output raw json
  --key=key                client key
  --version                Show version
```

_See code: [src/commands/rule/update.ts](https://github.com//nimbella-corp/nimbella-cli/blob/v0.1.15/src/commands/rule/update.ts)_

## `nim trigger:create TRIGGERNAME`

Create a trigger

```
USAGE
  $ nim trigger:create TRIGGERNAME

ARGUMENTS
  TRIGGERNAME  The name of the trigger

OPTIONS
  -A, --annotation-file=annotation-file  FILE containing annotation values in JSON format
  -P, --param-file=param-file            FILE containing parameter values in JSON format
  -a, --annotation=annotation            annotation values in KEY VALUE format
  -f, --feed=feed                        trigger feed action name
  -i, --insecure                         bypass certificate check
  -p, --param=param                      parameter values in KEY VALUE format
  -u, --auth=auth                        whisk auth
  -v, --verbose                          Verbose output
  --apihost=apihost                      whisk API host
  --apiversion=apiversion                whisk API version
  --cert=cert                            client cert
  --debug=debug                          Debug level output
  --help                                 Show help
  --key=key                              client key
  --version                              Show version
```

_See code: [src/commands/trigger/create.ts](https://github.com//nimbella-corp/nimbella-cli/blob/v0.1.15/src/commands/trigger/create.ts)_

## `nim trigger:delete TRIGGERPATH`

Delete a Trigger

```
USAGE
  $ nim trigger:delete TRIGGERPATH

ARGUMENTS
  TRIGGERPATH  The name of the trigger, in the format /NAMESPACE/NAME

OPTIONS
  -i, --insecure           bypass certificate check
  -u, --auth=auth          whisk auth
  -v, --verbose            Verbose output
  --apihost=apihost        whisk API host
  --apiversion=apiversion  whisk API version
  --cert=cert              client cert
  --debug=debug            Debug level output
  --help                   Show help
  --key=key                client key
  --version                Show version
```

_See code: [src/commands/trigger/delete.ts](https://github.com//nimbella-corp/nimbella-cli/blob/v0.1.15/src/commands/trigger/delete.ts)_

## `nim trigger:fire TRIGGERNAME`

Fire a trigger

```
USAGE
  $ nim trigger:fire TRIGGERNAME

ARGUMENTS
  TRIGGERNAME  The name of the trigger

OPTIONS
  -P, --param-file=param-file  FILE containing parameter values in JSON format
  -i, --insecure               bypass certificate check
  -p, --param=param            parameter values in KEY VALUE format
  -u, --auth=auth              whisk auth
  -v, --verbose                Verbose output
  --apihost=apihost            whisk API host
  --apiversion=apiversion      whisk API version
  --cert=cert                  client cert
  --debug=debug                Debug level output
  --help                       Show help
  --key=key                    client key
  --version                    Show version
```

_See code: [src/commands/trigger/fire.ts](https://github.com//nimbella-corp/nimbella-cli/blob/v0.1.15/src/commands/trigger/fire.ts)_

## `nim trigger:get TRIGGERPATH`

Get a trigger

```
USAGE
  $ nim trigger:get TRIGGERPATH

ARGUMENTS
  TRIGGERPATH  The name/path of the trigger, in the format /NAMESPACE/NAME

OPTIONS
  -i, --insecure           bypass certificate check
  -u, --auth=auth          whisk auth
  -v, --verbose            Verbose output
  --apihost=apihost        whisk API host
  --apiversion=apiversion  whisk API version
  --cert=cert              client cert
  --debug=debug            Debug level output
  --help                   Show help
  --key=key                client key
  --version                Show version
```

_See code: [src/commands/trigger/get.ts](https://github.com//nimbella-corp/nimbella-cli/blob/v0.1.15/src/commands/trigger/get.ts)_

## `nim trigger:list`

Lists all of your triggers

```
USAGE
  $ nim trigger:list

OPTIONS
  -i, --insecure           bypass certificate check
  -l, --limit=limit        [default: 30] only return LIMIT number of triggers from the collection (default 30)
  -n, --name               sort results by name
  -s, --skip=skip          exclude the first SKIP number of triggers from the result
  -u, --auth=auth          whisk auth
  -v, --verbose            Verbose output
  --apihost=apihost        whisk API host
  --apiversion=apiversion  whisk API version
  --cert=cert              client cert
  --debug=debug            Debug level output
  --help                   Show help
  --json                   output raw json
  --key=key                client key
  --name-sort              sort results by name
  --version                Show version
```

_See code: [src/commands/trigger/list.ts](https://github.com//nimbella-corp/nimbella-cli/blob/v0.1.15/src/commands/trigger/list.ts)_

## `nim trigger:update TRIGGERNAME`

Update or create a trigger

```
USAGE
  $ nim trigger:update TRIGGERNAME

ARGUMENTS
  TRIGGERNAME  The name of the trigger

OPTIONS
  -A, --annotation-file=annotation-file  FILE containing annotation values in JSON format
  -P, --param-file=param-file            FILE containing parameter values in JSON format
  -a, --annotation=annotation            annotation values in KEY VALUE format
  -i, --insecure                         bypass certificate check
  -p, --param=param                      parameter values in KEY VALUE format
  -u, --auth=auth                        whisk auth
  -v, --verbose                          Verbose output
  --apihost=apihost                      whisk API host
  --apiversion=apiversion                whisk API version
  --cert=cert                            client cert
  --debug=debug                          Debug level output
  --help                                 Show help
  --key=key                              client key
  --version                              Show version
```

_See code: [src/commands/trigger/update.ts](https://github.com//nimbella-corp/nimbella-cli/blob/v0.1.15/src/commands/trigger/update.ts)_

## `nim update [CHANNEL]`

update the nim CLI

```
USAGE
  $ nim update [CHANNEL]
```

_See code: [@oclif/plugin-update](https://github.com/oclif/plugin-update/blob/v1.3.9/src/commands/update.ts)_

## `nim web:list [NAMESPACE]`

Lists Web Content

```
USAGE
  $ nim web:list [NAMESPACE]

ARGUMENTS
  NAMESPACE  the namespace to list web content from (current namespace if omitted)

OPTIONS
  -l, --long         displays additional file info such as last update, owner and md5hash
  -v, --verbose      Greater detail in error messages
  --apihost=apihost  the API host of the namespace to list web content from
  --help             Show help
```

_See code: [src/commands/web/list.ts](https://github.com//nimbella-corp/nimbella-cli/blob/v0.1.15/src/commands/web/list.ts)_
