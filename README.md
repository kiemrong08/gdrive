gdrive
======


## Overview
gdrive is a command line utility for interacting with Google Drive.

## Prerequisites
None, binaries are statically linked.
If you want to compile from source you need the [go toolchain](http://golang.org/doc/install).

## Installation
Download `gdrive` from one of the links below. On unix systems
run `chmod +x gdrive` after download to make the binary executable.
The first time gdrive is launched, you will be prompted for a verification code.
The code is obtained by following the printed url and authenticating with the
google account for the drive you want access to. This will create a token file
inside the .gdrive folder in your home directory. Note that anyone with access
to this file will also have access to your google drive.
If you want to manage multiple drives you can use the global `--config` flag
or set the environment variable `GDRIVE_CONFIG_DIR`.
Example: `GDRIVE_CONFIG_DIR="/home/user/.gdrive-secondary" gdrive list`
You will be prompted for a new verification code if the folder does not exist.

### Downloads
| Filename               | Version | Description        | Shasum                                   |
|:-----------------------|:--------|:-------------------|:-----------------------------------------|
| [gdrive-osx-x64](https://docs.google.com/uc?id=0B3X9GlR6EmbnZUM0bXRBeUpYQ00&export=download) | 2.0.1 | OS X 64-bit | 180bc98408c7ec6deac6a66bbd9c307c4348ae6f |
| [gdrive-osx-386](https://docs.google.com/uc?id=0B3X9GlR6EmbnM05hQXhvWm9EOHM&export=download) | 2.0.1 | OS X 32-bit | 366ee217d4327a1855245d8c4a1204f4831eb979 |
| [gdrive-osx-arm](https://docs.google.com/uc?id=0B3X9GlR6EmbnelYxRU5LbEVfVzQ&export=download) | 2.0.1 | OS X arm | cdc31f83e50560a7f8fbf8a25b9c87c945d1407f |
| [gdrive-linux-x64](https://docs.google.com/uc?id=0B3X9GlR6EmbnWksyTEtCM0VfaFE&export=download) | 2.0.1 | Linux 64-bit | c636778c4a2c76e47ac731c142f4219a19c30263 |
| [gdrive-linux-386](https://docs.google.com/uc?id=0B3X9GlR6EmbnbndOUW50ZVllZ3M&export=download) | 2.0.1 | Linux 32-bit | 0968993e4a70a594e0f315034640fd811977e4f1 |
| [gdrive-linux-rpi](https://docs.google.com/uc?id=0B3X9GlR6EmbnbVRIelM5SG5zcmM&export=download) | 2.0.1 | Linux Raspberry Pi | 7865a1e96e70791aa0f33cb758e6cda7886be240 |
| [gdrive-linux-arm64](https://docs.google.com/uc?id=0B3X9GlR6EmbnNkxrQ3VzOGNMNWc&export=download) | 2.0.1 | Linux arm 64-bit | 00b293e4501da64e956d32b7c1589a014b541abe |
| [gdrive-linux-arm](https://docs.google.com/uc?id=0B3X9GlR6EmbnLW51cVJrazVLOG8&export=download) | 2.0.1 | Linux arm 32-bit | 3577a6462dafc47823d5ed053a978af84a99c5af |
| [gdrive-linux-mips64](https://docs.google.com/uc?id=0B3X9GlR6EmbnTS1fejFtaDMyLU0&export=download) | 2.0.1 | Linux mips 64-bit | e1e5992a5635467b84f149435544d980e99f30c6 |
| [gdrive-linux-mips64le](https://docs.google.com/uc?id=0B3X9GlR6EmbnV3pJU0ZBTEg0a2M&export=download) | 2.0.1 | Linux mips 64-bit le | 8273d53fc21b6028de781958c6f224f41c0a92db |
| [gdrive-linux-ppc64](https://docs.google.com/uc?id=0B3X9GlR6EmbnOXNPM01ITHl3NUk&export=download) | 2.0.1 | Linux PPC 64-bit | fc1409b9960ae4a209331e40a4cd9b10a789f8e6 |
| [gdrive-linux-ppc64le](https://docs.google.com/uc?id=0B3X9GlR6EmbnRVBCRlpXNl95bW8&export=download) | 2.0.1 | Linux PPC 64-bit le | 7a09ed4b43c31198efdf4e4a7da1e196cd3cd54f |
| [gdrive-windows-386.exe](https://docs.google.com/uc?id=0B3X9GlR6EmbncnpncGpZX0pULUU&export=download) | 2.0.1 | Window 32-bit | 134480ca113d03b91dbfa43326704b57f07ca547 |
| [gdrive-windows-x64.exe](https://docs.google.com/uc?id=0B3X9GlR6EmbncWNLOS1KYWhLVFE&export=download) | 2.0.1 | Windows 64-bit | c68df6e77aa7fa412bfe318ab270e1245a24966b |
| [gdrive-dragonfly-x64](https://docs.google.com/uc?id=0B3X9GlR6EmbnX1FiZzFaN1hRekk&export=download) | 2.0.1 | DragonFly BSD 64-bit | 0116d291a859152a4af842254eb88102c18f9ad6 |
| [gdrive-freebsd-x64](https://docs.google.com/uc?id=0B3X9GlR6Embnck8wR0ozV3J2WHM&export=download) | 2.0.1 | FreeBSD 64-bit | 0ab7d8509efcbbf41a4c684f9942c749706ea8ab |
| [gdrive-freebsd-386](https://docs.google.com/uc?id=0B3X9GlR6EmbnVUtwX010YUlENWs&export=download) | 2.0.1 | FreeBSD 32-bit | 4e1ac2aeeed59df1d8636641b796aad54ade42d2 |
| [gdrive-freebsd-arm](https://docs.google.com/uc?id=0B3X9GlR6EmbncXV3SU9NZDc3X3M&export=download) | 2.0.1 | FreeBSD arm | 1220f7f75579b28205d302f1e8ad0faeefc5d188 |
| [gdrive-netbsd-x64](https://docs.google.com/uc?id=0B3X9GlR6EmbnUk5JMVFiS0pKZW8&export=download) | 2.0.1 | NetBSD 64-bit | dba9e9f57b6ed3c370961e95efaea1ed0ea4429f |
| [gdrive-netbsd-386](https://docs.google.com/uc?id=0B3X9GlR6EmbnLWZRTy1LX1kxUkE&export=download) | 2.0.1 | NetBSD 32-bit | 8303ec4f0f7ba2acecc4509e0e73f8bf1eb2cd68 |
| [gdrive-netbsd-arm](https://docs.google.com/uc?id=0B3X9GlR6EmbnQUNFOWxBYmdjUEk&export=download) | 2.0.1 | NetBSD arm | 84aeb602e0cfbb09a35fff97f2af5990673f9bee |
| [gdrive-openbsd-x64](https://docs.google.com/uc?id=0B3X9GlR6EmbnYk50VlVuNUhuaVE&export=download) | 2.0.1 | OpenBSD 64-bit | 729794ef7cfc320cab84fd78e3113f5fdd476ac6 |
| [gdrive-openbsd-386](https://docs.google.com/uc?id=0B3X9GlR6EmbnOExCLVNYakJiSUk&export=download) | 2.0.1 | OpenBSD 32-bit | a1f45252d86ae238ce17b49c226b218aec805a02 |
| [gdrive-openbsd-arm](https://docs.google.com/uc?id=0B3X9GlR6EmbnN1htLTBSSElRUDQ&export=download) | 2.0.1 | OpenBSD arm | 5a732b15a4d36e61768388e323807e9a2fccb4bc |
| [gdrive-solaris-x64](https://docs.google.com/uc?id=0B3X9GlR6EmbnSEpJSDBidHNDNkE&export=download) | 2.0.1 | Solaris 64-bit | 82dc342873693b37302fc8f3cb97a667bae6e41c |
| [gdrive-plan9-x64](https://docs.google.com/uc?id=0B3X9GlR6EmbnZWMzR3pyZlZ0cFU&export=download) | 2.0.1 | Plan9 64-bit | e92e4a25517116c4fd466142baab03e0b9d11772 |
| [gdrive-plan9-386](https://docs.google.com/uc?id=0B3X9GlR6EmbnOXV4d0dNeGZCR00&export=download) | 2.0.1 | Plan9 32-bit | efdfced751ca43995ad28dc1aa96b29a8c237433 |

## Compile from source
```bash
git clone https://github.com/prasmussen/gdrive.git
cd gdrive
go get ./...
go build -o gdrive
```

## Gdrive 2
Gdrive 2 is more or less a full rewrite and is not backwards compatible
with gdrive 1 as all the command line arguments has changed slightly.
Gdrive 2 uses version 3 of the google drive api and my google-api-go-client
fork is no longer needed.

### Syncing
Gdrive 2 supports basic syncing. It only syncs one way at the time and works
more like rsync than e.g. dropbox. Files that are synced to google drive
are tagged with an appProperty so that the files on drive can be traversed
faster. This means that you can't upload files with `gdrive upload` into
a sync directory as the files would be missing the sync tag, and would be
ignored by the sync commands.
The current implementation is slow and uses a lot of memory if you are
syncing many files. Currently only one file is uploaded at the time,
the speed can be improved in the future by uploading several files concurrently.
To learn more see usage and the examples below.

#### .gdriveignore
Placing a .gdriveignore in the root of your sync directory can be used to
skip certain files from being synced. .gdriveignore follows the same
rules as [.gitignore](https://git-scm.com/docs/gitignore).


## Usage
```
gdrive [global] list [options]                                 List files
gdrive [global] download [options] <fileId>                    Download file or directory
gdrive [global] download query [options] <query>               Download all files and directories matching query
gdrive [global] upload [options] <path>                        Upload file or directory
gdrive [global] upload - [options] <name>                      Upload file from stdin
gdrive [global] update [options] <fileId> <path>               Update file, this creates a new revision of the file
gdrive [global] info [options] <fileId>                        Show file info
gdrive [global] mkdir [options] <name>                         Create directory
gdrive [global] share [options] <fileId>                       Share file or directory
gdrive [global] share list <fileId>                            List files permissions
gdrive [global] share revoke <fileId> <permissionId>           Revoke permission
gdrive [global] delete [options] <fileId>                      Delete file or directory
gdrive [global] sync list [options]                            List all syncable directories on drive
gdrive [global] sync content [options] <fileId>                List content of syncable directory
gdrive [global] sync download [options] <fileId> <path>        Sync drive directory to local directory
gdrive [global] sync upload [options] <path> <fileId>          Sync local directory to drive
gdrive [global] changes [options]                              List file changes
gdrive [global] revision list [options] <fileId>               List file revisions
gdrive [global] revision download [options] <fileId> <revId>   Download revision
gdrive [global] revision delete <fileId> <revId>               Delete file revision
gdrive [global] import [options] <path>                        Upload and convert file to a google document, see 'about import' for available conversions
gdrive [global] export [options] <fileId>                      Export a google document
gdrive [global] about [options]                                Google drive metadata, quota usage
gdrive [global] about import                                   Show supported import formats
gdrive [global] about export                                   Show supported export formats
gdrive version                                                 Print application version
gdrive help                                                    Print help
gdrive help <command>                                          Print command help
gdrive help <command> <subcommand>                             Print subcommand help
```

#### List files
```
gdrive [global] list [options]

global:
  -c, --config <configDir>         Application path, default: /Users/<user>/.gdrive
  --refresh-token <refreshToken>   Oauth refresh token used to get access token (for advanced users)
  --access-token <accessToken>     Oauth access token, only recommended for short-lived requests because of short lifetime (for advanced users)

options:
  -m, --max <maxFiles>       Max files to list, default: 30
  -q, --query <query>        Default query: "trashed = false and 'me' in owners". See https://developers.google.com/drive/search-parameters
  --order <sortOrder>        Sort order. See https://godoc.org/google.golang.org/api/drive/v3#FilesListCall.OrderBy
  --name-width <nameWidth>   Width of name column, default: 40, minimum: 9, use 0 for full width
  --absolute                 Show absolute path to file (will only show path from first parent)
  --no-header                Dont print the header
  --bytes                    Size in bytes
```

#### Download file or directory
```
gdrive [global] download [options] <fileId>

global:
  -c, --config <configDir>         Application path, default: /Users/<user>/.gdrive
  --refresh-token <refreshToken>   Oauth refresh token used to get access token (for advanced users)
  --access-token <accessToken>     Oauth access token, only recommended for short-lived requests because of short lifetime (for advanced users)

options:
  -f, --force       Overwrite existing file
  -r, --recursive   Download directory recursively, documents will be skipped
  --path <path>     Download path
  --delete          Delete remote file when download is successful
  --no-progress     Hide progress
  --stdout          Write file content to stdout
```

#### Download all files and directories matching query
```
gdrive [global] download query [options] <query>

global:
  -c, --config <configDir>         Application path, default: /Users/<user>/.gdrive
  --refresh-token <refreshToken>   Oauth refresh token used to get access token (for advanced users)
  --access-token <accessToken>     Oauth access token, only recommended for short-lived requests because of short lifetime (for advanced users)

options:
  -f, --force       Overwrite existing file
  -r, --recursive   Download directories recursively, documents will be skipped
  --path <path>     Download path
  --no-progress     Hide progress
```

#### Upload file or directory
```
gdrive [global] upload [options] <path>

global:
  -c, --config <configDir>         Application path, default: /Users/<user>/.gdrive
  --refresh-token <refreshToken>   Oauth refresh token used to get access token (for advanced users)
  --access-token <accessToken>     Oauth access token, only recommended for short-lived requests because of short lifetime (for advanced users)

options:
  -r, --recursive           Upload directory recursively
  -p, --parent <parent>     Parent id, used to upload file to a specific directory, can be specified multiple times to give many parents
  --name <name>             Filename
  --no-progress             Hide progress
  --mime <mime>             Force mime type
  --share                   Share file
  --delete                  Delete local file when upload is successful
  --chunksize <chunksize>   Set chunk size in bytes, default: 8388608
```

#### Upload file from stdin
```
gdrive [global] upload - [options] <name>

global:
  -c, --config <configDir>         Application path, default: /Users/<user>/.gdrive
  --refresh-token <refreshToken>   Oauth refresh token used to get access token (for advanced users)
  --access-token <accessToken>     Oauth access token, only recommended for short-lived requests because of short lifetime (for advanced users)

options:
  -p, --parent <parent>     Parent id, used to upload file to a specific directory, can be specified multiple times to give many parents
  --chunksize <chunksize>   Set chunk size in bytes, default: 8388608
  --mime <mime>             Force mime type
  --share                   Share file
  --no-progress             Hide progress
```

#### Update file, this creates a new revision of the file
```
gdrive [global] update [options] <fileId> <path>

global:
  -c, --config <configDir>         Application path, default: /Users/<user>/.gdrive
  --refresh-token <refreshToken>   Oauth refresh token used to get access token (for advanced users)
  --access-token <accessToken>     Oauth access token, only recommended for short-lived requests because of short lifetime (for advanced users)

options:
  -p, --parent <parent>     Parent id, used to upload file to a specific directory, can be specified multiple times to give many parents
  --name <name>             Filename
  --no-progress             Hide progress
  --mime <mime>             Force mime type
  --chunksize <chunksize>   Set chunk size in bytes, default: 8388608
```

#### Show file info
```
gdrive [global] info [options] <fileId>

global:
  -c, --config <configDir>         Application path, default: /Users/<user>/.gdrive
  --refresh-token <refreshToken>   Oauth refresh token used to get access token (for advanced users)
  --access-token <accessToken>     Oauth access token, only recommended for short-lived requests because of short lifetime (for advanced users)

options:
  --bytes   Show size in bytes
```

#### Create directory
```
gdrive [global] mkdir [options] <name>

global:
  -c, --config <configDir>         Application path, default: /Users/<user>/.gdrive
  --refresh-token <refreshToken>   Oauth refresh token used to get access token (for advanced users)
  --access-token <accessToken>     Oauth access token, only recommended for short-lived requests because of short lifetime (for advanced users)

options:
  -p, --parent <parent>   Parent id of created directory, can be specified multiple times to give many parents
```

#### Share file or directory
```
gdrive [global] share [options] <fileId>

global:
  -c, --config <configDir>         Application path, default: /Users/<user>/.gdrive
  --refresh-token <refreshToken>   Oauth refresh token used to get access token (for advanced users)
  --access-token <accessToken>     Oauth access token, only recommended for short-lived requests because of short lifetime (for advanced users)

options:
  --role <role>     Share role: owner/writer/commenter/reader, default: reader
  --type <type>     Share type: user/group/domain/anyone, default: anyone
  --email <email>   The email address of the user or group to share the file with. Requires 'user' or 'group' as type
  --discoverable    Make file discoverable by search engines
  --revoke          Delete all sharing permissions (owner roles will be skipped)
```

#### List files permissions
```
gdrive [global] share list <fileId>

global:
  -c, --config <configDir>         Application path, default: /Users/<user>/.gdrive
  --refresh-token <refreshToken>   Oauth refresh token used to get access token (for advanced users)
  --access-token <accessToken>     Oauth access token, only recommended for short-lived requests because of short lifetime (for advanced users)
```

#### Revoke permission
```
gdrive [global] share revoke <fileId> <permissionId>

global:
  -c, --config <configDir>         Application path, default: /Users/<user>/.gdrive
  --refresh-token <refreshToken>   Oauth refresh token used to get access token (for advanced users)
  --access-token <accessToken>     Oauth access token, only recommended for short-lived requests because of short lifetime (for advanced users)
```

#### Delete file or directory
```
gdrive [global] delete [options] <fileId>

global:
  -c, --config <configDir>         Application path, default: /Users/<user>/.gdrive
  --refresh-token <refreshToken>   Oauth refresh token used to get access token (for advanced users)
  --access-token <accessToken>     Oauth access token, only recommended for short-lived requests because of short lifetime (for advanced users)

options:
  -r, --recursive   Delete directory and all it's content
```

#### List all syncable directories on drive
```
gdrive [global] sync list [options]

global:
  -c, --config <configDir>         Application path, default: /Users/<user>/.gdrive
  --refresh-token <refreshToken>   Oauth refresh token used to get access token (for advanced users)
  --access-token <accessToken>     Oauth access token, only recommended for short-lived requests because of short lifetime (for advanced users)

options:
  --no-header   Dont print the header
```

#### List content of syncable directory
```
gdrive [global] sync content [options] <fileId>

global:
  -c, --config <configDir>         Application path, default: /Users/<user>/.gdrive
  --refresh-token <refreshToken>   Oauth refresh token used to get access token (for advanced users)
  --access-token <accessToken>     Oauth access token, only recommended for short-lived requests because of short lifetime (for advanced users)

options:
  --order <sortOrder>        Sort order. See https://godoc.org/google.golang.org/api/drive/v3#FilesListCall.OrderBy
  --path-width <pathWidth>   Width of path column, default: 60, minimum: 9, use 0 for full width
  --no-header                Dont print the header
  --bytes                    Size in bytes
```

#### Sync drive directory to local directory
```
gdrive [global] sync download [options] <fileId> <path>

global:
  -c, --config <configDir>         Application path, default: /Users/<user>/.gdrive
  --refresh-token <refreshToken>   Oauth refresh token used to get access token (for advanced users)
  --access-token <accessToken>     Oauth access token, only recommended for short-lived requests because of short lifetime (for advanced users)

options:
  --keep-remote         Keep remote file when a conflict is encountered
  --keep-local          Keep local file when a conflict is encountered
  --keep-largest        Keep largest file when a conflict is encountered
  --delete-extraneous   Delete extraneous local files
  --dry-run             Show what would have been transferred
  --no-progress         Hide progress
```

#### Sync local directory to drive
```
gdrive [global] sync upload [options] <path> <fileId>

global:
  -c, --config <configDir>         Application path, default: /Users/<user>/.gdrive
  --refresh-token <refreshToken>   Oauth refresh token used to get access token (for advanced users)
  --access-token <accessToken>     Oauth access token, only recommended for short-lived requests because of short lifetime (for advanced users)

options:
  --keep-remote             Keep remote file when a conflict is encountered
  --keep-local              Keep local file when a conflict is encountered
  --keep-largest            Keep largest file when a conflict is encountered
  --delete-extraneous       Delete extraneous remote files
  --dry-run                 Show what would have been transferred
  --no-progress             Hide progress
  --chunksize <chunksize>   Set chunk size in bytes, default: 8388608
```

#### List file changes
```
gdrive [global] changes [options]

global:
  -c, --config <configDir>         Application path, default: /Users/<user>/.gdrive
  --refresh-token <refreshToken>   Oauth refresh token used to get access token (for advanced users)
  --access-token <accessToken>     Oauth access token, only recommended for short-lived requests because of short lifetime (for advanced users)

options:
  -m, --max <maxChanges>     Max changes to list, default: 100
  --since <pageToken>        Page token to start listing changes from
  --now                      Get latest page token
  --name-width <nameWidth>   Width of name column, default: 40, minimum: 9, use 0 for full width
  --no-header                Dont print the header
```

#### List file revisions
```
gdrive [global] revision list [options] <fileId>

global:
  -c, --config <configDir>         Application path, default: /Users/<user>/.gdrive
  --refresh-token <refreshToken>   Oauth refresh token used to get access token (for advanced users)
  --access-token <accessToken>     Oauth access token, only recommended for short-lived requests because of short lifetime (for advanced users)

options:
  --name-width <nameWidth>   Width of name column, default: 40, minimum: 9, use 0 for full width
  --no-header                Dont print the header
  --bytes                    Size in bytes
```

#### Download revision
```
gdrive [global] revision download [options] <fileId> <revId>

global:
  -c, --config <configDir>         Application path, default: /Users/<user>/.gdrive
  --refresh-token <refreshToken>   Oauth refresh token used to get access token (for advanced users)
  --access-token <accessToken>     Oauth access token, only recommended for short-lived requests because of short lifetime (for advanced users)

options:
  -f, --force     Overwrite existing file
  --no-progress   Hide progress
  --stdout        Write file content to stdout
  --path <path>   Download path
```

#### Delete file revision
```
gdrive [global] revision delete <fileId> <revId>

global:
  -c, --config <configDir>         Application path, default: /Users/<user>/.gdrive
  --refresh-token <refreshToken>   Oauth refresh token used to get access token (for advanced users)
  --access-token <accessToken>     Oauth access token, only recommended for short-lived requests because of short lifetime (for advanced users)
```

#### Upload and convert file to a google document, see 'about import' for available conversions
```
gdrive [global] import [options] <path>

global:
  -c, --config <configDir>         Application path, default: /Users/<user>/.gdrive
  --refresh-token <refreshToken>   Oauth refresh token used to get access token (for advanced users)
  --access-token <accessToken>     Oauth access token, only recommended for short-lived requests because of short lifetime (for advanced users)

options:
  -p, --parent <parent>   Parent id, used to upload file to a specific directory, can be specified multiple times to give many parents
  --no-progress           Hide progress
```

#### Export a google document
```
gdrive [global] export [options] <fileId>

global:
  -c, --config <configDir>         Application path, default: /Users/<user>/.gdrive
  --refresh-token <refreshToken>   Oauth refresh token used to get access token (for advanced users)
  --access-token <accessToken>     Oauth access token, only recommended for short-lived requests because of short lifetime (for advanced users)

options:
  -f, --force     Overwrite existing file
  --mime <mime>   Mime type of exported file
  --print-mimes   Print available mime types for given file
```

#### Google drive metadata, quota usage
```
gdrive [global] about [options]

global:
  -c, --config <configDir>         Application path, default: /Users/<user>/.gdrive
  --refresh-token <refreshToken>   Oauth refresh token used to get access token (for advanced users)
  --access-token <accessToken>     Oauth access token, only recommended for short-lived requests because of short lifetime (for advanced users)

options:
  --bytes   Show size in bytes
```

#### Show supported import formats
```
gdrive [global] about import

global:
  -c, --config <configDir>         Application path, default: /Users/<user>/.gdrive
  --refresh-token <refreshToken>   Oauth refresh token used to get access token (for advanced users)
  --access-token <accessToken>     Oauth access token, only recommended for short-lived requests because of short lifetime (for advanced users)
```

#### Show supported export formats
```
gdrive [global] about export

global:
  -c, --config <configDir>         Application path, default: /Users/<user>/.gdrive
  --refresh-token <refreshToken>   Oauth refresh token used to get access token (for advanced users)
  --access-token <accessToken>     Oauth access token, only recommended for short-lived requests because of short lifetime (for advanced users)
```


## Examples
#### List files
```
$ gdrive list
Id                             Name                    Type   Size     Created
0B3X9GlR6EmbnZ3gyeGw4d3ozbUk   drive-windows-x64.exe   bin    6.6 MB   2015-07-18 16:43:58
0B3X9GlR6EmbnTXlSc1FqV1dvSTQ   drive-windows-386.exe   bin    5.2 MB   2015-07-18 16:43:53
0B3X9GlR6EmbnVjIzMDRqck1aekE   drive-osx-x64           bin    6.5 MB   2015-07-18 16:43:50
0B3X9GlR6EmbnbEpXdlhza25zT1U   drive-osx-386           bin    5.2 MB   2015-07-18 16:43:41
0B3X9GlR6Embnb095MGxEYmJhY2c   drive-linux-x64         bin    6.5 MB   2015-07-18 16:43:38
```

#### List largest files
```
$ gdrive list --query "name contains 'gdrive'" --order "quotaBytesUsed desc" -m 3
Id                             Name                     Type   Size     Created
0B3X9GlR6EmbnZXpDRG1xblM2LTg   gdrive-linux-mips64      bin    8.5 MB   2016-02-22 21:07:04
0B3X9GlR6EmbnNW5CTV8xdFkxTjg   gdrive-linux-mips64le    bin    8.5 MB   2016-02-22 21:07:07
0B3X9GlR6EmbnZ1NGS25FdEVlWEk   gdrive-osx-x64           bin    8.3 MB   2016-02-21 20:22:13
```
#### List file which import from other
```
# gdrive list -m 0 --query "" --name-width 0
Id                             Name                                                    Type   Size     Created
0B8uTQta6AZ6xVHJ1NXhEZXZZMFk   the-complete-piano-course update 26-12-2016.part4.rar   bin    4.0 GB   2016-02-26 00:51:22
0B8uTQta6AZ6xT3F2SVhNcHowZEE   the-complete-piano-course update 26-12-2016.part3.rar   bin    4.3 GB   2016-02-26 00:46:48
0B8uTQta6AZ6xX3NvWVVkT0g3ckU   the-complete-piano-course update 26-12-2016.part2.rar   bin    4.3 GB   2016-02-26 00:41:03
0B8uTQta6AZ6xdTN6cXI4XzNGdlk   the-complete-piano-course update 26-12-2016.part1.rar   bin    4.3 GB   2016-02-26 00:34:52
```


#### Upload file
```
$ gdrive upload gdrive-osx-x64
Uploading gdrive-osx-x64
Uploaded 0B3X9GlR6EmbnZ1NGS25FdEVlWEk at 3.8 MB/s, total 8.3 MB
```

#### Make directory
```
$ gdrive mkdir gdrive-bin
Directory 0B3X9GlR6EmbnY1RLVTk5VUtOVkk created
```

#### Upload file to directory
```
$ gdrive upload --parent 0B3X9GlR6EmbnY1RLVTk5VUtOVkk gdrive-osx-x64
Uploading gdrive-osx-x64
Uploaded 0B3X9GlR6EmbnNTk0SkV0bm5Hd0E at 2.5 MB/s, total 8.3 MB
```

#### Download file
```
$ gdrive download 0B3X9GlR6EmbnZ1NGS25FdEVlWEk
Downloading gdrive-osx-x64 -> gdrive-osx-x64
Downloaded 0B3X9GlR6EmbnZ1NGS25FdEVlWEk at 8.3 MB/s, total 8.3 MB
```

#### Share a file
```
$ gdrive share 0B3X9GlR6EmbnNTk0SkV0bm5Hd0E
Granted reader permission to anyone
```

#### Pipe content directly to google drive
```
$ echo "Hello World" | gdrive upload - hello.txt
Uploading hello.txt
Uploaded 0B3X9GlR6EmbnaXVrOUpIcWlUS0E at 8.0 B/s, total 12.0 B
```

#### Print file to stdout
```
$ gdrive download --stdout 0B3X9GlR6EmbnaXVrOUpIcWlUS0E
Hello World
```

#### Get file info
```
$ gdrive info 0B3X9GlR6EmbnNTk0SkV0bm5Hd0E
Id: 0B3X9GlR6EmbnNTk0SkV0bm5Hd0E
Name: gdrive-osx-x64
Path: gdrive-bin/gdrive-osx-x64
Mime: application/octet-stream
Size: 8.3 MB
Created: 2016-02-21 20:47:04
Modified: 2016-02-21 20:47:04
Md5sum: b607f29231a3b2d16098c4212516470f
Shared: True
Parents: 0B3X9GlR6EmbnY1RLVTk5VUtOVkk
ViewUrl: https://drive.google.com/file/d/0B3X9GlR6EmbnNTk0SkV0bm5Hd0E/view?usp=drivesdk
DownloadUrl: https://docs.google.com/uc?id=0B3X9GlR6EmbnNTk0SkV0bm5Hd0E&export=download
```

#### Update file (create new revision)
```
$ gdrive update 0B3X9GlR6EmbnNTk0SkV0bm5Hd0E gdrive-osx-x64
Uploading gdrive-osx-x64
Updated 0B3X9GlR6EmbnNTk0SkV0bm5Hd0E at 2.0 MB/s, total 8.3 MB
```

#### List file revisions
```
$ gdrive revision list 0B3X9GlR6EmbnNTk0SkV0bm5Hd0E
Id                                                    Name             Size     Modified              KeepForever
0B3X9GlR6EmbnOFlHSTZQNWJWMGN2ckZucC9VaEUwczV1cUNrPQ   gdrive-osx-x64   8.3 MB   2016-02-21 20:47:04   False
0B3X9GlR6EmbndVEwMlZCUldGWUlPb2lTS25rOFo1L2t6c2ZVPQ   gdrive-osx-x64   8.3 MB   2016-02-21 21:12:09   False
```

#### Download revision
```
$ gdrive revision download 0B3X9GlR6EmbnNTk0SkV0bm5Hd0E 0B3X9GlR6EmbnOFlHSTZQNWJWMGN2ckZucC9VaEUwczV1cUNrPQ
Downloading gdrive-osx-x64 -> gdrive-osx-x64
Download complete, rate: 8.3 MB/s, total size: 8.3 MB
```

#### Export google doc as docx
```
$ gdrive export --mime application/vnd.openxmlformats-officedocument.wordprocessingml.document 1Kt5A8X7X2RQrEi5t6Y9W1LayRc4hyrFiG63y2dIJEvk
Exported 'foo.docx' with mime type: 'application/vnd.openxmlformats-officedocument.wordprocessingml.document'
```

#### Import csv as google spreadsheet
```
$ gdrive import foo.csv
Imported 1mTl3DjIvap4tpTX_oMkDcbDT8ShtiGJRlozTfkXpeko with mime type: 'application/vnd.google-apps.spreadsheet'
```

#### Syncing directory to drive
```
# Create directory on drive
$ gdrive mkdir drive-bin
Directory 0B3X9GlR6EmbnOEd6cEh6bU9XZWM created

# Sync to drive
$ gdrive sync upload _release/bin 0B3X9GlR6EmbnOEd6cEh6bU9XZWM
Starting sync...
Collecting local and remote file information...
Found 32 local files and 0 remote files

6 remote directories are missing
[0001/0006] Creating directory drive-bin/bsd
[0002/0006] Creating directory drive-bin/linux
[0003/0006] Creating directory drive-bin/osx
[0004/0006] Creating directory drive-bin/plan9
[0005/0006] Creating directory drive-bin/solaris
[0006/0006] Creating directory drive-bin/windows

26 remote files are missing
[0001/0026] Uploading bsd/gdrive-dragonfly-x64 -> drive-bin/bsd/gdrive-dragonfly-x64
[0002/0026] Uploading bsd/gdrive-freebsd-386 -> drive-bin/bsd/gdrive-freebsd-386
[0003/0026] Uploading bsd/gdrive-freebsd-arm -> drive-bin/bsd/gdrive-freebsd-arm
[0004/0026] Uploading bsd/gdrive-freebsd-x64 -> drive-bin/bsd/gdrive-freebsd-x64
[0005/0026] Uploading bsd/gdrive-netbsd-386 -> drive-bin/bsd/gdrive-netbsd-386
[0006/0026] Uploading bsd/gdrive-netbsd-arm -> drive-bin/bsd/gdrive-netbsd-arm
[0007/0026] Uploading bsd/gdrive-netbsd-x64 -> drive-bin/bsd/gdrive-netbsd-x64
[0008/0026] Uploading bsd/gdrive-openbsd-386 -> drive-bin/bsd/gdrive-openbsd-386
[0009/0026] Uploading bsd/gdrive-openbsd-arm -> drive-bin/bsd/gdrive-openbsd-arm
[0010/0026] Uploading bsd/gdrive-openbsd-x64 -> drive-bin/bsd/gdrive-openbsd-x64
[0011/0026] Uploading linux/gdrive-linux-386 -> drive-bin/linux/gdrive-linux-386
[0012/0026] Uploading linux/gdrive-linux-arm -> drive-bin/linux/gdrive-linux-arm
[0013/0026] Uploading linux/gdrive-linux-arm64 -> drive-bin/linux/gdrive-linux-arm64
[0014/0026] Uploading linux/gdrive-linux-mips64 -> drive-bin/linux/gdrive-linux-mips64
[0015/0026] Uploading linux/gdrive-linux-mips64le -> drive-bin/linux/gdrive-linux-mips64le
[0016/0026] Uploading linux/gdrive-linux-ppc64 -> drive-bin/linux/gdrive-linux-ppc64
[0017/0026] Uploading linux/gdrive-linux-ppc64le -> drive-bin/linux/gdrive-linux-ppc64le
[0018/0026] Uploading linux/gdrive-linux-x64 -> drive-bin/linux/gdrive-linux-x64
[0019/0026] Uploading osx/gdrive-osx-386 -> drive-bin/osx/gdrive-osx-386
[0020/0026] Uploading osx/gdrive-osx-arm -> drive-bin/osx/gdrive-osx-arm
[0021/0026] Uploading osx/gdrive-osx-x64 -> drive-bin/osx/gdrive-osx-x64
[0022/0026] Uploading plan9/gdrive-plan9-386 -> drive-bin/plan9/gdrive-plan9-386
[0023/0026] Uploading plan9/gdrive-plan9-x64 -> drive-bin/plan9/gdrive-plan9-x64
[0024/0026] Uploading solaris/gdrive-solaris-x64 -> drive-bin/solaris/gdrive-solaris-x64
[0025/0026] Uploading windows/gdrive-windows-386.exe -> drive-bin/windows/gdrive-windows-386.exe
[0026/0026] Uploading windows/gdrive-windows-x64.exe -> drive-bin/windows/gdrive-windows-x64.exe
Sync finished in 1m18.891946279s

# Add new local file
$ echo "google drive binaries" > _release/bin/readme.txt

# Sync again
$ gdrive sync upload _release/bin 0B3X9GlR6EmbnOEd6cEh6bU9XZWM
Starting sync...
Collecting local and remote file information...
Found 33 local files and 32 remote files

1 remote files are missing
[0001/0001] Uploading readme.txt -> drive-bin/readme.txt
Sync finished in 2.201339535s

# Modify local file
$ echo "for all platforms" >> _release/bin/readme.txt

# Sync again
$ gdrive sync upload _release/bin 0B3X9GlR6EmbnOEd6cEh6bU9XZWM
Starting sync...
Collecting local and remote file information...
Found 33 local files and 33 remote files

1 local files has changed
[0001/0001] Updating readme.txt -> drive-bin/readme.txt
Sync finished in 1.890244258s
```

#### List content of sync directory
```
$ gdrive sync content 0B3X9GlR6EmbnOEd6cEh6bU9XZWM
Id                             Path                             Type   Size     Modified
0B3X9GlR6EmbnMldxMFV1UGVMTlE   bsd                              dir             2016-02-21 22:54:00
0B3X9GlR6EmbnM05sQ3hVUnJnOXc   bsd/gdrive-dragonfly-x64         bin    7.8 MB   2016-02-21 22:54:14
0B3X9GlR6EmbnVy1KXzA4dlU5RVE   bsd/gdrive-freebsd-386           bin    6.1 MB   2016-02-21 22:54:18
0B3X9GlR6Embnb29QQkFtSlRiZnc   bsd/gdrive-freebsd-arm           bin    6.1 MB   2016-02-21 22:54:20
0B3X9GlR6EmbnMkFQYVpSaHhHTXM   bsd/gdrive-freebsd-x64           bin    7.8 MB   2016-02-21 22:54:23
0B3X9GlR6EmbnVmJRMl9hUDloVU0   bsd/gdrive-netbsd-386            bin    6.1 MB   2016-02-21 22:54:25
0B3X9GlR6EmbnLVlTZWpxOEF4Q2s   bsd/gdrive-netbsd-arm            bin    6.1 MB   2016-02-21 22:54:28
0B3X9GlR6EmbnOENUZmh3anJmNG8   bsd/gdrive-netbsd-x64            bin    7.8 MB   2016-02-21 22:54:30
0B3X9GlR6EmbnWTRoQ2ZVQXRfQlU   bsd/gdrive-openbsd-386           bin    6.1 MB   2016-02-21 22:54:32
0B3X9GlR6EmbncEtlN3ZuQ0VUWms   bsd/gdrive-openbsd-arm           bin    6.1 MB   2016-02-21 22:54:35
0B3X9GlR6EmbnMlFLY1ptNEFyZWc   bsd/gdrive-openbsd-x64           bin    7.8 MB   2016-02-21 22:54:38
0B3X9GlR6EmbncGtSajQyNzloVEE   linux                            dir             2016-02-21 22:54:01
0B3X9GlR6EmbnMWVudkJmb1NZdmM   linux/gdrive-linux-386           bin    6.1 MB   2016-02-21 22:54:40
0B3X9GlR6Embnbnpla1R2VHV5T2M   linux/gdrive-linux-arm           bin    6.1 MB   2016-02-21 22:54:42
0B3X9GlR6EmbnM0s2cU1YWkNJSjA   linux/gdrive-linux-arm64         bin    7.7 MB   2016-02-21 22:54:45
0B3X9GlR6EmbnNU9NNi1TdDc4S2c   linux/gdrive-linux-mips64        bin    8.5 MB   2016-02-21 22:54:47
0B3X9GlR6EmbnSmdQNjRKZ2dWV1U   linux/gdrive-linux-mips64le      bin    8.5 MB   2016-02-21 22:54:50
0B3X9GlR6EmbnS0g0OVgxMHY5Z3c   linux/gdrive-linux-ppc64         bin    7.8 MB   2016-02-21 22:54:52
0B3X9GlR6EmbneVp6ZXRpR3FhWlU   linux/gdrive-linux-ppc64le       bin    7.8 MB   2016-02-21 22:54:54
0B3X9GlR6EmbnczdJT195dFVxdU0   linux/gdrive-linux-x64           bin    7.8 MB   2016-02-21 22:54:57
0B3X9GlR6EmbnTXZXeDRnSDdVS1E   osx                              dir             2016-02-21 22:54:02
0B3X9GlR6EmbnWnRheXJNR0pUMU0   osx/gdrive-osx-386               bin    6.6 MB   2016-02-21 22:54:59
0B3X9GlR6EmbnRzNqMWFXdDR1Rms   osx/gdrive-osx-arm               bin    6.6 MB   2016-02-21 22:55:01
0B3X9GlR6EmbnaDlVWTZDd0JIeEU   osx/gdrive-osx-x64               bin    8.3 MB   2016-02-21 22:55:04
0B3X9GlR6EmbnWW84UFBvbHlURXM   plan9                            dir             2016-02-21 22:54:02
0B3X9GlR6EmbnTmc0a2RNdDZDRUU   plan9/gdrive-plan9-386           bin    5.8 MB   2016-02-21 22:55:07
0B3X9GlR6EmbnT1pYZ2p4Sk9FVFk   plan9/gdrive-plan9-x64           bin    7.4 MB   2016-02-21 22:55:10
0B3X9GlR6EmbnbnZnXzlYVHoxdk0   readme.txt                       bin    40.0 B   2016-02-21 22:59:56
0B3X9GlR6EmbnSWF1QUlta3RnaGc   solaris                          dir             2016-02-21 22:54:03
0B3X9GlR6EmbnaWFOV0YxSGs5Znc   solaris/gdrive-solaris-x64       bin    7.7 MB   2016-02-21 22:55:13
0B3X9GlR6EmbnNE5ySkEzbWQ4Qms   windows                          dir             2016-02-21 22:54:03
0B3X9GlR6EmbnX1RIT2w1TWZYWFU   windows/gdrive-windows-386.exe   bin    6.1 MB   2016-02-21 22:55:15
0B3X9GlR6EmbndmVMU05POGRPS3c   windows/gdrive-windows-x64.exe   bin    7.8 MB   2016-02-21 22:55:18
```
