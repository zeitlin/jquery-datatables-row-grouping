# Introduction #

JQuery Datatables RowGrouping add-in is a additional plugin for the [DataTables](http://www.datatables.net) plugin. It enables you to easily handle grouping operations on the client side. This plugin is extension of the examle placed on the [DataTables site](http://www.datatables.net/release-datatables/examples/advanced_init/row_grouping.html) with several additional options.

# Details #

RowGrouping plugin enchances datatables so you will need to apply this plugin on the table where datatables plugin is already applied. Example of the initialization code is:

```

$("#myTable").dataTable().rowGrouping();

```

This line of code group rows in the table by the first column. There are several stragegies that can be used for grouping (e.g. group by letters, year etc) - you can see details in the GroupingTypes page.

## Options ##
RowGrouping plugin can be customized if you pass various options to the initialization code. Example of the customization using a plugin parameters is shown in the following example:

```

$("#myTable").dataTable().rowGrouping({iGroupingColumnIndex:5});

```
Using this line of code, row grouping will not be done by the first column - column 5 will be used instead.
See more datails about plugin options on the [Options](Options.md) page

## Examples ##

There are lot of examples of row groung usage, You can either download them from the http://code.google.com/p/jquery-datatables-row-grouping/downloads/list or you can see following online examples:
  * Basic http://jquery-datatables-row-grouping.googlecode.com/svn/trunk/default.html
  * Grouping by letters http://jquery-datatables-row-grouping.googlecode.com/svn/trunk/letters.html
  * Grouping by the year column http://jquery-datatables-row-grouping.googlecode.com/svn/trunk/year.html
  * Collapsible/expandable grouping http://jquery-datatables-row-grouping.googlecode.com/svn/trunk/collapsibleGroups.html
  * Two level grouping http://jquery-datatables-row-grouping.googlecode.com/svn/trunk/twoLevelGrouping.html