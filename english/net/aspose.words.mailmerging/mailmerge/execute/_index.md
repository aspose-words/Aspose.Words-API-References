---
title: Execute
second_title: Aspose.Words for .NET API Reference
description: 
type: docs
weight: 180
url: /net/aspose.words.mailmerging/mailmerge/execute/
---
## MailMerge.Execute method (1 of 6)

Performs a mail merge from a custom data source.

```csharp
public void Execute(IMailMergeDataSource dataSource)
```

| Parameter | Type | Description |
| --- | --- | --- |
| dataSource | IMailMergeDataSource | An object that implements the custom mail merge data source interface. |

## Remarks

Use this method to fill mail merge fields in the document with values from any data source such as a list or hashtable or objects. You need to write your own class that implements the [`IMailMergeDataSource`](../../imailmergedatasource) interface.

You can use this method only when [`IsBidiTextSupportedOnUpdate`](../../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate) is false, that is you do not need Right-To-Left language (such as Arabic or Hebrew) compatibility.

This method ignores the RemoveUnusedRegions option.

### See Also

* interface [IMailMergeDataSource](../../imailmergedatasource)
* class [MailMerge](../../mailmerge)
* namespace [Aspose.Words.MailMerging](../../mailmerge)
* assembly [Aspose.Words](../../../)

---

## MailMerge.Execute method (2 of 6)

Performs a mail merge operation for a single record.

```csharp
public void Execute(string[] fieldNames, object[] values)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fieldNames | String[] | Array of merge field names. Field names are not case sensitive. If a field name that is not found in the document is encountered, it is ignored. |
| values | Object[] | Array of values to be inserted into the merge fields. Number of elements in this array must be the same as the number of elements in fieldNames. |

## Remarks

Use this method to fill mail merge fields in the document with values from an array of objects.

This method merges data for one record only. The array of field names and the array of values represent the data of a single record.

This method does not use mail merge regions.

This method ignores the RemoveUnusedRegions option.

## Examples

Shows how to merge an image from a URI as mail merge data into a MERGEFIELD.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// MERGEFIELDs with "Image:" tags will receive an image during a mail merge.
// The string after the colon in the "Image:" tag corresponds to a column name
// in the data source whose cells contain URIs of image files.
builder.InsertField("MERGEFIELD  Image:logo_FromWeb ");
builder.InsertField("MERGEFIELD  Image:logo_FromFileSystem ");

// Create a data source that contains URIs of images that we will merge. 
// A URI can be a web URL that points to an image, or a local file system filename of an image file.
string[] columns = { "logo_FromWeb", "logo_FromFileSystem" };
object[] URIs = { ImageUrl, ImageDir + "Logo.jpg" };

// Execute a mail merge on a data source with one row.
doc.MailMerge.Execute(columns, URIs);

doc.Save(ArtifactsDir + "MailMergeEvent.ImageFromUrl.docx");
```

Shows how to perform a mail merge, and then save the document to the client browser.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" MERGEFIELD FullName ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD Company ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD Address ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD City ");

doc.MailMerge.Execute(new string[] { "FullName", "Company", "Address", "City" },
    new object[] { "James Bond", "MI5 Headquarters", "Milbank", "London" });

// Send the document to the client browser.
Assert.That(() => doc.Save(response, "Artifacts/MailMerge.ExecuteArray.docx", ContentDisposition.Inline, null),
    Throws.TypeOf<ArgumentNullException>()); //Thrown because HttpResponse is null in the test.

// We will need to close this response manually to ensure that we do not add any superfluous content to the document after saving.
Assert.That(() => response.End(), Throws.TypeOf<NullReferenceException>());
```

### See Also

* class [MailMerge](../../mailmerge)
* namespace [Aspose.Words.MailMerging](../../mailmerge)
* assembly [Aspose.Words](../../../)

---

## MailMerge.Execute method (3 of 6)

Performs mail merge from a DataTable into the document.

```csharp
public void Execute(DataTable table)
```

| Parameter | Type | Description |
| --- | --- | --- |
| table | DataTable | Table that contains data to be inserted into mail merge fields. Field names are not case sensitive. If a field name that is not found in the document is encountered, it is ignored. |

## Remarks

Use this method to fill mail merge fields in the document with values from a **DataTable**.

All records from the table are merged into the document.

You can use NEXT field in the Word document to cause **MailMerge** object to select next record from the **DataTable** and continue merging. This can be used when creating documents such as mailing labels.

When **MailMerge** object reaches end of the main document and there are still more rows in the **DataTable**, it copies entire content of the main document and appends it to the end of the destination document using a section break as a separator.

This method ignores the RemoveUnusedRegions option.

## Examples

Shows how to execute a mail merge with data from a DataTable.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // Below are two ways of using a DataTable as the data source for a mail merge.
    // 1 -  Use the entire table for the mail merge to create one output mail merge document for every row in the table:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 -  Use one row of the table to create one output mail merge document:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// Creates a mail merge source document.
/// </summary>
private static Document CreateSourceDocExecuteDataTable()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(" MERGEFIELD CustomerName ");
    builder.InsertParagraph();
    builder.InsertField(" MERGEFIELD Address ");

    return doc;
}
```

### See Also

* class [MailMerge](../../mailmerge)
* namespace [Aspose.Words.MailMerging](../../mailmerge)
* assembly [Aspose.Words](../../../)

---

## MailMerge.Execute method (4 of 6)

Performs mail merge from IDataReader into the document.

```csharp
public void Execute(IDataReader dataReader)
```

| Parameter | Type | Description |
| --- | --- | --- |
| dataReader | IDataReader | Data source for the mail merge operation. |

## Remarks

You can pass **SqlDataReader** or **OleDbDataReader** object into this method as a parameter because they both implemented **IDataReader** interface.

Note this method does not use mail merge regions and for multiple records the document will grow by repeating the whole document.

This method ignores the RemoveUnusedRegions option.

## Examples

Shows how to run a mail merge using data from a data reader.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Product:\t");
builder.InsertField(" MERGEFIELD ProductName");
builder.Write("\nSupplier:\t");
builder.InsertField(" MERGEFIELD CompanyName");
builder.Writeln();
builder.InsertField(" MERGEFIELD QuantityPerUnit");
builder.Write(" for $");
builder.InsertField(" MERGEFIELD UnitPrice");

// Create a connection string that points to the "Northwind" database file
// in our local file system, open a connection, and set up an SQL query.
string connectionString = @"Driver={Microsoft Access Driver (*.mdb)};Dbq=" + DatabaseDir + "Northwind.mdb";
string query = 
    @"SELECT Products.ProductName, Suppliers.CompanyName, Products.QuantityPerUnit, {fn ROUND(Products.UnitPrice,2)} as UnitPrice
    FROM Products 
    INNER JOIN Suppliers 
    ON Products.SupplierID = Suppliers.SupplierID";

using (OdbcConnection connection = new OdbcConnection())
{
    connection.ConnectionString = connectionString;
    connection.Open();

    // Create an SQL command that will source data for our mail merge.
    // The names of the table's columns that this SELECT statement will return
    // will need to correspond to the merge fields we placed above.
    OdbcCommand command = connection.CreateCommand();
    command.CommandText = query;

    // This will run the command and store the data in the reader.
    OdbcDataReader reader = command.ExecuteReader(CommandBehavior.CloseConnection);

    // Take the data from the reader and use it in the mail merge.
    doc.MailMerge.Execute(reader);
}

doc.Save(ArtifactsDir + "MailMerge.ExecuteDataReader.docx");
```

### See Also

* class [MailMerge](../../mailmerge)
* namespace [Aspose.Words.MailMerging](../../mailmerge)
* assembly [Aspose.Words](../../../)

---

## MailMerge.Execute method (5 of 6)

Performs mail merge from a DataView into the document.

```csharp
public void Execute(DataView dataView)
```

| Parameter | Type | Description |
| --- | --- | --- |
| dataView | DataView | Data source for the mail merge operation. |

## Remarks

This method is useful if you retrieve data into a **DataTable** but then need to apply a filter or sort before the mail merge.

Note this method does not use mail merge regions and for multiple records the document will grow by repeating the whole document.

This method ignores the RemoveUnusedRegions option.

## Examples

Shows how to edit mail merge data with a DataView.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Congratulations ");
builder.InsertField(" MERGEFIELD Name");
builder.Write(" for passing with a grade of ");
builder.InsertField(" MERGEFIELD Grade");

// Create a data table that our mail merge will source data from.
DataTable table = new DataTable("ExamResults");
table.Columns.Add("Name");
table.Columns.Add("Grade");
table.Rows.Add(new object[] { "John Doe", "67" });
table.Rows.Add(new object[] { "Jane Doe", "81" });
table.Rows.Add(new object[] { "John Cardholder", "47" });
table.Rows.Add(new object[] { "Joe Bloggs", "75" });

// We can use a data view to alter the mail merge data without making changes to the data table itself.
DataView view = new DataView(table);
view.Sort = "Grade DESC";
view.RowFilter = "Grade >= 50";

// Our data view sorts the entries in descending order along the "Grade" column
// and filters out rows with values of less than 50 on that column.
// Three out of the four rows fit those criteria so that the output document will contain three merge documents.
doc.MailMerge.Execute(view);

doc.Save(ArtifactsDir + "MailMerge.ExecuteDataView.docx");
```

### See Also

* class [MailMerge](../../mailmerge)
* namespace [Aspose.Words.MailMerging](../../mailmerge)
* assembly [Aspose.Words](../../../)

---

## MailMerge.Execute method (6 of 6)

Performs mail merge from a DataRow into the document.

```csharp
public void Execute(DataRow row)
```

| Parameter | Type | Description |
| --- | --- | --- |
| row | DataRow | Row that contains data to be inserted into mail merge fields. Field names are not case sensitive. If a field name that is not found in the document is encountered, it is ignored. |

## Remarks

Use this method to fill mail merge fields in the document with values from a **DataRow**.

This method ignores the RemoveUnusedRegions option.

## Examples

Shows how to execute a mail merge with data from a DataTable.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // Below are two ways of using a DataTable as the data source for a mail merge.
    // 1 -  Use the entire table for the mail merge to create one output mail merge document for every row in the table:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 -  Use one row of the table to create one output mail merge document:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// Creates a mail merge source document.
/// </summary>
private static Document CreateSourceDocExecuteDataTable()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(" MERGEFIELD CustomerName ");
    builder.InsertParagraph();
    builder.InsertField(" MERGEFIELD Address ");

    return doc;
}
```

### See Also

* class [MailMerge](../../mailmerge)
* namespace [Aspose.Words.MailMerging](../../mailmerge)
* assembly [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
