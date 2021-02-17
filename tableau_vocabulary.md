**Tableau Vocabulary**

**Version**: 2020.3

A collection of basic terminology used in **Tableau Desktop**. This is taken entirely from the [Tableau documentation](https://www.tableau.com/support/desktop) with some minor changes. This is **NOT** comprehensive, refer to the documentation for a comprehensive guide. This is for my personal use. So don't expect it to have full explanations and coherent paragraph structures. Sorry!

You need to know these terms, otherwise you will get confused by the jargon people use when explaining and discussing Tableau visualizations. Obviously, the more you use Tableau, the more comfortable you will become with the Tableau vocabulary, but it is important not to develop bad vocabulary. Even if you understand the underlying concept, using the wrong term to describe it is going to cause problems when you are explaining your work to others.


---

**The Tableau Workspace**

The Tableau workspace consists of menus, a toolbar, the Data pane, cards and shelves, and one or more sheets. Sheets can be worksheets, dashboards, or stories.

![](environ_workspace_area.png)

**A.** Workbook name. A workbook contains sheets. A sheet can be a worksheet, a dashboard, or a story.

**B.** Cards and shelves - Drag fields to the cards and shelves in the workspace to add data to your view.

**C.** Toolbar - Use the toolbar to access commands and analysis and navigation tools.

**D.** View - This is the canvas in the workspace where you create a visualization (also referred to as a *viz").

**E.** Click this icon to go to the Start page, where you can connect to data. 

**F.** Side Bar - In a worksheet, the side bar area contains the Data pane and the Analytics pane.

**G.** Click this tab to go to the Data Source page and view your data.

**H.** Status bar - Displays information about the current view.

**I.** Sheet tabs - Tabs represent each sheet in your workbook. This can include worksheets, dashboards, and stories.

---

**Workbook and Sheets**

Tableau uses a workbook and sheet file structure, much like Microsoft Excel. A workbook contains sheets. A sheet can be a worksheet, a dashboard, or a story.

- A **worksheet** contains a single view along with shelves, cards, legends, and the Data and Analytics panes in its side bar.

- A **dashboard** is a collection of views from multiple worksheets. The Dashboard and Layout panes are available in its side bar. 
- A **story** contains a sequence of worksheets or dashboards that work together to convey information. The Story and Layout panes are available in its side bar.

---

**Column and Rows shelves**

Drag fields from the Data pane to create the structure for your visualizations.

The **Columns** shelf creates the columns of a table, while the  **Rows** shelf creates the rows of a table. You can place any number of fields on these shelves.

When you place a dimension of the **Rows** or **Columns** shelves, headers for the members of that dimension are created. When you place a measure on the **Rows** or **Column** shelf, quantitative axes for that measure are created. As you add more fields to the view, additional headers and axes are included in the table and you get an increasingly detailed picture of your data.

In the view shown below, the members of the **Segment** dimension are displayed as column headers, while the **Profit** measure is displayed as a vertical axis.

![](wwd_shelf_cr1.png)

Tableau displays data using **marks**, where every mark corresponds to a row (or a group of rows) in your data source. The inner fields on the **Rows** and **Columns** shelves determine the default mark type. For example, if the inner fields are a measure and a dimension, the default mark type is a bar. You can manually select a different mark type using the Marks card drop-down menu.

Adding more fields to the **Rows** and **Column** shelves adds more rows, columns, and panes to the table.

![](wwd_shelf_cr2.png)

---

**Marks**

When you drag fields to the view, the data are displayed using marks. Each mark represents the intersection of all of the dimensions in the view.

For example, in a view with **Region** and **Year** dimensions, there is a mark for every combination of those two dimensions (East 2011, East 2012, West 2011, West 2012, etc.). In this case, the mark type is set to Text, so the **Abc** represents the location where the value for the text mark will appear—once a measure such as **Sales** is added to the view.

![](viewparts_marks1_9.2.png)


Marks can be displayed in many different ways including lines, shapes, bars, maps, and so on. You can show additional information about the data using mark properties such as color, size, shape, labels, etc. The type of mark you use and the mark properties are controlled by the Marks card. Drag fields to the Marks card to show more data. For example, the same view above is shown again below but this time with **Profit** on Color. With this additional information, it is clear that the West region had the highest profit in 2014.

![](viewparts_marks2_9.2.png)

**Marks card**

The Marks card is a key element for visual analysis in Tableau. As you drag fields to different properties in the Marks card, you add context and detail to the marks in the view.

You can use the Marks card to set the mark type, and to encode your data with color, size, shape, text, and detail. 

![](build_manual_shelves_marks1.png)

In this example, three different fields have been dragged to different properties in the Marks card. Segment is on Color, Region is on Shape, and Quantity is on Size.

---

**Filters shelf**

The Filters shelf allows you to specify which data to include and exclude. For example, you might want to analyze the profit for each customer segment, but only for certain shipping containers and delivery times. By placing fields on the Filters shelf, you can create such a view.

---

**Pages shelf**

The **Pages** shelf lets you break a view into a series of pages so you can better analyze how a specific field affects the rest of the data in a view. When you place a dimension on the **Pages** shelf you are adding a new row for each member in the dimension. When you place a measure on the **Pages** shelf, Tableau automatically converts the measure into a discrete measure.

The **Pages** shelf creates a set of pages, with a different view on each page. Each view is based on a member of the field you placed on the **Pages** shelf. You can easily flip through the views and compare them on a common axis, using the controls that get added to the view when you move a field to the **Pages** shelf. For example, the view below shows the **Profit** vs. **Sales** by **Region** for each day throughout the month. The image below shows days 1, 2, 3, and 4. You would have to scroll down to see other days in the month.

![](pages_shelf1.png)

---

A **view** is a visualization or viz that you create in Tableau. A viz might be a chart, a graph, a plot, or even a text table.

**Options for starting a view**

If you aren't sure where to place a field, you can let Tableau help you determine the best way to display the data.

- You can drag fields from the **Data** pane and drop them onto the cards and shelves that are part of every Tableau worksheet.

- You can double-click one or more fields in the **Data** pane.

- You can select one or more fields in the **Data** pane and then choose a chart type from **Show me**, which identifies the chart types that are appropriate for the fields you selected.

- You can drop a field on the **Drop field here** grid to start creating a view from a tabular perspective.

**The View area**

Data views are displayed in a table on every worksheet. A table is a collection of rows and column, and consists of the following components: Headers, Axes, Panes, Cells, and Marks. In addition to these, you can choose to show or hide Titles, Captions, Field Labels, and Legends.

![](view_parts3.png)

**A.** Field Labels - The label of a discrete field added to the row or column shelf that describes the members of that field. For example, Category is a discrete field that contains three members; Furniture, Office Supplies and Technology.

**B.** Titles - The name that you give your worksheet, dashboard, or story. Titles display automatically for worksheets and stories and you can turn them on to display them in your dashboards.

**C.** Marks - The data that represents the intersection of the fields (dimensions and measures) included in your view. Marks can be represented using lines, bars, shapes, maps and so on.

**D.** Legends - A key that describes how the data is encoded in your view. For example if you use shapes or colors in your view, the legend describes what each shape or color represents.

**E.** Axes - Created when you add a measure (fields that contain quantitative, numerical information) to the view. By default, Tableau generates a continuous axis for this data.

**F.** Headers - The member name of a field.

**G.** Captions - Text that describes the data in the view. Captions can be automatically generated and can be toggled on and off.


**Cells**

Cells are the basic components of any table you can create in Tableau, defined by the intersection of a row and a column. For example, in a text table, a cell is where the text is displayed, as shown in the view below:

![](cells1.png)


**Panes**

A pane is defined by the intersection of fields on the rows and columns shelves.

In a table calculation, this is seen as one or more cells that belong to the same field, which are computed down or across according to the calculation, as in the example below:

![](table_calculations5.png)


---

**Data Pane**

In the worksheet, the columns from your data source are shown as fields on the left side in the **Data** pane. The **Data** pane contains a variety of fields organized by table. For each table or folder in a data source, dimension fields appear above the gray line and measure fields appear below the gray line. Dimension fields typically hold categorical data such as product types and dates, while measure fields hold numeric data such as sales and profit. In some cases, a table or folder might contain only dimensions, or only measures to start with. 


The Data pane includes:
    
- **Dimension fields**

- **Measure fields**

- **Calculated fields** - If your underlying data doesn't include all of the fields you need to answer your questions, you can create new fields in Tableau using calculations and then save them as part of your data source. These fields are called calculated fields.

- **Sets** Subsets of data that you define. Sets are custom fields based on existing dimensions and criteria that you specify.

- **Parameters** Values that can be used as placeholders in formulas, or replace constant values in calculated fields and filters.

**Analytics Pane**

Drag reference lines, box plots, trend lines forecasts, and other items into your view from the **Analytics** pane, which appears on the left side of the workspace. Toggle between the **Data** pane and the **Analytics** pane by clicking the tabs at the top of the side bar.

![](environ_analytics_pane.png)

---

**Data Source Page**

Before or during your analysis, you may want to make changes to the Tableau data source. You can do that on the data source page. Tableau takes you to the data source page after you establish the initial connection to your data. You can also access the data source by clicking the **Data Source** tab from any location in the workbook.

The look of the page and the options available vary depending on the type of data that you are connected to, the data source page generally consists of four main areas: left pane, canvas, data grid, and metadata grid.

![](environ_workspace_datasource_page.png)

**A.** Left Pane - Displays the connected data source and other details about your data

**B.** Canvas: logical player - The canvas opens with the logical layer, where you can create relationships between logical tables

**C.** Canvas: physical layer - Double-click a table in the logical layer to go to the physical layer of the canvas, where you can add joins and unions between tables.

**D.** Data grid - Displays first $1,000$ rows of the data contained in the Tableau data source.

**E.** Metadata grid- Displays the field in your data source as rows.

---

**Tableau Concepts**

A **row**, or record, can be anything from information around a transaction at a retail store, to weather measurements at a specific location, or stats about a social media post.

It is important to know what a record (row) in the data represents. This is the **granularity** of the data.

Here, each record is a day | Here, each record is a month
:-------------------------:|:----------------------------:
![](data_structure_granularity_day.png)  |  ![](data_structure_granularity_month.png)

A best practice is to have a **unique identifier (UID)**, a value that identifies each row as a unique piece of data. In Superstore, that would be Row ID. Not all data sets have a UID.

A **column** of data in table comes into Tableau Desktop as a **field** in the data pane, but they are essentially interchangeable terms (We use the term **column** in Tableau desktop for use in the columns and rows shelf and to describe certain visualizations.) A field of data should contain items that can be grouped into a larger relationship. The items themselves are called **values** or **members** (only discrete dimensions contain members).

What values are allowed in a given field are determined by the *domain* of the field (see note below). For example, a column for *grocery store departments* might contain the members *deli*, *bakery*, *produce*, etc., but it wouldn't include *bread* or *salami* because those are items, not departments. Phrased another way, the domain of the department field is limited to just the possible grocery store departments.

Additionally, a well-structured data set would have a column for *Sales* and a column for *Profit*, not a single column for *Money*, because profit is a separate concept from sales.

- The domain of the Sales field would be values ≥ 0, since sales cannot be negative.

- The domain of the Profit field, however, would be all values, since profit can be negative.

> **Note:** *Domain* can also mean the values present in the data. If the column *grocery store department* erroneously contained *salami*, by this definition, that value would be in the domain of the column. The definitions are slightly contradictory. One is the values that could or should be there, the other is values that actually are there.

---

**Aggregation and Granularity**

A concept related to what makes a row is the idea of aggregation and granulality, which are opposites ends of a spectrum.

**Aggregation**

- refers to how multiple data values are brought together into a single value, such as counting all the Google searches for Pumpkin spice or taking the average of all the temperatures readings around Seatle on a given day.

- By default, measures in Tableau are always are aggregated. The default aggregation is SUM. You can change the aggregation to options like Average, Median, Count Distinct, Minimum, etc.

**Granularity**

- refers to how detailed the data is. What does a row or record in the data set represent? A person with malaria? A provinces' total cases of malaria for the month? That's the granularity.

- Knowing the granularity of the data is crucial to working with level of detail (LOD) expressions.

---

**Categorizing fields**

Each **column** in the data table comes in Tableau Desktop as a **field**, which appears in the **Data** pane. Fields in Tableau Desktop must be either a dimension or measure (separated by a line within tables in the **Data** pane) and either discrete or continuous (color coded: blue fields are discrete and green fields are continuous).

- **Dimensions**  are qualitative, meaning they can't be measured but are instead described. Dimensions are often things like city or country, eye color, category, team name, etc. Dimensions are usually discrete.

- **Measures** are quantitative, meaning they can be measured and recorded with numbers. Measures can be things like sales, height, clicks, etc. In Tableau Desktop, measures are automatically aggregated; the default aggregation is SUM. Measures are usually continuous.

- **Discrete** means individually separate or distinct. Toyata is distinct from Mazda. In Tableau Desktop, discrete values come into the view as a label and they create panes.

- **Continuous** means forming an unbroken, continuous whole. In Tableau Desktop, continuous values come into the view as an axis.

- Dimensions are usually discrete, and measures are usually continuous. However, this is not always the case. Dates can be either discrete or continuous.

 - Dates are dimensions and automatically come into the view as discrete (aka date parts, such as *August*, which considers the month of August without considering other information like the year). A trend line applied to a timeline with discrete dates will be broken into multiple trend lines, one per pane.

 - We can chose to use continuous dates if preferred (aka date truncations, such as *August 2017*, which is different than *August 2018*). A trend line applied to a timeline with continuous dates will have a single trend line for the entire date axis.
 
 ---

**Data type icons in Tableau**



- Text (string) values  ![](symbol_text.png)    
- Date values           ![](symbol_date.png)      
- Date and Time values  ![](symbol_datetime.png) 
- Numerical values      ![](symbol_number.png)    
- Boolean values (relational only)   ![](symbol_bool.png)    
- Geographic values (used with maps) ![](geoicon.png)      
-  Cluster Group         ![](symbol_cluster.png)  

---

**Blue versus green fields**

Tableau represents data differently in the view depending on whether  the field is **discrete** (blue), or **continuous** (green). 

- Green measures and dimensions are continuous. Continuous field values are treated as an infinite range. Generally, continuous fields add axes to the view.


- Blue measures and dimensions  are discrete. Discrete values are treated as finite. Generally, discrete fields add headers to the view.

People sometimes call these fields **pills**.

**Examples of continuous and discrete fields used in a view** 

In the example on the left (below), because the **Quantity** field is set to **Continuous**, it creates a horizontal axis along the bottom of the view. The green background and the axis help you to see that it's a continuous field.

In the example on the right, the **Quantity** field has been set to **Discrete**. It creates horizontal headers instead of an axis. The blue background and the horizontal headers help you to see that it's discrete.

![](cont_disct_1.png)

In both examples, the **Sales** field is set to **Continuous**. It creates a vertical axis because it continuous and it's been added to the Rows shelf. If it was on the Columns shelf, it would create a horizontal axis. The green background and aggregation function (in this case, SUM) help to indicate that it's a measure.

The absence of an aggregation function in the **Quantity** field name help to indicate that it's a dimension.

---

**Logical and Physical layer**

(needs to be completed)


```python

```
