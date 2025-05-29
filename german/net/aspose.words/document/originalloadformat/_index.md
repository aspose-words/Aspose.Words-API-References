---
title: Document.OriginalLoadFormat
linktitle: OriginalLoadFormat
articleTitle: OriginalLoadFormat
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft OriginalLoadFormat, um einfach auf das Format des in Ihr Objekt geladenen Originaldokuments zuzugreifen und so die Dokumentenverwaltung zu verbessern.
type: docs
weight: 310
url: /de/net/aspose.words/document/originalloadformat/
---
## Document.OriginalLoadFormat property

Ruft das Format des Originaldokuments ab, das in dieses Objekt geladen wurde.

```csharp
public LoadFormat OriginalLoadFormat { get; }
```

## Bemerkungen

Wenn Sie ein neues leeres Dokument erstellt haben, gibt dasDoc Wert.

## Beispiele

Zeigt, wie Details zum Ladevorgang eines Dokuments abgerufen werden.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Assert.AreEqual(MyDir + "Document.docx", doc.OriginalFileName);
Assert.AreEqual(LoadFormat.Docx, doc.OriginalLoadFormat);
```

### Siehe auch

* enum [LoadFormat](../../loadformat/)
* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
