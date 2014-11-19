# le_rsyslog-cookbook

This cookbook should be used as a wrapper cookbook which will set up rsyslog to send logs to [logentries.com](https://logentries.com/).

## Supported Platforms

* debian
* ubuntu >= 12.04

## Attributes

<table>
  <tr>
    <th>Key</th>
    <th>Type</th>
    <th>Description</th>
    <th>Default</th>
  </tr>
  <tr>
    <td><tt>['le_rsyslog']['logentries']['token']</tt></td>
    <td>String</td>
    <td>logentries TCP token</td>
    <td><tt>None</tt></td>
  </tr>
  <tr>
    <td><tt>['le_rsyslog']['logentries']['logs']</tt></td>
    <td>Array of objects</td>
    <td>logname => absolute position of log to follow</td>
    <td><tt>None</tt></td>
  </tr>
</table>

## Usage

### le_rsyslog::default

Include `le_rsyslog` in your node's `run_list`:

```json
{
  "run_list": [
    "recipe[le_rsyslog::default]"
  ]
}
```

## License and Authors

Author:: Joe Heung (<joe@joeheung.com>)