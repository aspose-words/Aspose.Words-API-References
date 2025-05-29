---
title: StructuredDocumentTag.SdtType
linktitle: SdtType
articleTitle: SdtType
second_title: Aspose.Words för .NET
description: Upptäck SdtType-egenskapen i StructuredDocumentTag för att enkelt identifiera taggtyper och förbättra din dokumenthantering och organisation.
type: docs
weight: 250
url: /sv/net/aspose.words.markup/structureddocumenttag/sdttype/
---
## StructuredDocumentTag.SdtType property

Hämtar typ av detta**Tagg för strukturerat dokument** .

```csharp
public SdtType SdtType { get; }
```

## Exempel

Visar hur man hämtar typen för en tagg för ett strukturerat dokument.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");

List<StructuredDocumentTag> tags = doc.GetChildNodes(NodeType.StructuredDocumentTag, true)
    .OfType<StructuredDocumentTag>().ToList();

Assert.AreEqual(SdtType.RepeatingSection, tags[0].SdtType);
Assert.AreEqual(SdtType.RepeatingSectionItem, tags[1].SdtType);
Assert.AreEqual(SdtType.RichText, tags[2].SdtType);
```

### Se även

* enum [SdtType](../../sdttype/)
* class [StructuredDocumentTag](../)
* namnutrymme [Aspose.Words.Markup](../../../aspose.words.markup/)
* hopsättning [Aspose.Words](../../../)
