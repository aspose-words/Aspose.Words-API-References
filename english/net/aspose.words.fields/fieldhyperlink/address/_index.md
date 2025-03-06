---
title: FieldHyperlink.Address
linktitle: Address
articleTitle: Address
second_title: Aspose.Words for .NET
description: Discover the FieldHyperlink Address property. Easily manage hyperlink destinations for seamless navigation in your applications. Enhance user experience today!
type: docs
weight: 20
url: /net/aspose.words.fields/fieldhyperlink/address/
---
## FieldHyperlink.Address property

Gets or sets a location where this hyperlink jumps.

```csharp
public string Address { get; set; }
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
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
