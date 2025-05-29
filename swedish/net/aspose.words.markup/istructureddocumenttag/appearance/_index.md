---
title: IStructuredDocumentTag.Appearance
linktitle: Appearance
articleTitle: Appearance
second_title: Aspose.Words för .NET
description: Upptäck egenskapen IStructuredDocumentTag Appearance för att anpassa och förbättra dina strukturerade dokumenttaggar för en förbättrad användarupplevelse.
type: docs
weight: 10
url: /sv/net/aspose.words.markup/istructureddocumenttag/appearance/
---
## IStructuredDocumentTag.Appearance property

Hämtar eller ställer in utseendet på den strukturerade dokumenttaggen.

```csharp
public SdtAppearance Appearance { get; set; }
```

## Exempel

Visar hur man visar taggar runt innehåll.

```csharp
Document doc = new Document(MyDir + "Multi-section structured document tags.docx");
StructuredDocumentTagRangeStart tag =
    doc.GetChild(NodeType.StructuredDocumentTagRangeStart, 0, true) as StructuredDocumentTagRangeStart;

if (tag.Appearance == SdtAppearance.Hidden)
    tag.Appearance = SdtAppearance.Tags;
```

### Se även

* enum [SdtAppearance](../../sdtappearance/)
* interface [IStructuredDocumentTag](../)
* namnutrymme [Aspose.Words.Markup](../../../aspose.words.markup/)
* hopsättning [Aspose.Words](../../../)
