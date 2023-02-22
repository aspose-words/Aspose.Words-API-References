---
title: StructuredDocumentTag.SdtType
second_title: Aspose.Words per .NET API Reference
description: StructuredDocumentTag proprietà. Ottiene il tipo di questo Tag del documento strutturato .
type: docs
weight: 250
url: /it/net/aspose.words.markup/structureddocumenttag/sdttype/
---
## StructuredDocumentTag.SdtType property

Ottiene il tipo di questo **Tag del documento strutturato** .

```csharp
public SdtType SdtType { get; }
```

### Esempi

Mostra come ottenere il tipo di tag di un documento strutturato.

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
* spazio dei nomi [Aspose.Words.Markup](../../structureddocumenttag/)
* assemblea [Aspose.Words](../../../)


