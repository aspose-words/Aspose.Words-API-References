---
title: FieldInclude.TextConverter
linktitle: TextConverter
articleTitle: TextConverter
second_title: Aspose.Words for .NET
description: FieldInclude TextConverter property. Gets or sets the name of the text converter for the format of the included file in C#.
type: docs
weight: 50
url: /net/aspose.words.fields/fieldinclude/textconverter/
---
## FieldInclude.TextConverter property

Gets or sets the name of the text converter for the format of the included file.

```csharp
public string TextConverter { get; set; }
```

## Examples

Shows how to create an INCLUDE field, and set its properties.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// We can use an INCLUDE field to import a portion of another document in the local file system.
// The bookmark from the other document that we reference with this field contains this imported portion.
FieldInclude field = (FieldInclude)builder.InsertField(FieldType.FieldInclude, true);
field.SourceFullName = MyDir + "Bookmarks.docx";
field.BookmarkName = "MyBookmark1";
field.LockFields = false;
field.TextConverter = "Microsoft Word";

Assert.True(Regex.Match(field.GetFieldCode(), " INCLUDE .* MyBookmark1 \\\\c \"Microsoft Word\"").Success);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INCLUDE.docx");
```

### See Also

* class [FieldInclude](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
