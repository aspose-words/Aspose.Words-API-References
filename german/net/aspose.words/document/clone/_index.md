---
title: Document.Clone
second_title: Aspose.Words für .NET-API-Referenz
description: Document methode. Führt eine tiefe Kopie derDocument .
type: docs
weight: 530
url: /de/net/aspose.words/document/clone/
---
## Document.Clone method

Führt eine tiefe Kopie der[`Document`](../) .

```csharp
public Document Clone()
```

### Rückgabewert

Das geklonte Dokument.

### Beispiele

Zeigt, wie ein Dokument tief geklont wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

// Beim Klonen wird ein neues Dokument mit demselben Inhalt wie das Original erstellt,
// aber mit einer einzigartigen Kopie jedes Knotens des Originaldokuments.
Document clone = doc.Clone();

Assert.AreEqual(doc.FirstSection.Body.FirstParagraph.Runs[0].GetText(), 
    clone.FirstSection.Body.FirstParagraph.Runs[0].Text);
Assert.AreNotEqual(doc.FirstSection.Body.FirstParagraph.Runs[0].GetHashCode(),
    clone.FirstSection.Body.FirstParagraph.Runs[0].GetHashCode());
```

### Siehe auch

* class [Document](../)
* namensraum [Aspose.Words](../../document/)
* Montage [Aspose.Words](../../../)


