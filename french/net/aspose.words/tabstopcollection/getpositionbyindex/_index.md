---
title: TabStopCollection.GetPositionByIndex
linktitle: GetPositionByIndex
articleTitle: GetPositionByIndex
second_title: Aspose.Words pour .NET
description: Découvrez la méthode GetPositionByIndex de TabStopCollection pour trouver facilement la position des taquets de tabulation en points par index. Optimisez votre mise en page sans effort !
type: docs
weight: 100
url: /fr/net/aspose.words/tabstopcollection/getpositionbyindex/
---
## TabStopCollection.GetPositionByIndex method

Obtient la position (en points) du taquet de tabulation à l'index spécifié.

```csharp
public double GetPositionByIndex(int index)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| index | Int32 | Un index dans la collection des taquets de tabulation. |

### Return_Value

La position de la tabulation.

## Exemples

Montre comment trouver un onglet, s'arrêter à son index et vérifier sa position.

```csharp
Document doc = new Document();
TabStopCollection tabStops = doc.FirstSection.Body.Paragraphs[0].ParagraphFormat.TabStops;

tabStops.Add(ConvertUtil.MillimeterToPoint(30), TabAlignment.Left, TabLeader.Dashes);
tabStops.Add(ConvertUtil.MillimeterToPoint(60), TabAlignment.Left, TabLeader.Dashes);

// Vérifiez la position du deuxième taquet de tabulation dans la collection.
Assert.AreEqual(ConvertUtil.MillimeterToPoint(60), tabStops.GetPositionByIndex(1), 0.1d);
```

### Voir également

* class [TabStopCollection](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
