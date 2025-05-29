---
title: StructuredDocumentTagRangeStart.Appearance
linktitle: Appearance
articleTitle: Appearance
second_title: Aspose.Words för .NET
description: Upptäck hur du anpassar utseendet på StructuredDocumentTagRangeStart för förbättrad dokumentformatering och läsbarhet.
type: docs
weight: 20
url: /sv/net/aspose.words.markup/structureddocumenttagrangestart/appearance/
---
## StructuredDocumentTagRangeStart.Appearance property

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
* class [StructuredDocumentTagRangeStart](../)
* namnutrymme [Aspose.Words.Markup](../../../aspose.words.markup/)
* hopsättning [Aspose.Words](../../../)
