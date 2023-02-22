---
title: ImageFieldMergingArgs Class
second_title: Aspose.Words for .NET API Reference
description: Aspose.Words.MailMerging.ImageFieldMergingArgs class. Provides data for the ImageFieldMerging event in C#.
type: docs
weight: 3630
url: /net/aspose.words.mailmerging/imagefieldmergingargs/
---
## ImageFieldMergingArgs class

Provides data for the [`ImageFieldMerging`](../ifieldmergingcallback/imagefieldmerging/) event.

To learn more, visit the [Mail Merge and Reporting](https://docs.aspose.com/words/net/mail-merge-and-reporting/) documentation article.

```csharp
public class ImageFieldMergingArgs : FieldMergingArgsBase
```

## Properties

| Name | Description |
| --- | --- |
| [Document](../../aspose.words.mailmerging/fieldmergingargsbase/document/) { get; } | Returns the [`Document`](../fieldmergingargsbase/document/) object for which the mail merge is performed. |
| [DocumentFieldName](../../aspose.words.mailmerging/fieldmergingargsbase/documentfieldname/) { get; } | Gets the name of the merge field as specified in the document. |
| [Field](../../aspose.words.mailmerging/fieldmergingargsbase/field/) { get; } | Gets the object that represents the current merge field. |
| [FieldName](../../aspose.words.mailmerging/fieldmergingargsbase/fieldname/) { get; } | Gets the name of the merge field in the data source. |
| [FieldValue](../../aspose.words.mailmerging/fieldmergingargsbase/fieldvalue/) { get; set; } | Gets or sets the value of the field from the data source. |
| [Image](../../aspose.words.mailmerging/imagefieldmergingargs/image/) { get; set; } | Specifies the image that the mail merge engine must insert into the document. |
| [ImageFileName](../../aspose.words.mailmerging/imagefieldmergingargs/imagefilename/) { get; set; } | Sets the file name of the image that the mail merge engine must insert into the document. |
| [ImageHeight](../../aspose.words.mailmerging/imagefieldmergingargs/imageheight/) { get; set; } | Specifies the image height for the image to insert into the document. |
| [ImageStream](../../aspose.words.mailmerging/imagefieldmergingargs/imagestream/) { get; set; } | Specifies the stream for the mail merge engine to read an image from. |
| [ImageWidth](../../aspose.words.mailmerging/imagefieldmergingargs/imagewidth/) { get; set; } | Specifies the image width for the image to insert into the document. |
| [RecordIndex](../../aspose.words.mailmerging/fieldmergingargsbase/recordindex/) { get; } | Gets the zero based index of the record that is being merged. |
| [Shape](../../aspose.words.mailmerging/imagefieldmergingargs/shape/) { get; set; } | Specifies the shape that the mail merge engine must insert into the document. |
| [TableName](../../aspose.words.mailmerging/fieldmergingargsbase/tablename/) { get; } | Gets the name of the data table for the current merge operation or empty string if the name is not available. |

## Remarks

This event occurs during mail merge when an image mail merge field is encountered in the document. You can respond to this event to return a file name, stream, or an Image object to the mail merge engine so it is inserted into the document.

There are three properties available [`ImageFileName`](./imagefilename/), [`ImageStream`](./imagestream/) and [`Image`](./image/) to specify where the image must be taken from. Set only one of these properties.

To insert an image mail merge field into a document in Word, select Insert/Field command, then select MergeField and type Image:MyFieldName.

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

Shows how to set the dimensions of images as MERGEFIELDS accepts them during a mail merge.

```csharp
{
    Document doc = new Document();

    // Insert a MERGEFIELD that will accept images from a source during a mail merge. Use the field code to reference
    // a column in the data source containing local system filenames of images we wish to use in the mail merge.
    DocumentBuilder builder = new DocumentBuilder(doc);
    FieldMergeField field = (FieldMergeField)builder.InsertField("MERGEFIELD Image:ImageColumn");

    // The data source should have such a column named "ImageColumn".
    Assert.AreEqual("Image:ImageColumn", field.FieldName);

    // Create a suitable data source.
    DataTable dataTable = new DataTable("Images");
    dataTable.Columns.Add(new DataColumn("ImageColumn"));
    dataTable.Rows.Add(ImageDir + "Logo.jpg");
    dataTable.Rows.Add(ImageDir + "Transparent background logo.png");
    dataTable.Rows.Add(ImageDir + "Enhanced Windows MetaFile.emf");

    // Configure a callback to modify the sizes of images at merge time, then execute the mail merge.
    doc.MailMerge.FieldMergingCallback = new MergedImageResizer(200, 200, MergeFieldImageDimensionUnit.Point);
    doc.MailMerge.Execute(dataTable);

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.MERGEFIELD.ImageDimension.docx");

/// <summary>
/// Sets the size of all mail merged images to one defined width and height.
/// </summary>
private class MergedImageResizer : IFieldMergingCallback
{
    public MergedImageResizer(double imageWidth, double imageHeight, MergeFieldImageDimensionUnit unit)
    {
        mImageWidth = imageWidth;
        mImageHeight = imageHeight;
        mUnit = unit;
    }

    public void FieldMerging(FieldMergingArgs e)
    {
        throw new NotImplementedException();
    }

    public void ImageFieldMerging(ImageFieldMergingArgs args)
    {
        args.ImageFileName = args.FieldValue.ToString();
        args.ImageWidth = new MergeFieldImageDimension(mImageWidth, mUnit);
        args.ImageHeight = new MergeFieldImageDimension(mImageHeight, mUnit);

        Assert.AreEqual(mImageWidth, args.ImageWidth.Value);
        Assert.AreEqual(mUnit, args.ImageWidth.Unit);
        Assert.AreEqual(mImageHeight, args.ImageHeight.Value);
        Assert.AreEqual(mUnit, args.ImageHeight.Unit);
    }

    private readonly double mImageWidth;
    private readonly double mImageHeight;
    private readonly MergeFieldImageDimensionUnit mUnit;
}
```

### See Also

* class [FieldMergingArgsBase](../fieldmergingargsbase/)
* namespace [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* assembly [Aspose.Words](../../)
