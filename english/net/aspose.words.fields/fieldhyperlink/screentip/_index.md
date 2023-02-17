---
title: FieldHyperlink.ScreenTip
second_title: Aspose.Words for .NET API Reference
description: FieldHyperlink property. Gets or sets the ScreenTip text for the hyperlink in C#.
type: docs
weight: 50
url: /net/aspose.words.fields/fieldhyperlink/screentip/
---
## FieldHyperlink.ScreenTip property

Gets or sets the ScreenTip text for the hyperlink.

```csharp
public string ScreenTip { get; set; }
```

## Examples

Shows how to use HYPERLINK fields to link to documents in the local file system.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldHyperlink field = (FieldHyperlink)builder.InsertField(FieldType.FieldHyperlink, true);

// When we click this HYPERLINK field in Microsoft Word,
// it will open the linked document and then place the cursor at the specified bookmark.
field.Address = MyDir + "Bookmarks.docx";
field.SubAddress = "MyBookmark3";
field.ScreenTip = "Open " + field.Address + " on bookmark " + field.SubAddress + " in a new window";

builder.Writeln();

// When we click this HYPERLINK field in Microsoft Word,
// it will open the linked document, and automatically scroll down to the specified iframe.
field = (FieldHyperlink)builder.InsertField(FieldType.FieldHyperlink, true);
field.Address = MyDir + "Iframes.html";
field.ScreenTip = "Open " + field.Address;
field.Target = "iframe_3";
field.OpenInNewWindow = true;
field.IsImageMap = false;

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.HYPERLINK.docx");
```

### See Also

* class [FieldHyperlink](../)
* namespace [Aspose.Words.Fields](../../fieldhyperlink/)
* assembly [Aspose.Words](../../../)
