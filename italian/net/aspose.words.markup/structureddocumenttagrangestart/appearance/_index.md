---
title: StructuredDocumentTagRangeStart.Appearance
linktitle: Appearance
articleTitle: Appearance
second_title: Aspose.Words per .NET
description: Scopri come personalizzare l'aspetto di StructuredDocumentTagRangeStart per migliorare la formattazione del documento e la leggibilità.
type: docs
weight: 20
url: /it/net/aspose.words.markup/structureddocumenttagrangestart/appearance/
---
## StructuredDocumentTagRangeStart.Appearance property

Ottiene o imposta l'aspetto del tag del documento strutturato.

```csharp
public SdtAppearance Appearance { get; set; }
```

## Esempi

Mostra come visualizzare i tag attorno al contenuto.

```csharp
Document doc = new Document(MyDir + "Multi-section structured document tags.docx");
StructuredDocumentTagRangeStart tag =
    doc.GetChild(NodeType.StructuredDocumentTagRangeStart, 0, true) as StructuredDocumentTagRangeStart;

if (tag.Appearance == SdtAppearance.Hidden)
    tag.Appearance = SdtAppearance.Tags;
```

### Guarda anche

* enum [SdtAppearance](../../sdtappearance/)
* class [StructuredDocumentTagRangeStart](../)
* spazio dei nomi [Aspose.Words.Markup](../../../aspose.words.markup/)
* assemblea [Aspose.Words](../../../)
