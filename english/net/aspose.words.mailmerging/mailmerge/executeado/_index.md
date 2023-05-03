---
title: MailMerge.ExecuteADO
linktitle: ExecuteADO
second_title: Aspose.Words for .NET API Reference
description: MailMerge ExecuteADO method. Performs mail merge from an ADO Recordset object into the document in C#.
type: docs
weight: 190
url: /net/aspose.words.mailmerging/mailmerge/executeado/
---
## MailMerge.ExecuteADO method

Performs mail merge from an ADO Recordset object into the document.

```csharp
public void ExecuteADO(object recordset)
```

| Parameter | Type | Description |
| --- | --- | --- |
| recordset | Object | ADO Recordset or Record object. |

## Remarks

This method is useful when you intend to use Aspose.Words classes as COM objects from unmanaged code such as an application built using ASP or Visual Basic 6.0.

This method ignores the RemoveUnusedRegions option.

For more information see description of [`Execute`](../execute/).

## Examples

```csharp
[VBScript]

Dim RS
Set RS = CreateObject("ADODB.Recordset")
RS.Open _
    "SELECT TOP 50 * FROM Customers ORDER BY Country, CompanyName", _
    "Provider=Microsoft.Jet.OLEDB.4.0;Data Source=Northwind.mdb"

Dim License
Set License = CreateObject("Aspose.Words.License")
License.SetLicense "C:\MyPath\MyLicense.lic"

Dim Helper
Set Helper = CreateObject("Aspose.Words.ComHelper")
Dim Doc
Set Doc = Helper.Open("CustomerLabels.doc")

Doc.MailMerge.ExecuteADO RS
Doc.Save "C:\MyPath\CustomerLabels Out VBScript.doc"
```

Shows how to run a mail merge with data from an ADO dataset.

```csharp
public void ExecuteADO()
{
    Document doc = CreateSourceDocADOMailMerge();

    // To work with ADO DataSets, we will need to add a reference to the Microsoft ActiveX Data Objects library,
    // which is included in the .NET distribution and stored in "adodb.dll".
    ADODB.Connection connection = new ADODB.Connection();

    // Create a connection string that points to the "Northwind" database file
    // in our local file system and open a connection.
    string connectionString = @"Provider=Microsoft.Jet.OLEDB.4.0;Data Source=" + DatabaseDir + "Northwind.mdb";
    connection.Open(connectionString);

    // Populate our DataSet by running an SQL command on our database.
    // The names of the columns in the result table will need to correspond
    // to the values of the MERGEFIELDS that will accommodate our data.
    const string command = @"SELECT ProductName, QuantityPerUnit, UnitPrice FROM Products";

    ADODB.Recordset recordset = new ADODB.Recordset();
    recordset.Open(command, connection);

    // Execute the mail merge and save the document.
    doc.MailMerge.ExecuteADO(recordset);
    doc.Save(ArtifactsDir + "MailMerge.ExecuteADO.docx");
}

/// <summary>
/// Create a blank document and populate it with MERGEFIELDS that will accept data when a mail merge is executed.
/// </summary>
private static Document CreateSourceDocADOMailMerge()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Write("Product:\t");
    builder.InsertField(" MERGEFIELD ProductName");
    builder.Writeln();
    builder.InsertField(" MERGEFIELD QuantityPerUnit");
    builder.Write(" for $");
    builder.InsertField(" MERGEFIELD UnitPrice");

    return doc;
}
```

### See Also

* class [MailMerge](../)
* namespace [Aspose.Words.MailMerging](../../mailmerge/)
* assembly [Aspose.Words](../../../)
