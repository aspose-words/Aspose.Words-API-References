---
title: Document.OriginalLoadFormat
linktitle: OriginalLoadFormat
articleTitle: OriginalLoadFormat
second_title: Aspose.Words pour .NET
description: Découvrez la propriété OriginalLoadFormat pour accéder facilement au format du document original chargé dans votre objet, améliorant ainsi la gestion des documents.
type: docs
weight: 310
url: /fr/net/aspose.words/document/originalloadformat/
---
## Document.OriginalLoadFormat property

Obtient le format du document d'origine qui a été chargé dans cet objet.

```csharp
public LoadFormat OriginalLoadFormat { get; }
```

## Remarques

Si vous avez créé un nouveau document vierge, renvoie leDoc valeur.

## Exemples

Montre comment récupérer les détails de l'opération de chargement d'un document.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Assert.AreEqual(MyDir + "Document.docx", doc.OriginalFileName);
Assert.AreEqual(LoadFormat.Docx, doc.OriginalLoadFormat);
```

### Voir également

* enum [LoadFormat](../../loadformat/)
* class [Document](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
