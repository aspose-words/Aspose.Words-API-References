---
title: TabStopCollection.RemoveByIndex
second_title: Référence de l'API Aspose.Words pour .NET
description: TabStopCollection méthode. Supprime un taquet de tabulation à lindex spécifié de la collection.
type: docs
weight: 110
url: /fr/net/aspose.words/tabstopcollection/removebyindex/
---
## TabStopCollection.RemoveByIndex method

Supprime un taquet de tabulation à l'index spécifié de la collection.

```csharp
public void RemoveByIndex(int index)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| index | Int32 | Un index dans la collection de taquets de tabulation. |

### Exemples

Montre comment sélectionner un taquet de tabulation dans un document par son index et le supprimer.

```csharp
Document doc = new Document();
TabStopCollection tabStops = doc.FirstSection.Body.Paragraphs[0].ParagraphFormat.TabStops;

tabStops.Add(ConvertUtil.MillimeterToPoint(30), TabAlignment.Left, TabLeader.Dashes);
tabStops.Add(ConvertUtil.MillimeterToPoint(60), TabAlignment.Left, TabLeader.Dashes);

Assert.AreEqual(2, tabStops.Count);

// Supprime le premier taquet de tabulation.
tabStops.RemoveByIndex(0);

Assert.AreEqual(1, tabStops.Count);

doc.Save(ArtifactsDir + "TabStopCollection.RemoveByIndex.docx");
```

### Voir également

* class [TabStopCollection](../)
* espace de noms [Aspose.Words](../../tabstopcollection/)
* Assemblée [Aspose.Words](../../../)


