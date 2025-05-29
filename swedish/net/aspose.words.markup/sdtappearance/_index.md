---
title: SdtAppearance Enum
linktitle: SdtAppearance
articleTitle: SdtAppearance
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Markup.SdtAppearance enum för att anpassa utseendet på strukturerade dokumenttaggar. Förbättra din dokumentformatering utan ansträngning!
type: docs
weight: 4680
url: /sv/net/aspose.words.markup/sdtappearance/
---
## SdtAppearance enumeration

Anger utseendet på en strukturerad dokumenttagg.

```csharp
public enum SdtAppearance
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| BoundingBox | `0` | Representerar en strukturerad dokumenttagg som visas som en skuggad rektangel eller avgränsningsruta. |
| Tags | `1` | Representerar en strukturerad dokumenttagg som visas som start- och slutmarkörer. |
| Hidden | `2` | Representerar en strukturerad dokumenttagg som inte visas. |
| Default | `0` | StandardinställningBoundingBox . |

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

* namnutrymme [Aspose.Words.Markup](../../aspose.words.markup/)
* hopsättning [Aspose.Words](../../)
