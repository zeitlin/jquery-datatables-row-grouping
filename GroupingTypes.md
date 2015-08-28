[Overview](Overview.md) Grouping types
# Introduction #

RowGrouping plugin enables you to apply different kinds of grouping strategies such as
  * Grouping by name
  * Grouping by letter
  * Grouping by year

## Grouping by name ##

Default behaviour of to plugin is grouping by names. Plugin will take value of the cell that should be used for grouping in the first row and create summary heading row for the group with the value of the same cell.
If next row has the same value in the grouoing cell it will be added to the group, otherwise if the grouping value is different a new heading summary row will be injected as it is shown in the following example.
|Grouping cell|Data1|Data2|Data3|
|:------------|:----|:----|:----|
|**A**        |
|A            | a   | b   | c   |
|A            | d   | e   | f   |
|A            | h   | i   | j   |
|**B**        |
|B            | a   | b   | c   |
|B            | h   | i   | j   |
|B            | d   | e   | f   |
|**C**        |
|C            | a   | b   | c   |
|C            | d   | e   | f   |

As you can see before the first row is injected summary row A and second and third row are just included in the table. Fourth row sa grouping value in the cell "B" so new grouping row will be injected. The last grouping row is added before the first row with grouping value "C". See live example on the http://jquery-datatables-row-grouping.googlecode.com/svn/trunk/default.html .

## Grouping by letter ##

You can perform grouping by the first letter of the grouping cell if ou set 'sGroupBy' parameter to the value "letter" as it is shown in the following example:

```
$("#example").dataTable().rowGrouping({
 					sGroupBy: "letter"
});

```
Grouping metod is identical to the one explained in the previous section. However, in this case values in the grouping cells are not compared directly  - only their first leters are compared when new grouping row is added. You can see live example on the http://jquery-datatables-row-grouping.googlecode.com/svn/trunk/letters.html .

## Grouping by letter ##

You can perform grouping by the year value of the date colum if ou set 'sGroupBy' parameter to the value "year" as it is shown in the following example:

```
$("#example").dataTable().rowGrouping({
 					sGroupBy: "year",
 					sDateFormat: "dd/MM/yyyy"
});

```
Grouping metod is identical to the onse explained in the previous section. However, in this case values in the grouping cells are extracted from the year part of the date column. In this case all values in the grouping column should have dd/MM/yyyy format (default one) but you can chnage formatin in the 'sDateFormat'. You can see live example on the http://jquery-datatables-row-grouping.googlecode.com/svn/trunk/year.html .

## Grouping custimization ##
You can make additional customization of grouping plugin such as:
  * If grouping column is not the first one you can specify what column should be used instead if yu set 'iGroupingColumnIndex' parameter
  * Once grouping is done you can either hide or leave grouping column if you set 'bHideGroupingColumn' parameter
  * If groupng cells do not have value you can set that labe will be placed in the suppary headint row (e.g. "N/A").Parameter'sEmptyGroupLabel' is used for this setting.
  * By default groups are ordered ascending if they are grouped by name or letter od descending if you group them by year. You can add custom ordering if you add additional column that will contain ordering indexes for all grouping values and set 'iGroupingOrderByColumnIndex' to the vale of this column - see http://jquery-datatables-row-grouping.googlecode.com/svn/trunk/customGroupOrdering.html