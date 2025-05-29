---
title: IStructuredDocumentTag.SdtType
linktitle: SdtType
articleTitle: SdtType
second_title: Aspose.Words per .NET
description: Scopri la proprietà IStructuredDocumentTag SdtType per identificare facilmente il tipo di tag di documenti strutturati per una gestione avanzata dei documenti.
type: docs
weight: 120
url: /it/net/aspose.words.markup/istructureddocumenttag/sdttype/
---
## IStructuredDocumentTag.SdtType property

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
* interface [IStructuredDocumentTag](../)
* spazio dei nomi [Aspose.Words.Markup](../../../aspose.words.markup/)
* assemblea [Aspose.Words](../../../)
