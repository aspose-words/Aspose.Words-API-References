---
title: TabStopCollection.GetIndexByPosition
linktitle: GetIndexByPosition
articleTitle: GetIndexByPosition
second_title: Aspose.Words pour .NET
description: TabStopCollection GetIndexByPosition méthode. Obtient lindex dun taquet de tabulation avec la position spécifiée en points en C#.
type: docs
weight: 90
url: /fr/net/aspose.words/tabstopcollection/getindexbyposition/
---
## TabStopCollection.GetIndexByPosition method

Obtient l'index d'un taquet de tabulation avec la position spécifiée en points.

```csharp
public int GetIndexByPosition(double position)
```

## Exemples

Montre comment rechercher une position pour voir si un taquet de tabulation existe à cet endroit et obtenir son index.

```csharp
Document doc = new Document();
TabStopCollection tabStops = doc.FirstSection.Body.Paragraphs[0].ParagraphFormat.TabStops;

// Ajout d'un taquet de tabulation à une position de 30 mm.
tabStops.Add(ConvertUtil.MillimeterToPoint(30), TabAlignment.Left, TabLeader.Dashes);

// Un résultat "0" renvoyé par "GetIndexByPosition" confirme qu'un taquet de tabulation
// à 30 mm existe dans cette collection, et il est à l'index 0.
Assert.AreEqual(0, tabStops.GetIndexByPosition(ConvertUtil.MillimeterToPoint(30)));

// Un "-1" renvoyé par "GetIndexByPosition" confirme que
// il n'y a pas de taquet de tabulation dans cette collection avec une position de 60 mm.
Assert.AreEqual(-1, tabStops.GetIndexByPosition(ConvertUtil.MillimeterToPoint(60)));
```

### Voir également

* class [TabStopCollection](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
