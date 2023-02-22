---
title: Document.Clone
second_title: Référence de l'API Aspose.Words pour .NET
description: Document méthode. Effectue une copie complète duDocument .
type: docs
weight: 530
url: /fr/net/aspose.words/document/clone/
---
## Document.Clone method

Effectue une copie complète du[`Document`](../) .

```csharp
public Document Clone()
```

### Return_Value

Le document cloné.

### Exemples

Montre comment cloner en profondeur un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

// Le clonage produira un nouveau document avec le même contenu que l'original,
// mais avec une copie unique de chacun des nœuds du document d'origine.
Document clone = doc.Clone();

Assert.AreEqual(doc.FirstSection.Body.FirstParagraph.Runs[0].GetText(), 
    clone.FirstSection.Body.FirstParagraph.Runs[0].Text);
Assert.AreNotEqual(doc.FirstSection.Body.FirstParagraph.Runs[0].GetHashCode(),
    clone.FirstSection.Body.FirstParagraph.Runs[0].GetHashCode());
```

### Voir également

* class [Document](../)
* espace de noms [Aspose.Words](../../document/)
* Assemblée [Aspose.Words](../../../)


