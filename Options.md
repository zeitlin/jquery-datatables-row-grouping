[Overview](Overview.md) Options

# Introduction #

In this page you can find various options that can be applied to the plugin.

## Setting options in the plugin ##

Plugin can be customized when you pass options to the rowGrouping initialization call. Example is shown below:

```
$("#example").dataTable().rowGrouping({ 
		GroupingColumnIndex:5, 	
		sGroupBy: "year",
		bHideGroupingColumn: false
});
```

In this example rows are grouped by the column 5, where in the rows is placed year data, and column is not hidden.

## Available options ##

In the table below you can find list of available initialization options.

| Option | Type | Description | Default |
|:-------|:-----|:------------|:--------|
|iGroupingColumnIndex |Integer|             Index of the column that will be used for grouping | 0       |
|sGroupingColumnSortDirection |Enumeration|         Sort direction of the group |         |
|iGroupingOrderByColumnIndex |Integer|Index of the column that will be used for ordering groups. If not set iGroupingColumnIndex will be used| 0       |
|sGrupingClass |String|              CSS class that will be associated to the group row| "group" |
|bSetGroupingClassOnTR                                |Boolean|             If it is set to true class will be set to the TR instead of the TD within the grouping TR|false    |
|bHideGroupingColumn                                  |Boolean|             Hide column used for grouping once results are grouped. |true     |
|bHideGroupingOrderByColumn                           |Boolean|             Hide column used for ordering groups once results are grouped. | true    |
|sGroupBy                                             |Enumeration|         Type of grouping that should be applied. Values "name"(default), "letter", "year"|"name"   |
|sGroupLabelPrefix                                    |String|              Prefix that will be added to each group cell|         |
|bExpandableGrouping                                  |Boolean|             Attach expand/collapse handlers to the grouping rows |false    |
|bExpandSingleGroup                                   |Boolean|             Use accordon grouping|false    |
|iExpandGroupOffset                                   |Integer|             Number of pixels to set scroll position above the currently selected group. If -1 scroll will be alligned to the table|100      |
|sDateFormat                                           |String|              Date format used for year grouping. | "dd/MM/yyyy" |
|sEmptyGroupLabel                                     |String|              Label that will be placed as group if grouping cells are empty. |"-"      |
|iGroupingColumnIndex2                                |Integer|             Index of the secondary column that will be used for grouping | 0       |
|sGroupingColumnSortDirection2                        |Enumeration|         Sort direction of the secondary group |         |
|iGroupingOrderByColumnIndex2                         |Integer|             Index of the column that will be used for ordering secondary groups |-1       |
|sGrupingClass2    |String|              Class that will be associated to the secondary group row. | "subgroup" |
|bHideGroupingColumn2                                 |Boolean|             Hide column used for secondary grouping once results are grouped. |true     |
|bHideGroupingOrderByColumn2                          |Boolean|             Hide column used for ordering secondary groups once results are grouped. |true     |
|sGroupBy2                                            |Enumeration|         Type of grouping that should be applied to secondary column. Values "name"(default), "letter", "year"|"name"   |
|sGroupLabelPrefix2                                   |String|              Prefix that will be added to each secondary group cell |         |
|fnOnGrouped                                          |Function|            Function that is called when grouping is finished. Function has no parameters. |         |