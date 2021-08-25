# How to perform Excel like filtering in the WinUI DataGrid (SfDataGrid)?

## About the sample
This example illustrates how to perform Excel like filtering in the [WinUI DataGrid](https://www.syncfusion.com/winui-controls/datagrid) (SfDataGrid)?

[WinUI DataGrid](https://www.syncfusion.com/winui-controls/datagrid) (SfDataGrid) provides excel like filtering UI and also advanced filter UI to filter the data easily. UI filtering can be enabled by setting [SfDataGrid.AllowFiltering](https://help.syncfusion.com/cr/winui/Syncfusion.UI.Xaml.DataGrid.SfDataGrid.html#Syncfusion_UI_Xaml_DataGrid_SfDataGrid_AllowFiltering) property to true , where you can open filter UI by clicking the Filter icon in column header and filter the records.

```XML

<syncfusion:SfDataGrid x:Name="dataGrid"    
                       AutoGenerateColumns="False"
                       AllowFiltering="True"
                       ColumnWidthMode="Star"
                       AllowEditing="True"
                       ItemsSource="{Binding ProductInfo}">

```

You can enable/disable filtering for particular column by setting [GridColumn.AllowFiltering](https://help.syncfusion.com/cr/winui/Syncfusion.UI.Xaml.DataGrid.GridColumn.html#Syncfusion_UI_Xaml_DataGrid_GridColumn_AllowFiltering) property.

```XML

<syncfusion:GridTextColumn    HeaderText="Product" 
                              MappingName="Product"  
                              AllowFiltering="True"  />

```
#### Note:
```    
       1.	GridColumn.AllowFiltering has higher priority than SfDataGrid.AllowFiltering property.      
```

![Shows the filter applied in SfDataGrid](ExcelLikeFilter.gif)

## Built-in UI Views

DataGrid filter UI comprises of two different UIs.
        
•	**Checkbox Filter UI** - Provides excel like filter interface with list of check box’s.        
•	**Advanced Filter UI** - Provides advanced filter options to filter the data.

By default, both Checkbox Filter and Advanced Filter are loaded while opening the filter pop-up. You can switch between AdvancedFilter and CheckboxFilter by using AdvancedFilter button in the UI View.

![Displays the two UI views in SfDataGrid](ExcelFilterUIView.png)

## Checkbox Filter UI

In [CheckBoxFilterControl](https://help.syncfusion.com/cr/winui/Syncfusion.UI.Xaml.DataGrid.CheckboxFilterControl.html) a list with checkboxes in show [FilterElement](https://help.syncfusion.com/cr/winui/Syncfusion.UI.Xaml.Grids.FilterElement.html), you may need to filter out all data which the checkboxes are checked or filter out all data which the checkboxes are unchecked.

The following are the control parts of **Checkbox Filtering.**

![Control parts of Checkbox Filtering](CheckBoxFilterControl.png)

![CheckBoxFilter applied in SfDataGrid](CheckBoxFiltering.gif)

## Advanced Filter UI

Advanced filter UI provides multiple filter options to filter the data easily. Filter menu options are loaded based on Advanced filter type by automatically detecting the underlying date type.

Below are the built-in filter types supported.

•	**Text Filters** – Loads various menu options to filter the display text effectively.

•	**Number Filters** – Loads various menu options to filter the numeric data.

•	**Date Filters** – Loads various menu options and [DatePicker](https://docs.microsoft.com/en-us/windows/winui/api/microsoft.ui.xaml.controls.datepicker?view=winui-3.0) to filter DateTime type column.

|   Text Filters       	|   Number Filters  | Date Filters        |
| ----------------------|:-----------------:|---------------------|
| When the string value is bounded to the [GridColumn](https://help.syncfusion.com/cr/winui/Syncfusion.UI.Xaml.DataGrid.GridColumn.html) or the items source is [dynamic](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/reference-types) ,then **Text Filters** are loaded in [AdvancedFilterControl](https://help.syncfusion.com/cr/winui/Syncfusion.UI.Xaml.DataGrid.AdvancedFilterControl.html).|  When integer, double, short, decimal, byte or long are bound to the [GridColumn](https://help.syncfusion.com/cr/winui/Syncfusion.UI.Xaml.DataGrid.GridColumn.html) then **Number Filters** are loaded in [AdvancedFilterControl](https://help.syncfusion.com/cr/winui/Syncfusion.UI.Xaml.DataGrid.AdvancedFilterControl.html). | When the DateTime type value is bound to the [GridColumn](https://help.syncfusion.com/cr/winui/Syncfusion.UI.Xaml.DataGrid.GridColumn.html) , then **Date Filters** are loaded in [AdvancedFilterControl](https://help.syncfusion.com/cr/winui/Syncfusion.UI.Xaml.DataGrid.AdvancedFilterControl.html). |
|  ![Displays text filter](TextFilter.png) |  ![Displays number filter](NumberFilter.png) |  ![Displays date filter](DateFilter.png) |
|  **Filter menu options** <br> 1.	Equals <br>2.	Does Not Equal <br>3.	Begins With <br>4.	Does Not Begin With <br>5.	Ends With <br>6.	Does Not End With <br>7.	Contains <br>8.	Does Not Contain <br>9.	Empty <br>10.	Not Empty <br>11.	Null <br>12.	Not Null <br> |  **Filter menu options** <br>1. Equals <br>2. Does Not Equal <br>3. Null <br>4. Not Null <br>5. Less Than <br>6. Less Than or Equal <br>7. Greater Than <br>8. Greater Than or Equal  | **Filter menu options**   <br> 1. Equals <br> 2.	Does Not Equal <br> 3.	Before <br> 4.	Before Or Equal <br> 5.	After <br> 6.	After Or Equal <br> 7.	Null <br> 8.	Not Null |

#### Note:
``` 
      1.	Null and Not Null options are available only when AllowBlankFilters is set to True.
      2.	If the column is GridUnboundColumn, then Text Filters will be loaded.
```
![AdvancedFiltering applied in SfDataGrid](AdvancedFiltering.gif)

Take a moment to peruse the [WinUI DataGrid - Filtering](https://help.syncfusion.com/winui/datagrid/filtering) documentation, where you can find about filtering with code examples.

## Requirements to run the demo
Visual Studio 2015 and above versions
