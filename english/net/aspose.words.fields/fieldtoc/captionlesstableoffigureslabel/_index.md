---
title: FieldToc.CaptionlessTableOfFiguresLabel
linktitle: CaptionlessTableOfFiguresLabel
articleTitle: CaptionlessTableOfFiguresLabel
second_title: Aspose.Words for .NET
description: Discover the FieldToc CaptionlessTableOfFiguresLabel property to customize your table of figures. Easily manage sequence identifiers without captions!
type: docs
weight: 30
url: /net/aspose.words.fields/fieldtoc/captionlesstableoffigureslabel/
---
## FieldToc.CaptionlessTableOfFiguresLabel property

Gets or sets the name of the sequence identifier used when building a table of figures that does not include caption's label and number.

```csharp
public string CaptionlessTableOfFiguresLabel { get; set; }
```

## Examples

Shows how to set the name of the sequence identifier.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);
fieldToc.CaptionlessTableOfFiguresLabel = "Test";

Assert.AreEqual(" TOC  \\a Test", fieldToc.GetFieldCode());
```

### See Also

* class [FieldToc](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
