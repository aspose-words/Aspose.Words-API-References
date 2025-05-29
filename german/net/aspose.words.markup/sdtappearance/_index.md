---
title: SdtAppearance Enum
linktitle: SdtAppearance
articleTitle: SdtAppearance
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aufzählung Aspose.Words.Markup.SdtAppearance zum Anpassen des Erscheinungsbilds strukturierter Dokument-Tags. Verbessern Sie mühelos die Formatierung Ihrer Dokumente!
type: docs
weight: 4680
url: /de/net/aspose.words.markup/sdtappearance/
---
## SdtAppearance enumeration

Gibt das Erscheinungsbild eines strukturierten Dokument-Tags an.

```csharp
public enum SdtAppearance
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| BoundingBox | `0` | Stellt ein strukturiertes Dokument-Tag dar, das als schattiertes Rechteck oder Begrenzungsrahmen angezeigt wird. |
| Tags | `1` | Stellt ein strukturiertes Dokument-Tag dar, das als Start- und Endmarkierungen angezeigt wird. |
| Hidden | `2` | Stellt ein strukturiertes Dokument-Tag dar, das nicht angezeigt wird. |
| Default | `0` | StandardmäßigBoundingBox . |

## Beispiele

Zeigt, wie Tags um Inhalte herum angezeigt werden.

```csharp
Document doc = new Document(MyDir + "Multi-section structured document tags.docx");
StructuredDocumentTagRangeStart tag =
    doc.GetChild(NodeType.StructuredDocumentTagRangeStart, 0, true) as StructuredDocumentTagRangeStart;

if (tag.Appearance == SdtAppearance.Hidden)
    tag.Appearance = SdtAppearance.Tags;
```

### Siehe auch

* namensraum [Aspose.Words.Markup](../../aspose.words.markup/)
* Montage [Aspose.Words](../../)
