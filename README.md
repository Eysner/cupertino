# Cupertino
**CLI for the Apple Dev Center**

Automate administrative tasks that you would normally have to do through the Apple Dev Center websites. Life's too short to manage device identifiers by hand!

This project is starting with the iOS Provisioning Portal, and may later expand to include iTunes Connect and/or Mac Developer Certificate Utility.

## Installation

```sh
$ gem install cupertino
```

## Usage

### Devices

```sh
$ ios devices:list

+---------------------------+------------------------------------------+
| Device Name               | Device Identifier                        |
+---------------------------+------------------------------------------+
| Johnny Appleseed iPad     | 0123456789012345678901234567890123abcdef |
| Johnny Appleseed iPhone   | abcdef0123456789012345678901234567890123 |
+---------------------------+------------------------------------------+

$ ios devices:add "iPad 1"=abc123
$ ios devices:add "iPad 2"=def456 "iPad 3"=ghi789 ...
```

### Provisioning Profiles

```sh
$ ios profiles:list

+----------------------------------+--------------+---------+
| Profile                          | App ID       | Status  |
+----------------------------------+--------------+---------+
| iOS Team Provisioning Profile: * | ABCDEFG123.* | Valid   |
+----------------------------------+--------------+---------+
```

### App IDs

```sh
$ ios app_ids:list

+-----------------------------+------------------------+-------------------+-------------------+
| Bundle Seed ID              | Description            | Development       | Distribution      |
+-----------------------------+------------------------+-------------------+-------------------+
| 123ABCDEFG.com.mattt.bundle | App Bundle Description | Passes            | Passes            |
|                             |                        | Data Protection   | Data Protection   |
|                             |                        | iCloud            | iCloud            |
|                             |                        | In-App Purchase   | In-App Purchase   |
|                             |                        | Game Center       | Game Center       |
|                             |                        | Push Notification | Push Notification |
+-----------------------------+------------------------+-------------------+-------------------+
```

### Certificates

```
$ ios certificates:list

+------------------+----------------------------------+-----------------+--------+
| Name             | Provisioning Profiles            | Expiration Date | Status |
+------------------+----------------------------------+-----------------+--------+
| Johnny Appleseed | iOS Team Provisioning Profile: * | Dec 23, 2012    | Issued |
+------------------+----------------------------------+-----------------+--------+
```

## Commands

_Crossed out commands are not yet implemented_

- `devices:add`
- `devices:list`
- ~~`devices:remove`~~

- `profiles:list`
- ~~`profiles:add`~~
- ~~`profiles:edit`~~

- `certificates:list [development|distribution]`
- ~~`certificates:add [development|distribution]`~~
- ~~`certificates:download CERTIFICATE_NAME`~~
- ~~`certificates:revoke CERTIFICATE_NAME`~~

- `app_ids:list`
- ~~`app_ids:new`~~

## Contact

Mattt Thompson

- http://github.com/mattt
- http://twitter.com/mattt
- m@mattt.me

## License

Cupertino is available under the MIT license. See the LICENSE file for more info.
