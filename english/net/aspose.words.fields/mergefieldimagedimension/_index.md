---
title: MergeFieldImageDimension Class
linktitle: MergeFieldImageDimension
articleTitle: MergeFieldImageDimension
second_title: Aspose.Words for .NET
description: Aspose.Words.Fields.MergeFieldImageDimension class. Represents an image dimension i.e. the width or the height used across a mail merge process in C#.
type: docs
weight: 2730
url: /net/aspose.words.fields/mergefieldimagedimension/
---
## MergeFieldImageDimension class

Represents an image dimension (i.e. the width or the height) used across a mail merge process.

To learn more, visit the [Working with Fields](https://docs.aspose.com/words/net/working-with-fields/) documentation article.

```csharp
public class MergeFieldImageDimension
```

## Constructors

| Name | Description |
| --- | --- |
| [MergeFieldImageDimension](mergefieldimagedimension/#constructor)(*double*) | Creates an image dimension instance with the given value in points. |
| [MergeFieldImageDimension](mergefieldimagedimension/#constructor_1)(*double, [MergeFieldImageDimensionUnit](../mergefieldimagedimensionunit/)*) | Creates an image dimension instance with the given value and the given unit. |

## Properties

| Name | Description |
| --- | --- |
| [Unit](../../aspose.words.fields/mergefieldimagedimension/unit/) { get; set; } | The unit. |
| [Value](../../aspose.words.fields/mergefieldimagedimension/value/) { get; set; } | The value. |

## Remarks

To indicate that the image should be inserted with its original dimension during a mail merge, you should assign a negative value to the [`Value`](./value/) property.

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
    }

    private readonly double mImageWidth;
    private readonly double mImageHeight;
    private readonly MergeFieldImageDimensionUnit mUnit;
}
```

### See Also

* namespace [Aspose.Words.Fields](../../aspose.words.fields/)
* assembly [Aspose.Words](../../)
