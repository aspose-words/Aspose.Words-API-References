---
title: MailMerge.ExecuteWithRegions
linktitle: ExecuteWithRegions
articleTitle: ExecuteWithRegions
second_title: Aspose.Words for .NET
description: MailMerge ExecuteWithRegions method. Performs a mail merge from a custom data source with mail merge regions in C#.
type: docs
weight: 200
url: /net/aspose.words.mailmerging/mailmerge/executewithregions/
---
## ExecuteWithRegions(*[IMailMergeDataSource](../../imailmergedatasource/)*) {#executewithregions}

Performs a mail merge from a custom data source with mail merge regions.

```csharp
public void ExecuteWithRegions(IMailMergeDataSource dataSource)
```

| Parameter | Type | Description |
| --- | --- | --- |
| dataSource | IMailMergeDataSource | An object that implements the custom mail merge data source interface. |

## Remarks

Use this method to fill mail merge fields in the document with values from any custom data source such as an XML file or collections of business objects. You need to write your own class that implements the [`IMailMergeDataSource`](../../imailmergedatasource/) interface.

You can use this method only when [`IsBidiTextSupportedOnUpdate`](../../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/) is `false`, that is you do not need Right-To-Left language (such as Arabic or Hebrew) compatibility.

## Examples

Shows how to use mail merge regions to execute a nested mail merge.

```csharp
public void CustomDataSource()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Normally, MERGEFIELDs contain the name of a column of a mail merge data source.
    // Instead, we can use "TableStart:" and "TableEnd:" prefixes to begin/end a mail merge region.
    // Each region will belong to a table with a name that matches the string immediately after the prefix's colon.
    builder.InsertField(" MERGEFIELD TableStart:Customers");

    // These MERGEFIELDs are inside the mail merge region of the "Customers" table.
    // When we execute the mail merge, this field will receive data from rows in a data source named "Customers".
    builder.Write("Full name:\t");
    builder.InsertField(" MERGEFIELD FullName ");
    builder.Write("\nAddress:\t");
    builder.InsertField(" MERGEFIELD Address ");
    builder.Write("\nOrders:\n");

    // Create a second mail merge region inside the outer region for a data source named "Orders".
    // The "Orders" data entries have a many-to-one relationship with the "Customers" data source.
    builder.InsertField(" MERGEFIELD TableStart:Orders");

    builder.Write("\tItem name:\t");
    builder.InsertField(" MERGEFIELD Name ");
    builder.Write("\n\tQuantity:\t");
    builder.InsertField(" MERGEFIELD Quantity ");
    builder.InsertParagraph();

    builder.InsertField(" MERGEFIELD TableEnd:Orders");
    builder.InsertField(" MERGEFIELD TableEnd:Customers");

    // Create related data with names that match those of our mail merge regions.
    CustomerList customers = new CustomerList();
    customers.Add(new Customer("Thomas Hardy", "120 Hanover Sq., London"));
    customers.Add(new Customer("Paolo Accorti", "Via Monte Bianco 34, Torino"));

    customers[0].Orders.Add(new Order("Rugby World Cup Cap", 2));
    customers[0].Orders.Add(new Order("Rugby World Cup Ball", 1));
    customers[1].Orders.Add(new Order("Rugby World Cup Guide", 1));

    // To mail merge from your data source, we must wrap it into an object that implements the IMailMergeDataSource interface.
    CustomerMailMergeDataSource customersDataSource = new CustomerMailMergeDataSource(customers);

    doc.MailMerge.ExecuteWithRegions(customersDataSource);

    doc.Save(ArtifactsDir + "NestedMailMergeCustom.CustomDataSource.docx");
}

/// <summary>
/// An example of a "data entity" class in your application.
/// </summary>
public class Customer
{
    public Customer(string aFullName, string anAddress)
    {
        FullName = aFullName;
        Address = anAddress;
        Orders = new List<Order>();
    }

    public string FullName { get; set; }
    public string Address { get; set; }
    public List<Order> Orders { get; set; }
}

/// <summary>
/// An example of a typed collection that contains your "data" objects.
/// </summary>
public class CustomerList : ArrayList
{
    public new Customer this[int index]
    {
        get { return (Customer) base[index]; }
        set { base[index] = value; }
    }
}

/// <summary>
/// An example of a child "data entity" class in your application.
/// </summary>
public class Order
{
    public Order(string oName, int oQuantity)
    {
        Name = oName;
        Quantity = oQuantity;
    }

    public string Name { get; set; }
    public int Quantity { get; set; }
}

/// <summary>
/// A custom mail merge data source that you implement to allow Aspose.Words 
/// to mail merge data from your Customer objects into Microsoft Word documents.
/// </summary>
public class CustomerMailMergeDataSource : IMailMergeDataSource
{
    public CustomerMailMergeDataSource(CustomerList customers)
    {
        mCustomers = customers;

        // When we initialize the data source, its position must be before the first record.
        mRecordIndex = -1;
    }

    /// <summary>
    /// The name of the data source. Used by Aspose.Words only when executing mail merge with repeatable regions.
    /// </summary>
    public string TableName
    {
        get { return "Customers"; }
    }

    /// <summary>
    /// Aspose.Words calls this method to get a value for every data field.
    /// </summary>
    public bool GetValue(string fieldName, out object fieldValue)
    {
        switch (fieldName)
        {
            case "FullName":
                fieldValue = mCustomers[mRecordIndex].FullName;
                return true;
            case "Address":
                fieldValue = mCustomers[mRecordIndex].Address;
                return true;
            case "Order":
                fieldValue = mCustomers[mRecordIndex].Orders;
                return true;
            default:
                // Return "false" to the Aspose.Words mail merge engine to signify
                // that we could not find a field with this name.
                fieldValue = null;
                return false;
        }
    }

    /// <summary>
    /// A standard implementation for moving to a next record in a collection.
    /// </summary>
    public bool MoveNext()
    {
        if (!IsEof)
            mRecordIndex++;

        return !IsEof;
    }

    public IMailMergeDataSource GetChildDataSource(string tableName)
    {
        switch (tableName)
        {
            // Get the child data source, whose name matches the mail merge region that uses its columns.
            case "Orders":
                return new OrderMailMergeDataSource(mCustomers[mRecordIndex].Orders);
            default:
                return null;
        }
    }

    private bool IsEof
    {
        get { return (mRecordIndex >= mCustomers.Count); }
    }

    private readonly CustomerList mCustomers;
    private int mRecordIndex;
}

public class OrderMailMergeDataSource : IMailMergeDataSource
{
    public OrderMailMergeDataSource(List<Order> orders)
    {
        mOrders = orders;

        // When we initialize the data source, its position must be before the first record.
        mRecordIndex = -1;
    }

    /// <summary>
    /// The name of the data source. Used by Aspose.Words only when executing mail merge with repeatable regions.
    /// </summary>
    public string TableName
    {
        get { return "Orders"; }
    }

    /// <summary>
    /// Aspose.Words calls this method to get a value for every data field.
    /// </summary>
    public bool GetValue(string fieldName, out object fieldValue)
    {
        switch (fieldName)
        {
            case "Name":
                fieldValue = mOrders[mRecordIndex].Name;
                return true;
            case "Quantity":
                fieldValue = mOrders[mRecordIndex].Quantity;
                return true;
            default:
                // Return "false" to the Aspose.Words mail merge engine to signify
                // that we could not find a field with this name.
                fieldValue = null;
                return false;
        }
    }

    /// <summary>
    /// A standard implementation for moving to a next record in a collection.
    /// </summary>
    public bool MoveNext()
    {
        if (!IsEof)
            mRecordIndex++;

        return !IsEof;
    }

    /// <summary>
    /// Return null because we do not have any child elements for this sort of object.
    /// </summary>
    public IMailMergeDataSource GetChildDataSource(string tableName)
    {
        return null;
    }

    private bool IsEof
    {
        get { return (mRecordIndex >= mOrders.Count); }
    }

    private readonly List<Order> mOrders;
    private int mRecordIndex;
}
```

### See Also

* interface [IMailMergeDataSource](../../imailmergedatasource/)
* class [MailMerge](../)
* namespace [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* assembly [Aspose.Words](../../../)

---

## ExecuteWithRegions(*[IMailMergeDataSourceRoot](../../imailmergedatasourceroot/)*) {#executewithregions_1}

Performs a mail merge from a custom data source with mail merge regions.

```csharp
public void ExecuteWithRegions(IMailMergeDataSourceRoot dataSourceRoot)
```

| Parameter | Type | Description |
| --- | --- | --- |
| dataSourceRoot | IMailMergeDataSourceRoot | An object that implements the custom mail merge data source root interface. |

## Remarks

Use this method to fill mail merge fields in the document with values from any custom data source such as an XML file or collections of business objects. You need to write your own classes that implement the [`IMailMergeDataSourceRoot`](../../imailmergedatasourceroot/) and [`IMailMergeDataSource`](../../imailmergedatasource/) interfaces.

You can use this method only when [`IsBidiTextSupportedOnUpdate`](../../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/) is `false`, that is you do not need Right-To-Left language (such as Arabic or Hebrew) compatibility.

## Examples

Performs mail merge from a custom data source with master-detail data.

```csharp
public void CustomDataSourceRoot()
{
    // Create a document with two mail merge regions named "Washington" and "Seattle".
    string[] mailMergeRegions = { "Vancouver", "Seattle" };
    Document doc = CreateSourceDocumentWithMailMergeRegions(mailMergeRegions);

    // Create two data sources for the mail merge.
    EmployeeList employeesWashingtonBranch = new EmployeeList();
    employeesWashingtonBranch.Add(new Employee("John Doe", "Sales"));
    employeesWashingtonBranch.Add(new Employee("Jane Doe", "Management"));

    EmployeeList employeesSeattleBranch = new EmployeeList();
    employeesSeattleBranch.Add(new Employee("John Cardholder", "Management"));
    employeesSeattleBranch.Add(new Employee("Joe Bloggs", "Sales"));

    // Register our data sources by name in a data source root.
    //  If we are about to use this data source root in a mail merge with regions,
    // each source's registered name must match the name of an existing mail merge region in the mail merge source document.
    DataSourceRoot sourceRoot = new DataSourceRoot();
    sourceRoot.RegisterSource(mailMergeRegions[0], new EmployeeListMailMergeSource(employeesWashingtonBranch));
    sourceRoot.RegisterSource(mailMergeRegions[1], new EmployeeListMailMergeSource(employeesSeattleBranch));

    // Since we have consecutive mail merge regions, we would normally have to perform two mail merges.
    // However, one mail merge source with a data root can fill in multiple regions
    // if the root contains tables with corresponding names/column names.
    doc.MailMerge.ExecuteWithRegions(sourceRoot);

    doc.Save(ArtifactsDir + "MailMergeCustom.CustomDataSourceRoot.docx");
}

/// <summary>
/// Create a document that contains consecutive mail merge regions, with names designated by the input array,
/// for a data table of employees.
/// </summary>
private static Document CreateSourceDocumentWithMailMergeRegions(string[] regions)
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    foreach (string s in regions)
    {
        builder.Writeln("\n" + s + " branch: ");
        builder.InsertField(" MERGEFIELD TableStart:" + s);
        builder.InsertField(" MERGEFIELD FullName");
        builder.Write(", ");
        builder.InsertField(" MERGEFIELD Department");
        builder.InsertField(" MERGEFIELD TableEnd:" + s);
    }

    return doc;
}

/// <summary>
/// An example of a "data entity" class in your application.
/// </summary>
private class Employee
{
    public Employee(string aFullName, string aDepartment)
    {
        FullName = aFullName;
        Department = aDepartment;
    }

    public string FullName { get; }
    public string Department { get; }
}

/// <summary>
/// An example of a typed collection that contains your "data" objects.
/// </summary>
private class EmployeeList : ArrayList
{
    public new Employee this[int index]
    {
        get { return (Employee)base[index]; }
        set { base[index] = value; }
    }
}

/// <summary>
/// Data source root that can be passed directly into a mail merge which can register and contain many child data sources.
/// These sources must all implement IMailMergeDataSource, and are registered and differentiated by a name
/// which corresponds to a mail merge region that will read the respective data.
/// </summary>
private class DataSourceRoot : IMailMergeDataSourceRoot
{
    public IMailMergeDataSource GetDataSource(string tableName)
    {
        EmployeeListMailMergeSource source = mSources[tableName];
        source.Reset();
        return mSources[tableName];
    }

    public void RegisterSource(string sourceName, EmployeeListMailMergeSource source)
    {
        mSources.Add(sourceName, source);
    }

    private readonly Dictionary<string, EmployeeListMailMergeSource> mSources = new Dictionary<string, EmployeeListMailMergeSource>();
}

/// <summary>
/// Custom mail merge data source.
/// </summary>
private class EmployeeListMailMergeSource : IMailMergeDataSource
{
    public EmployeeListMailMergeSource(EmployeeList employees)
    {
        mEmployees = employees;
        mRecordIndex = -1;
    }

    /// <summary>
    /// A standard implementation for moving to a next record in a collection.
    /// </summary>
    public bool MoveNext()
    {
        if (!IsEof)
            mRecordIndex++;

        return !IsEof;
    }

    private bool IsEof
    {
        get { return (mRecordIndex >= mEmployees.Count); }
    }

    public void Reset()
    {
        mRecordIndex = -1;
    }

    /// <summary>
    /// The name of the data source. Used by Aspose.Words only when executing mail merge with repeatable regions.
    /// </summary>
    public string TableName
    {
        get { return "Employees"; }
    }

    /// <summary>
    /// Aspose.Words calls this method to get a value for every data field.
    /// </summary>
    public bool GetValue(string fieldName, out object fieldValue)
    {
        switch (fieldName)
        {
            case "FullName":
                fieldValue = mEmployees[mRecordIndex].FullName;
                return true;
            case "Department":
                fieldValue = mEmployees[mRecordIndex].Department;
                return true;
            default:
                // Return "false" to the Aspose.Words mail merge engine to signify
                // that we could not find a field with this name.
                fieldValue = null;
                return false;
        }
    }

    /// <summary>
    /// Child data sources are for nested mail merges.
    /// </summary>
    public IMailMergeDataSource GetChildDataSource(string tableName)
    {
        throw new System.NotImplementedException();
    }

    private readonly EmployeeList mEmployees;
    private int mRecordIndex;
}
```

### See Also

* interface [IMailMergeDataSourceRoot](../../imailmergedatasourceroot/)
* class [MailMerge](../)
* namespace [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* assembly [Aspose.Words](../../../)

---

## ExecuteWithRegions(*DataSet*) {#executewithregions_2}

Performs mail merge from a **DataSet** into a document with mail merge regions.

```csharp
public void ExecuteWithRegions(DataSet dataSet)
```

| Parameter | Type | Description |
| --- | --- | --- |
| dataSet | DataSet | **DataSet** that contains data to be inserted into mail merge fields. |

## Remarks

Use this method to perform mail merge from one or more tables into repeatable mail merge regions in the document. The mail merge regions inside the document will dynamically grow to accommodate records in the corresponding tables.

Every table in the **DataSet** must have a name.

The document must have mail merge regions defined with names that refer to the tables in the **DataSet**.

To specify a mail merge region in the document you need to insert two mail merge fields to mark beginning and end of the mail merge region.

All document content that is included inside a mail merge region will be automatically repeated for every record in the **DataTable**.

To mark beginning of a mail merge region insert a MERGEFIELD with name TableStart:MyTable, where MyTable corresponds to one of the table names in your **DataSet**.

To mark the end of the mail merge region insert another MERGEFIELD with name TableEnd:MyTable.

To insert a MERGEFIELD in Word use Insert/Field command and select MergeField then type the name of the field.

The **TableStart** and **TableEnd** fields must be inside the same section in your document.

If used inside a table, **TableStart** and **TableEnd** must be inside the same row in the table.

Mail merge regions in a document should be well formed (there always needs to be a pair of matching **TableStart** and **TableEnd** merge fields with the same table name).

## Examples

Shows how to execute a nested mail merge with two merge regions and two data tables.

```csharp
public void ExecuteWithRegionsNested()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Normally, MERGEFIELDs contain the name of a column of a mail merge data source.
    // Instead, we can use "TableStart:" and "TableEnd:" prefixes to begin/end a mail merge region.
    // Each region will belong to a table with a name that matches the string immediately after the prefix's colon.
    builder.InsertField(" MERGEFIELD TableStart:Customers");

    // This MERGEFIELD is inside the mail merge region of the "Customers" table.
    // When we execute the mail merge, this field will receive data from rows in a data source named "Customers".
    builder.Write("Orders for ");
    builder.InsertField(" MERGEFIELD CustomerName");
    builder.Write(":");

    // Create column headers for a table that will contain values from a second inner region.
    builder.StartTable();
    builder.InsertCell();
    builder.Write("Item");
    builder.InsertCell();
    builder.Write("Quantity");
    builder.EndRow();

    // Create a second mail merge region inside the outer region for a table named "Orders".
    // The "Orders" table has a many-to-one relationship with the "Customers" table on the "CustomerID" column.
    builder.InsertCell();
    builder.InsertField(" MERGEFIELD TableStart:Orders");
    builder.InsertField(" MERGEFIELD ItemName");
    builder.InsertCell();
    builder.InsertField(" MERGEFIELD Quantity");

    // End the inner region, and then end the outer region. The opening and closing of a mail merge region must
    // happen on the same row of a table.
    builder.InsertField(" MERGEFIELD TableEnd:Orders");
    builder.EndTable();

    builder.InsertField(" MERGEFIELD TableEnd:Customers");

    // Create a dataset that contains the two tables with the required names and relationships.
    // Each merge document for each row of the "Customers" table of the outer merge region will perform its mail merge on the "Orders" table.
    // Each merge document will display all rows of the latter table whose "CustomerID" column values match the current "Customers" table row.
    DataSet customersAndOrders = CreateDataSet();
    doc.MailMerge.ExecuteWithRegions(customersAndOrders);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteWithRegionsNested.docx");
}

/// <summary>
/// Generates a data set that has two data tables named "Customers" and "Orders", with a one-to-many relationship on the "CustomerID" column.
/// </summary>
private static DataSet CreateDataSet()
{
    DataTable tableCustomers = new DataTable("Customers");
    tableCustomers.Columns.Add("CustomerID");
    tableCustomers.Columns.Add("CustomerName");
    tableCustomers.Rows.Add(new object[] { 1, "John Doe" });
    tableCustomers.Rows.Add(new object[] { 2, "Jane Doe" });

    DataTable tableOrders = new DataTable("Orders");
    tableOrders.Columns.Add("CustomerID");
    tableOrders.Columns.Add("ItemName");
    tableOrders.Columns.Add("Quantity");
    tableOrders.Rows.Add(new object[] { 1, "Hawaiian", 2 });
    tableOrders.Rows.Add(new object[] { 2, "Pepperoni", 1 });
    tableOrders.Rows.Add(new object[] { 2, "Chicago", 1 });

    DataSet dataSet = new DataSet();
    dataSet.Tables.Add(tableCustomers);
    dataSet.Tables.Add(tableOrders);
    dataSet.Relations.Add(tableCustomers.Columns["CustomerID"], tableOrders.Columns["CustomerID"]);

    return dataSet;
}
```

### See Also

* class [MailMerge](../)
* namespace [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* assembly [Aspose.Words](../../../)

---

## ExecuteWithRegions(*DataTable*) {#executewithregions_3}

Performs mail merge from a **DataTable** into the document with mail merge regions.

```csharp
public void ExecuteWithRegions(DataTable dataTable)
```

| Parameter | Type | Description |
| --- | --- | --- |
| dataTable | DataTable | Data source for the mail merge operation. The table must have its TableName property set. |

## Remarks

The document must have a mail merge region defined with name that matches TableName.

If there are other mail merge regions defined in the document they are left intact. This allows to perform several mail merge operations.

## Examples

Demonstrates how to format cells during a mail merge.

```csharp
public void AlternatingRows()
{
    Document doc = new Document(MyDir + "Mail merge destination - Northwind suppliers.docx");

    doc.MailMerge.FieldMergingCallback = new HandleMergeFieldAlternatingRows();

    DataTable dataTable = GetSuppliersDataTable();
    doc.MailMerge.ExecuteWithRegions(dataTable);

    doc.Save(ArtifactsDir + "MailMergeEvent.AlternatingRows.docx");
}

/// <summary>
/// Formats table rows as a mail merge takes place to alternate between two colors on odd/even rows.
/// </summary>
private class HandleMergeFieldAlternatingRows : IFieldMergingCallback
{
    /// <summary>
    /// Called when a mail merge merges data into a MERGEFIELD.
    /// </summary>
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        if (mBuilder == null)
            mBuilder = new DocumentBuilder(args.Document);

        // This is true of we are on the first column, which means we have moved to a new row.
        if (args.FieldName == "CompanyName")
        {
            Color rowColor = IsOdd(mRowIdx) ? Color.FromArgb(213, 227, 235) : Color.FromArgb(242, 242, 242);

            for (int colIdx = 0; colIdx < 4; colIdx++)
            {
                mBuilder.MoveToCell(0, mRowIdx, colIdx, 0);
                mBuilder.CellFormat.Shading.BackgroundPatternColor = rowColor;
            }

            mRowIdx++;
        }
    }

    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs args)
    {
        // Do nothing.
    }

    private DocumentBuilder mBuilder;
    private int mRowIdx;
}

/// <summary>
/// Function needed for Visual Basic autoporting that returns the parity of the passed number.
/// </summary>
private static bool IsOdd(int value)
{
    return (value / 2 * 2).Equals(value);
}

/// <summary>
/// Creates a mail merge data source.
/// </summary>
private static DataTable GetSuppliersDataTable()
{
    DataTable dataTable = new DataTable("Suppliers");
    dataTable.Columns.Add("CompanyName");
    dataTable.Columns.Add("ContactName");
    for (int i = 0; i < 10; i++)
    {
        DataRow datarow = dataTable.NewRow();
        dataTable.Rows.Add(datarow);
        datarow[0] = "Company " + i;
        datarow[1] = "Contact " + i;
    }

    return dataTable;
}
```

Shows how to use regions to execute two separate mail merges in one document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// If we want to perform two consecutive mail merges on one document while taking data from two tables
// related to each other in any way, we can separate the mail merges with regions.
// Normally, MERGEFIELDs contain the name of a column of a mail merge data source.
// Instead, we can use "TableStart:" and "TableEnd:" prefixes to begin/end a mail merge region.
// Each region will belong to a table with a name that matches the string immediately after the prefix's colon.
// These regions are separate for unrelated data, while they can be nested for hierarchical data.
builder.Writeln("\tCities: ");
builder.InsertField(" MERGEFIELD TableStart:Cities");
builder.InsertField(" MERGEFIELD Name");
builder.InsertField(" MERGEFIELD TableEnd:Cities");
builder.InsertParagraph();

// Both MERGEFIELDs refer to the same column name, but values for each will come from different data tables.
builder.Writeln("\tFruit: ");
builder.InsertField(" MERGEFIELD TableStart:Fruit");
builder.InsertField(" MERGEFIELD Name");
builder.InsertField(" MERGEFIELD TableEnd:Fruit");

// Create two unrelated data tables.
DataTable tableCities = new DataTable("Cities");
tableCities.Columns.Add("Name");
tableCities.Rows.Add(new object[] { "Washington" });
tableCities.Rows.Add(new object[] { "London" });
tableCities.Rows.Add(new object[] { "New York" });

DataTable tableFruit = new DataTable("Fruit");
tableFruit.Columns.Add("Name");
tableFruit.Rows.Add(new object[] { "Cherry" });
tableFruit.Rows.Add(new object[] { "Apple" });
tableFruit.Rows.Add(new object[] { "Watermelon" });
tableFruit.Rows.Add(new object[] { "Banana" });

// We will need to run one mail merge per table. The first mail merge will populate the MERGEFIELDs
// in the "Cities" range while leaving the fields the "Fruit" range unfilled.
doc.MailMerge.ExecuteWithRegions(tableCities);

// Run a second merge for the "Fruit" table, while using a data view
// to sort the rows in ascending order on the "Name" column before the merge.
DataView dv = new DataView(tableFruit);
dv.Sort = "Name ASC";
doc.MailMerge.ExecuteWithRegions(dv);

doc.Save(ArtifactsDir + "MailMerge.ExecuteWithRegionsConcurrent.docx");
```

### See Also

* class [MailMerge](../)
* namespace [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* assembly [Aspose.Words](../../../)

---

## ExecuteWithRegions(*DataView*) {#executewithregions_4}

Performs mail merge from a **DataView** into the document with mail merge regions.

```csharp
public void ExecuteWithRegions(DataView dataView)
```

| Parameter | Type | Description |
| --- | --- | --- |
| dataView | DataView | Data source for the mail merge operation. The source table of the **DataView** must have its **TableName** property set. |

## Remarks

This method is useful if you retrieve data into a **DataTable** but then need to apply a filter or sort before the mail merge.

The document must have a mail merge region defined with name that matches **DataView.Table.TableName**.

If there are other mail merge regions defined in the document they are left intact. This allows to perform several mail merge operations.

## Examples

Shows how to use regions to execute two separate mail merges in one document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// If we want to perform two consecutive mail merges on one document while taking data from two tables
// related to each other in any way, we can separate the mail merges with regions.
// Normally, MERGEFIELDs contain the name of a column of a mail merge data source.
// Instead, we can use "TableStart:" and "TableEnd:" prefixes to begin/end a mail merge region.
// Each region will belong to a table with a name that matches the string immediately after the prefix's colon.
// These regions are separate for unrelated data, while they can be nested for hierarchical data.
builder.Writeln("\tCities: ");
builder.InsertField(" MERGEFIELD TableStart:Cities");
builder.InsertField(" MERGEFIELD Name");
builder.InsertField(" MERGEFIELD TableEnd:Cities");
builder.InsertParagraph();

// Both MERGEFIELDs refer to the same column name, but values for each will come from different data tables.
builder.Writeln("\tFruit: ");
builder.InsertField(" MERGEFIELD TableStart:Fruit");
builder.InsertField(" MERGEFIELD Name");
builder.InsertField(" MERGEFIELD TableEnd:Fruit");

// Create two unrelated data tables.
DataTable tableCities = new DataTable("Cities");
tableCities.Columns.Add("Name");
tableCities.Rows.Add(new object[] { "Washington" });
tableCities.Rows.Add(new object[] { "London" });
tableCities.Rows.Add(new object[] { "New York" });

DataTable tableFruit = new DataTable("Fruit");
tableFruit.Columns.Add("Name");
tableFruit.Rows.Add(new object[] { "Cherry" });
tableFruit.Rows.Add(new object[] { "Apple" });
tableFruit.Rows.Add(new object[] { "Watermelon" });
tableFruit.Rows.Add(new object[] { "Banana" });

// We will need to run one mail merge per table. The first mail merge will populate the MERGEFIELDs
// in the "Cities" range while leaving the fields the "Fruit" range unfilled.
doc.MailMerge.ExecuteWithRegions(tableCities);

// Run a second merge for the "Fruit" table, while using a data view
// to sort the rows in ascending order on the "Name" column before the merge.
DataView dv = new DataView(tableFruit);
dv.Sort = "Name ASC";
doc.MailMerge.ExecuteWithRegions(dv);

doc.Save(ArtifactsDir + "MailMerge.ExecuteWithRegionsConcurrent.docx");
```

### See Also

* class [MailMerge](../)
* namespace [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* assembly [Aspose.Words](../../../)

---

## ExecuteWithRegions(*IDataReader, string*) {#executewithregions_5}

Performs mail merge from **IDataReader** into the document with mail merge regions.

```csharp
public void ExecuteWithRegions(IDataReader dataReader, string tableName)
```

| Parameter | Type | Description |
| --- | --- | --- |
| dataReader | IDataReader | Source of the data records for mail merge such as **OleDbDataReader** or **SqlDataReader**. |
| tableName | String | Name of the mail merge region in the document to populate. |

## Remarks

You can pass **SqlDataReader** or **OleDbDataReader** object into this method as a parameter because they both implemented **IDataReader** interface.

## Examples

Shows how to insert images stored in a database BLOB field into a report.

```csharp
public void ImageFromBlob()
{
    Document doc = new Document(MyDir + "Mail merge destination - Northwind employees.docx");

    doc.MailMerge.FieldMergingCallback = new HandleMergeImageFieldFromBlob();

    string connString = $"Provider=Microsoft.ACE.OLEDB.12.0;Data Source={DatabaseDir + "Northwind.accdb"};";
    string query = "SELECT FirstName, LastName, Title, Address, City, Region, Country, PhotoBLOB FROM Employees";

    using (OleDbConnection conn = new OleDbConnection(connString))
    {
        conn.Open();

        // Open the data reader, which needs to be in a mode that reads all records at once.
        OleDbCommand cmd = new OleDbCommand(query, conn);
        IDataReader dataReader = cmd.ExecuteReader();

        doc.MailMerge.ExecuteWithRegions(dataReader, "Employees");
    }

    doc.Save(ArtifactsDir + "MailMergeEvent.ImageFromBlob.docx");
}

private class HandleMergeImageFieldFromBlob : IFieldMergingCallback
{
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        // Do nothing.
    }

    /// <summary>
    /// This is called when a mail merge encounters a MERGEFIELD in the document with an "Image:" tag in its name.
    /// </summary>
    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs e)
    {
        MemoryStream imageStream = new MemoryStream((byte[])e.FieldValue);
        e.ImageStream = imageStream;
    }
}
```

### See Also

* class [MailMerge](../)
* namespace [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* assembly [Aspose.Words](../../../)
