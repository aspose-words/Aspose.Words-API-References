---
title: FontInfoCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words pour .NET
description: Découvrez la propriété FontInfoCollection Count, récupérez sans effort le nombre total d'éléments de votre collection pour une gestion transparente des données.
type: docs
weight: 10
url: /fr/net/aspose.words.fonts/fontinfocollection/count/
---
## FontInfoCollection.Count property

Obtient le nombre d'éléments contenus dans la collection.

```csharp
public int Count { get; }
```

## Exemples

Affiche des informations sur les polices présentes dans le document vierge.

```csharp
Document doc = new Document();

// Un document vierge contient trois polices par défaut. Chaque police du document
// aura un objet FontInfo correspondant qui contient des détails sur cette police.
Assert.AreEqual(3, doc.FontInfos.Count);

Assert.True(doc.FontInfos.Contains("Times New Roman"));
Assert.AreEqual(204, doc.FontInfos["Times New Roman"].Charset);

Assert.True(doc.FontInfos.Contains("Symbol"));
Assert.True(doc.FontInfos.Contains("Arial"));
```

### Voir également

* class [FontInfoCollection](../)
* espace de noms [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Assemblée [Aspose.Words](../../../)
