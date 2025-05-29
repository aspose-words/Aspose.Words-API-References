---
title: StructuredDocumentTagRangeStart.Appearance
linktitle: Appearance
articleTitle: Appearance
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie Sie das Erscheinungsbild von StructuredDocumentTagRangeStart anpassen können, um die Dokumentformatierung und Lesbarkeit zu verbessern.
type: docs
weight: 20
url: /de/net/aspose.words.markup/structureddocumenttagrangestart/appearance/
---
## StructuredDocumentTagRangeStart.Appearance property

Ruft das Erscheinungsbild des strukturierten Dokumenttags ab oder legt es fest.

```csharp
public SdtAppearance Appearance { get; set; }
```

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

* enum [SdtAppearance](../../sdtappearance/)
* class [StructuredDocumentTagRangeStart](../)
* namensraum [Aspose.Words.Markup](../../../aspose.words.markup/)
* Montage [Aspose.Words](../../../)
