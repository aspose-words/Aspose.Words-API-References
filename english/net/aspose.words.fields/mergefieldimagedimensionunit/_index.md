---
title: MergeFieldImageDimensionUnit Enum
linktitle: MergeFieldImageDimensionUnit
articleTitle: MergeFieldImageDimensionUnit
second_title: Aspose.Words for .NET
description: Discover Aspose.Words.Fields.MergeFieldImageDimensionUnit enum for precise image dimension control in mail merges. Enhance your document automation today!
type: docs
weight: 3170
url: /net/aspose.words.fields/mergefieldimagedimensionunit/
---
## MergeFieldImageDimensionUnit enumeration

Specifies an unit of an image dimension (i.e. the width or the height) used across a mail merge process.

```csharp
public enum MergeFieldImageDimensionUnit
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Point | `0` | The point (i.e. 1/72 inch). |
| Percent | `1` | The percent of the original image dimension value. |

## Examples

Shows how to set the dimensions of images as MERGEFIELDS accepts them during a mail merge.

```csharp
public void MergeFieldImageDimension()
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
}

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
        Assert.Null(args.Shape);
    }

    private readonly double mImageWidth;
    private readonly double mImageHeight;
    private readonly MergeFieldImageDimensionUnit mUnit;
}
```

### See Also

* namespace [Aspose.Words.Fields](../../aspose.words.fields/)
* assembly [Aspose.Words](../../)
