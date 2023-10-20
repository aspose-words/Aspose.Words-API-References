---
title: PageInfo.Colored
linktitle: Colored
articleTitle: Colored
second_title: Aspose.Words pour .NET
description: PageInfo Colored propriété. Retoursvrai si la page contient du contenu coloré en C#.
type: docs
weight: 10
url: /fr/net/aspose.words.rendering/pageinfo/colored/
---
## PageInfo.Colored property

Retours`vrai` si la page contient du contenu coloré.

```csharp
public bool Colored { get; }
```

## Exemples

Montre comment vérifier si la page est en couleur ou non.

```csharp
Document doc = new Document(MyDir + "Document.docx");

// Vérifiez que la première page du document n'est pas colorée.
Assert.IsFalse(doc.GetPageInfo(0).Colored);
```

### Voir également

* class [PageInfo](../)
* espace de noms [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* Assemblée [Aspose.Words](../../../)
