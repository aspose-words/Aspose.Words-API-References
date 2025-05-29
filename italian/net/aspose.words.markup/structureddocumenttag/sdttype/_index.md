---
title: StructuredDocumentTag.SdtType
linktitle: SdtType
articleTitle: SdtType
second_title: Aspose.Words per .NET
description: Scopri la proprietà SdtType di StructuredDocumentTag per identificare facilmente i tipi di tag, migliorando così la gestione e l'organizzazione dei tuoi documenti.
type: docs
weight: 250
url: /it/net/aspose.words.markup/structureddocumenttag/sdttype/
---
## StructuredDocumentTag.SdtType property

Ottiene il tipo di questo**Tag del documento strutturato** .

```csharp
public SdtType SdtType { get; }
```

## Esempi

Mostra come ottenere il tipo di un tag di documento strutturato.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");

List<StructuredDocumentTag> tags = doc.GetChildNodes(NodeType.StructuredDocumentTag, true)
    .OfType<StructuredDocumentTag>().ToList();

Assert.AreEqual(SdtType.RepeatingSection, tags[0].SdtType);
Assert.AreEqual(SdtType.RepeatingSectionItem, tags[1].SdtType);
Assert.AreEqual(SdtType.RichText, tags[2].SdtType);
```

### Guarda anche

* enum [SdtType](../../sdttype/)
* class [StructuredDocumentTag](../)
* spazio dei nomi [Aspose.Words.Markup](../../../aspose.words.markup/)
* assemblea [Aspose.Words](../../../)
