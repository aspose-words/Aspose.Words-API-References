---
title: IFieldMergingCallback.ImageFieldMerging
second_title: Aspose.Words for .NET API Reference
description: IFieldMergingCallback method. Called when the Aspose.Words mail merge engine is about to insert an image into a merge field in C#.
type: docs
weight: 20
url: /net/aspose.words.mailmerging/ifieldmergingcallback/imagefieldmerging/
---
## IFieldMergingCallback.ImageFieldMerging method

Called when the Aspose.Words mail merge engine is about to insert an image into a merge field.

```csharp
public void ImageFieldMerging(ImageFieldMergingArgs args)
```

## Examples

Shows how to insert images stored in a database BLOB field into a report.

```csharp
public void ImageFromBlob()
{
    Document doc = new Document(MyDir + "Mail merge destination - Northwind employees.docx");

    doc.MailMerge.FieldMergingCallback = new HandleMergeImageFieldFromBlob();

    string connString = $"Provider=Microsoft.Jet.OLEDB.4.0;Data Source={DatabaseDir + "Northwind.mdb"};";
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

* class [ImageFieldMergingArgs](../../imagefieldmergingargs/)
* interface [IFieldMergingCallback](../)
* namespace [Aspose.Words.MailMerging](../../ifieldmergingcallback/)
* assembly [Aspose.Words](../../../)
