---
title: FieldIncludePicture.IsLinked
linktitle: IsLinked
second_title: Aspose.Words for .NET API Reference
description: FieldIncludePicture IsLinked property. Gets or sets whether to reduce the file size by not storing graphics data with the document in C#.
type: docs
weight: 30
url: /net/aspose.words.fields/fieldincludepicture/islinked/
---
## IsLinked property

Gets or sets whether to reduce the file size by not storing graphics data with the document.

```csharp
public bool IsLinked { get; set; }
```

## Examples

Shows how to insert images using IMPORT and INCLUDEPICTURE fields.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Below are two similar field types that we can use to display images linked from the local file system.
// 1 -  The INCLUDEPICTURE field:
FieldIncludePicture fieldIncludePicture = (FieldIncludePicture)builder.InsertField(FieldType.FieldIncludePicture, true);
fieldIncludePicture.SourceFullName = ImageDir + "Transparent background logo.png";

Assert.True(Regex.Match(fieldIncludePicture.GetFieldCode(), " INCLUDEPICTURE  .*").Success);

// Apply the PNG32.FLT filter.
fieldIncludePicture.GraphicFilter = "PNG32";
fieldIncludePicture.IsLinked = true;
fieldIncludePicture.ResizeHorizontally = true;
fieldIncludePicture.ResizeVertically = true;

// 2 -  The IMPORT field:
FieldImport fieldImport = (FieldImport)builder.InsertField(FieldType.FieldImport, true);
fieldImport.SourceFullName = ImageDir + "Transparent background logo.png";
fieldImport.GraphicFilter = "PNG32";
fieldImport.IsLinked = true;

Assert.True(Regex.Match(fieldImport.GetFieldCode(), " IMPORT  .* \\\\c PNG32 \\\\d").Success);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.IMPORT.INCLUDEPICTURE.docx");
```

### See Also

* class [FieldIncludePicture](../)
* namespace [Aspose.Words.Fields](../../fieldincludepicture/)
* assembly [Aspose.Words](../../../)
