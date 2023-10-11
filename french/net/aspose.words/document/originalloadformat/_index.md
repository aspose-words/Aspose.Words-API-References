---
title: Document.OriginalLoadFormat
second_title: Référence de l'API Aspose.Words pour .NET
description: Document propriété. Obtient le format du document original chargé dans cet objet.
type: docs
weight: 300
url: /fr/net/aspose.words/document/originalloadformat/
---
## Document.OriginalLoadFormat property

Obtient le format du document original chargé dans cet objet.

```csharp
public LoadFormat OriginalLoadFormat { get; }
```

### Remarques

Si vous avez créé un nouveau document vierge, renvoie leDoc valeur.

### Exemples

Montre comment récupérer les détails de l’opération de chargement d’un document.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Assert.AreEqual(MyDir + "Document.docx", doc.OriginalFileName);
Assert.AreEqual(LoadFormat.Docx, doc.OriginalLoadFormat);
```

### Voir également

* enum [LoadFormat](../../loadformat/)
* class [Document](../)
* espace de noms [Aspose.Words](../../document/)
* Assemblée [Aspose.Words](../../../)


