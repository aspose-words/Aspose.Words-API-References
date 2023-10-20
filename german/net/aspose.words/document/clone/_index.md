---
title: Document.Clone
linktitle: Clone
articleTitle: Clone
second_title: Aspose.Words für .NET
description: Document Clone methode. Führt eine tiefe Kopie des ausDocument  in C#.
type: docs
weight: 550
url: /de/net/aspose.words/document/clone/
---
## Document.Clone method

Führt eine tiefe Kopie des aus[`Document`](../) .

```csharp
public Document Clone()
```

### Rückgabewert

Das geklonte Dokument.

## Beispiele

Zeigt, wie ein Dokument tief geklont wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

// Durch das Klonen wird ein neues Dokument mit demselben Inhalt wie das Original erstellt.
// aber mit einer eindeutigen Kopie jedes Knotens des Originaldokuments.
Document clone = doc.Clone();

Assert.AreEqual(doc.FirstSection.Body.FirstParagraph.Runs[0].GetText(), 
    clone.FirstSection.Body.FirstParagraph.Runs[0].Text);
Assert.AreNotEqual(doc.FirstSection.Body.FirstParagraph.Runs[0].GetHashCode(),
    clone.FirstSection.Body.FirstParagraph.Runs[0].GetHashCode());
```

### Siehe auch

* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
