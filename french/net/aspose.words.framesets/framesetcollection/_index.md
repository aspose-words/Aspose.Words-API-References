---
title: FramesetCollection Class
linktitle: FramesetCollection
articleTitle: FramesetCollection
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words FramesetCollection, votre solution de référence pour gérer plusieurs instances Frameset sans effort dans le traitement de documents.
type: docs
weight: 3520
url: /fr/net/aspose.words.framesets/framesetcollection/
---
## FramesetCollection class

Représente une collection d'instances du[`Frameset`](../frameset/) classe.

Pour en savoir plus, visitez le[Programmation avec des documents](https://docs.aspose.com/words/net/programming-with-documents/) article de documentation.

```csharp
public class FramesetCollection : IEnumerable<Frameset>
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [FramesetCollection](framesetcollection/)() | Default_Constructor |

## Propriétés

| Nom | La description |
| --- | --- |
| [Count](../../aspose.words.framesets/framesetcollection/count/) { get; } | Obtient le nombre de cadres ou de pages de cadres contenus dans la collection. |
| [Item](../../aspose.words.framesets/framesetcollection/item/) { get; } | Obtient une ou plusieurs pages de cadres à l'index spécifié. |

## Méthodes

| Nom | La description |
| --- | --- |
| [GetEnumerator](../../aspose.words.framesets/framesetcollection/getenumerator/)() | Renvoie un énumérateur qui parcourt la collection. |

## Exemples

Montre comment accéder aux cadres sur la page.

```csharp
// Le document contient plusieurs cadres avec des liens vers d'autres documents.
Document doc = new Document(MyDir + "Frameset.docx");

Assert.AreEqual(3, doc.Frameset.ChildFramesets.Count);
// Nous pouvons vérifier l'URL par défaut (une URL de page Web ou un document local) ou si le cadre est une ressource externe.
Assert.AreEqual("https://fichier-exemples-com.github.io/uploads/2017/02/fichier-exemple_100kB.docx",
    doc.Frameset.ChildFramesets[0].ChildFramesets[0].FrameDefaultUrl);
Assert.True(doc.Frameset.ChildFramesets[0].ChildFramesets[0].IsFrameLinkToFile);

Assert.AreEqual("Document.docx", doc.Frameset.ChildFramesets[1].FrameDefaultUrl);
Assert.False(doc.Frameset.ChildFramesets[1].IsFrameLinkToFile);

// Modifier les propriétés de l'un de nos cadres.
doc.Frameset.ChildFramesets[0].ChildFramesets[0].FrameDefaultUrl =
    "https://github.com/aspose-words/Aspose.Words-for-.NET/blob/master/Examples/Data/Absolute%20position%20tab.docx";
doc.Frameset.ChildFramesets[0].ChildFramesets[0].IsFrameLinkToFile = false;
```

### Voir également

* class [Frameset](../frameset/)
* espace de noms [Aspose.Words.Framesets](../../aspose.words.framesets/)
* Assemblée [Aspose.Words](../../)
