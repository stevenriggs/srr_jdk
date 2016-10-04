srr_jdk Cookbook
==================
Installs the JDK from a .gz file

Requirements
------------
Linux only:  Tested on CentOS 6.5 and RHEL 6.5

A JDK install .gz file available by URL.


Attributes
----------
#### srr_jdk::default
<table>
  <tr>
    <th>Key</th>
    <th>Type</th>
    <th>Description</th>
    <th>Default</th>
  </tr>
  <tr>
    <td><tt>['srr_jdk']['downloadurlroot']</tt></td>
    <td>String</td>
    <td>URL location of the .gz installer file</td>
    <td><tt>"http://download.oracle.com/otn/java/jdk/7u71-b14/"</tt></td>
  </tr>
  <tr>
    <td><tt>['srr_jdk']['installfile']</tt></td>
    <td>String</td>
    <td>Name of the .gz installer file</td>
    <td><tt>"jdk-7u67-linux-x64.gz"</tt></td>
  </tr>
  <tr>
    <td><tt>['srr_jdk']['javafoldername']</tt></td>
    <td>String</td>
    <td>Name of the installation folder name. May be different than the .gz filename.</td>
    <td><tt>"jdk1.7.0_67"</tt></td>
  </tr>
  <tr>
    <td><tt>['srr_jdk']['installroot']</tt></td>
    <td>String</td>
    <td>The root folder to install java</td>
    <td><tt>"/usr/java"</tt></td>
  </tr>
</table>

Usage
-----
#### srr_jdk::default

## Use a wrapper cookbook ##
In your metadata.rb: add the line 'depends srr_jdk'
In your recipes/default.rb: add the line 'include_recipe srr_jdk'
In your attributes/default.rb: Override any attributes you like.

Or just include `srr_jdk` in your node's `run_list`:

```json
{
  "name":"my_node",
  "run_list": [
    "recipe[srr_jdk]"
  ]
}
```


License and Authors
-------------------
Authors: Steven Riggs
