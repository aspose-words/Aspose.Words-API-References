---
title: FontInfoCollection.Contains
linktitle: Contains
articleTitle: Contains
second_title: Aspose.Words pour .NET
description: FontInfoCollection Contains méthode. Détermine si la collection contient une police portant le nom donné en C#.
type: docs
weight: 60
url: /fr/net/aspose.words.fonts/fontinfocollection/contains/
---
## FontInfoCollection.Contains method

Détermine si la collection contient une police portant le nom donné.

```csharp
public bool Contains(string name)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| name | String | Nom de la police à localiser, qui ne respecte pas la casse. |

### Return_Value

`vrai` si l'objet est trouvé dans la collection ; sinon,`FAUX`.

## Exemples

Affiche des informations sur les polices présentes dans le document vierge.

```csharp
Document doc = new Document();

// Un document vierge contient 3 polices par défaut. Chaque police du document
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
