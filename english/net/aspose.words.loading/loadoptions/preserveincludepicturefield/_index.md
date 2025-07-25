---
title: LoadOptions.PreserveIncludePictureField
linktitle: PreserveIncludePictureField
articleTitle: PreserveIncludePictureField
second_title: Aspose.Words for .NET
description: Control the INCLUDEPICTURE field in Microsoft Word formats with LoadOptions PreserveIncludePictureField. Easily manage document formatting for optimal results.
type: docs
weight: 120
url: /net/aspose.words.loading/loadoptions/preserveincludepicturefield/
---
## LoadOptions.PreserveIncludePictureField property

Gets or sets whether to preserve the INCLUDEPICTURE field when reading Microsoft Word formats. The default value is `false`.

```csharp
public bool PreserveIncludePictureField { get; set; }
```

## Remarks

By default, the INCLUDEPICTURE field is converted into a shape object. You can override that if you need the field to be preserved, for example, if you wish to update it programmatically. Note however that this approach is not common for Aspose.Words. Use it on your own risk.

One of the possible use cases may be using a MERGEFIELD as a child field to dynamically change the source path of the picture. In this case you need the INCLUDEPICTURE to be preserved in the model.

## Examples

Shows how to preserve or discard INCLUDEPICTURE fields when loading a document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldIncludePicture includePicture = (FieldIncludePicture)builder.InsertField(FieldType.FieldIncludePicture, true);
includePicture.SourceFullName = ImageDir + "Transparent background logo.png";
includePicture.Update(true);

using (MemoryStream docStream = new MemoryStream())
{
    doc.Save(docStream, new OoxmlSaveOptions(SaveFormat.Docx));

    // We can set a flag in a LoadOptions object to decide whether to convert all INCLUDEPICTURE fields
    // into image shapes when loading a document that contains them.
    LoadOptions loadOptions = new LoadOptions
    {
        PreserveIncludePictureField = preserveIncludePictureField
    };

    doc = new Document(docStream, loadOptions);

    if (preserveIncludePictureField)
    {
        Assert.That(doc.Range.Fields.Any(f => f.Type == FieldType.FieldIncludePicture), Is.True);

        doc.UpdateFields();
        doc.Save(ArtifactsDir + "Field.PreserveIncludePicture.docx");
    }
    else
    {
        Assert.That(doc.Range.Fields.Any(f => f.Type == FieldType.FieldIncludePicture), Is.False);
    }
}
```

### See Also

* class [LoadOptions](../)
* namespace [Aspose.Words.Loading](../../../aspose.words.loading/)
* assembly [Aspose.Words](../../../)
