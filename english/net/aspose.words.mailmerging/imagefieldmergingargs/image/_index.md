---
title: ImageFieldMergingArgs.Image
linktitle: Image
second_title: Aspose.Words for .NET API Reference
description: ImageFieldMergingArgs Image property. Specifies the image that the mail merge engine must insert into the document in C#.
type: docs
weight: 10
url: /net/aspose.words.mailmerging/imagefieldmergingargs/image/
---
## Image property

Specifies the image that the mail merge engine must insert into the document.

```csharp
public Image Image { get; set; }
```

## Examples

Shows how to use a callback to customize image merging logic.

```csharp
public void MergeFieldImages()
{
    Document doc = new Document();

    // Insert a MERGEFIELD that will accept images from a source during a mail merge. Use the field code to reference
    // a column in the data source which contains local system filenames of images we wish to use in the mail merge.
    DocumentBuilder builder = new DocumentBuilder(doc);
    FieldMergeField field = (FieldMergeField)builder.InsertField("MERGEFIELD Image:ImageColumn");

    // In this case, the field expects the data source to have such a column named "ImageColumn".
    Assert.AreEqual("Image:ImageColumn", field.FieldName);

    // Filenames can be lengthy, and if we can find a way to avoid storing them in the data source,
    // we may considerably reduce its size.
    // Create a data source that refers to images using short names.
    DataTable dataTable = new DataTable("Images");
    dataTable.Columns.Add(new DataColumn("ImageColumn"));
    dataTable.Rows.Add("Dark logo");
    dataTable.Rows.Add("Transparent logo");

    // Assign a merging callback that contains all logic that processes those names,
    // and then execute the mail merge. 
    doc.MailMerge.FieldMergingCallback = new ImageFilenameCallback();
    doc.MailMerge.Execute(dataTable);

    doc.Save(ArtifactsDir + "Field.MERGEFIELD.Images.docx");
}

/// <summary>
/// Contains a dictionary that maps names of images to local system filenames that contain these images.
/// If a mail merge data source uses one of the dictionary's names to refer to an image,
/// this callback will pass the respective filename to the merge destination.
/// </summary>
private class ImageFilenameCallback : IFieldMergingCallback
{
    public ImageFilenameCallback()
    {
        mImageFilenames = new Dictionary<string, string>();
        mImageFilenames.Add("Dark logo", ImageDir + "Logo.jpg");
        mImageFilenames.Add("Transparent logo", ImageDir + "Transparent background logo.png");
    }

    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        throw new NotImplementedException();
    }

    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs args)
    {
        if (mImageFilenames.ContainsKey(args.FieldValue.ToString()))
        {
            #if NET48 || JAVA
            args.Image = Image.FromFile(mImageFilenames[args.FieldValue.ToString()]);
            #elif NET5_0_OR_GREATER
            args.Image = SKBitmap.Decode(mImageFilenames[args.FieldValue.ToString()]);
            args.ImageFileName = mImageFilenames[args.FieldValue.ToString()];
            #endif
        }

        Assert.NotNull(args.Image);
    }

    private readonly Dictionary<string, string> mImageFilenames;
}
```

### See Also

* class [ImageFieldMergingArgs](../)
* namespace [Aspose.Words.MailMerging](../../imagefieldmergingargs/)
* assembly [Aspose.Words](../../../)
