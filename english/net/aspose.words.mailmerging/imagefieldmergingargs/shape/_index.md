---
title: ImageFieldMergingArgs.Shape
linktitle: Shape
articleTitle: Shape
second_title: Aspose.Words for .NET
description: Discover how the ImageFieldMergingArgs Shape property enhances your mail merge documents by allowing precise shape insertion for a polished look.
type: docs
weight: 60
url: /net/aspose.words.mailmerging/imagefieldmergingargs/shape/
---
## ImageFieldMergingArgs.Shape property

Specifies the shape that the mail merge engine must insert into the document.

```csharp
public Shape Shape { get; set; }
```

## Remarks

When this property is specified, the mail merge engine ignores all other properties like [`ImageFileName`](../imagefilename/) or [`ImageStream`](../imagestream/) and simply inserts the shape into the document.

Use this property to fully control the process of merging an image merge field. For example, you can specify [`WrapType`](../../../aspose.words.drawing/shapebase/wraptype/) or any other shape property to fine tune the resulting node. However, please note that you are responsible for providing the content of the shape.

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
    Assert.That(field.FieldName, Is.EqualTo("Image:ImageColumn"));

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

        Assert.That(args.ImageWidth.Value, Is.EqualTo(mImageWidth));
        Assert.That(args.ImageWidth.Unit, Is.EqualTo(mUnit));
        Assert.That(args.ImageHeight.Value, Is.EqualTo(mImageHeight));
        Assert.That(args.ImageHeight.Unit, Is.EqualTo(mUnit));
        Assert.That(args.Shape, Is.Null);
    }

    private readonly double mImageWidth;
    private readonly double mImageHeight;
    private readonly MergeFieldImageDimensionUnit mUnit;
}
```

### See Also

* class [Shape](../../../aspose.words.drawing/shape/)
* class [ImageFieldMergingArgs](../)
* namespace [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* assembly [Aspose.Words](../../../)
