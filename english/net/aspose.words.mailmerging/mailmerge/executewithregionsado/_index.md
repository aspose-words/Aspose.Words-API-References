---
title: MailMerge.ExecuteWithRegionsADO
linktitle: ExecuteWithRegionsADO
articleTitle: ExecuteWithRegionsADO
second_title: Aspose.Words for .NET
description: Streamline your document creation with the MailMerge ExecuteWithRegionsADO method. Effortlessly merge ADO Recordset data for personalized results.
type: docs
weight: 210
url: /net/aspose.words.mailmerging/mailmerge/executewithregionsado/
---
## MailMerge.ExecuteWithRegionsADO method

Performs mail merge from an ADO Recordset object into the document with mail merge regions.

```csharp
public void ExecuteWithRegionsADO(object recordset, string tableName)
```

| Parameter | Type | Description |
| --- | --- | --- |
| recordset | Object | ADO Recordset or Record object. |
| tableName | String | Name of the mail merge region in the document to populate. |

## Remarks

This method is useful when you intend to use Aspose.Words classes as COM objects from unmanaged code such as an application built using ASP or Visual Basic 6.0.

For more information see description of [`ExecuteWithRegions`](../executewithregions/).

## Examples

```csharp
[VBScript]

Dim RS
Set RS = CreateObject("ADODB.Recordset")
RS.Open _
    "SELECT * FROM AsposeWordOrderDetails WHERE OrderId = 10444 ORDER BY ProductID", _
    "Provider=Microsoft.Jet.OLEDB.4.0;Data Source=Northwind.mdb"

Dim Helper
Set Helper = CreateObject("Aspose.Words.ComHelper")

Dim Doc
Set Doc = Helper.Open("Invoice.doc")

Doc.MailMerge.ExecuteWithRegionsADO RS, "OrderDetails"
Doc.Save "Invoice Out VBScript.doc"
```

Shows how to run a mail merge with multiple regions, compiled with data from an ADO dataset.

```csharp
public void ExecuteWithRegionsADO()
{
    Document doc = CreateSourceDocADOMailMergeWithRegions();

    // To work with ADO DataSets, we will need to add a reference to the Microsoft ActiveX Data Objects library,
    // which is included in the .NET distribution and stored in "adodb.dll".
    Interop.ADODB.Connection connection = new Interop.ADODB.Connection();

    // Create a connection string that points to the "Northwind" database file
    // in our local file system and open a connection.
    string connectionString = @"Provider=Microsoft.ACE.OLEDB.12.0;Data Source=" + DatabaseDir + "Northwind.accdb";
    connection.Open(connectionString);

    // Populate our DataSet by running an SQL command on our database.
    // The names of the columns in the result table will need to correspond
    // to the values of the MERGEFIELDS that will accommodate our data.
    string command = "SELECT FirstName, LastName, City FROM Employees";

    Interop.ADODB.Recordset recordset = new Interop.ADODB.Recordset();
    recordset.Open(command, connection);

    // Run a mail merge on just the first region, filling its MERGEFIELDS with data from the record set.
    doc.MailMerge.ExecuteWithRegionsADO(recordset, "MergeRegion1");

    // Close the record set and reopen it with data from another SQL query.
    command = "SELECT * FROM Customers";

    recordset.Close();
    recordset.Open(command, connection);

    // Run a second mail merge on the second region and save the document.
    doc.MailMerge.ExecuteWithRegionsADO(recordset, "MergeRegion2");

    doc.Save(ArtifactsDir + "MailMerge.ExecuteWithRegionsADO.docx");

}

/// <summary>
/// Create a document with two mail merge regions.
/// </summary>
private static Document CreateSourceDocADOMailMergeWithRegions()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("\tEmployees: ");
    builder.InsertField(" MERGEFIELD TableStart:MergeRegion1");
    builder.InsertField(" MERGEFIELD FirstName");
    builder.Write(", ");
    builder.InsertField(" MERGEFIELD LastName");
    builder.Write(", ");
    builder.InsertField(" MERGEFIELD City");
    builder.InsertField(" MERGEFIELD TableEnd:MergeRegion1");
    builder.InsertParagraph();

    builder.Writeln("\tCustomers: ");
    builder.InsertField(" MERGEFIELD TableStart:MergeRegion2");
    builder.InsertField(" MERGEFIELD ContactName");
    builder.Write(", ");
    builder.InsertField(" MERGEFIELD Address");
    builder.Write(", ");
    builder.InsertField(" MERGEFIELD City");
    builder.InsertField(" MERGEFIELD TableEnd:MergeRegion2");

    return doc;
}
```

### See Also

* class [MailMerge](../)
* namespace [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* assembly [Aspose.Words](../../../)
