---
title: Document.Clone
linktitle: Clone
articleTitle: Clone
second_title: Aspose.Words pour .NET
description: Dupliquez facilement vos documents grâce à notre méthode de clonage de documents. Réalisez des copies précises et détaillées pour une édition fluide et un flux de travail efficace.
type: docs
weight: 590
url: /fr/net/aspose.words/document/clone/
---
## Document.Clone method

Effectue une copie en profondeur du[`Document`](../) .

```csharp
public Document Clone()
```

### Return_Value

Le document cloné.

## Exemples

Montre comment cloner en profondeur un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

// Le clonage produira un nouveau document avec le même contenu que l'original,
// mais avec une copie unique de chacun des nœuds du document original.
Document clone = doc.Clone();

Assert.AreEqual(doc.FirstSection.Body.FirstParagraph.Runs[0].GetText(),
    clone.FirstSection.Body.FirstParagraph.Runs[0].Text);
Assert.AreNotEqual(doc.FirstSection.Body.FirstParagraph.Runs[0].GetHashCode(),
    clone.FirstSection.Body.FirstParagraph.Runs[0].GetHashCode());
```

### Voir également

* class [Document](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
