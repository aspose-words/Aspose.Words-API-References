---
title: Document.OriginalLoadFormat
linktitle: OriginalLoadFormat
articleTitle: OriginalLoadFormat
second_title: Aspose.Words für .NET
description: Document OriginalLoadFormat eigendom. Ruft das Format des Originaldokuments ab das in dieses Objekt geladen wurde in C#.
type: docs
weight: 300
url: /de/net/aspose.words/document/originalloadformat/
---
## Document.OriginalLoadFormat property

Ruft das Format des Originaldokuments ab, das in dieses Objekt geladen wurde.

```csharp
public LoadFormat OriginalLoadFormat { get; }
```

## Bemerkungen

Wenn Sie ein neues leeres Dokument erstellt haben, wird Folgendes zurückgegeben:Doc Wert.

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
