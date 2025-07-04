---
title: FieldInclude.LockFields
linktitle: LockFields
articleTitle: LockFields
second_title: Aspose.Words for .NET
description: Manage document updates effortlessly with the FieldInclude LockFields property. Control field editing and enhance document integrity with ease.
type: docs
weight: 30
url: /net/aspose.words.fields/fieldinclude/lockfields/
---
## FieldInclude.LockFields property

Gets or sets whether to prevent fields in the included document from being updated.

```csharp
public bool LockFields { get; set; }
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

Assert.That(Regex.Match(field.GetFieldCode(), " INCLUDE .* MyBookmark1 \\\\c \"Microsoft Word\"").Success, Is.True);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INCLUDE.docx");
```

### See Also

* class [FieldInclude](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
