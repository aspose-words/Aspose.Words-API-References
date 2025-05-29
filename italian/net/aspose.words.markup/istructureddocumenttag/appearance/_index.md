---
title: IStructuredDocumentTag.Appearance
linktitle: Appearance
articleTitle: Appearance
second_title: Aspose.Words per .NET
description: Scopri la proprietà Aspetto IStructuredDocumentTag per personalizzare e migliorare i tag dei tuoi documenti strutturati, migliorando l'esperienza utente.
type: docs
weight: 10
url: /it/net/aspose.words.markup/istructureddocumenttag/appearance/
---
## IStructuredDocumentTag.Appearance property

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
* interface [IStructuredDocumentTag](../)
* spazio dei nomi [Aspose.Words.Markup](../../../aspose.words.markup/)
* assemblea [Aspose.Words](../../../)
