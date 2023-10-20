---
title: Frameset Class
linktitle: Frameset
articleTitle: Frameset
second_title: Aspose.Words pour .NET
description: Aspose.Words.Framesets.Frameset classe. Représente une page de cadres ou un seul cadre sur une page de cadres en C#.
type: docs
weight: 3080
url: /fr/net/aspose.words.framesets/frameset/
---
## Frameset class

Représente une page de cadres ou un seul cadre sur une page de cadres.

Pour en savoir plus, visitez le[Programmation avec des documents](https://docs.aspose.com/words/net/programming-with-documents/) article documentaire.

```csharp
public class Frameset
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [Frameset](frameset/)() | Default_Constructor |

## Propriétés

| Nom | La description |
| --- | --- |
| [ChildFramesets](../../aspose.words.framesets/frameset/childframesets/) { get; } | Obtient la collection de cadres enfants et de pages de cadres. |
| [FrameDefaultUrl](../../aspose.words.framesets/frameset/framedefaulturl/) { get; set; } | Obtient ou définit l'URL de la page Web ou le nom du fichier de document à afficher dans ce cadre. |
| [IsFrameLinkToFile](../../aspose.words.framesets/frameset/isframelinktofile/) { get; set; } | Obtient ou définit une valeur indiquant si le nom de la page Web ou du fichier de document spécifié dans the [`FrameDefaultUrl`](./framedefaulturl/) la propriété est une ressource externe à laquelle le cadre est lié. |

## Remarques

Si le[`ChildFramesets`](./childframesets/) la propriété contient des éléments, cette instance est une page de cadres, sinon il s'agit d'un seul cadre.

## Exemples

Montre comment accéder aux cadres sur la page.

```csharp
// Le document contient plusieurs cadres avec des liens vers d'autres documents.
Document doc = new Document(MyDir + "Frameset.docx");

// Nous pouvons vérifier l'URL par défaut (une URL de page Web ou un document local) ou si le cadre est une ressource externe.
Assert.AreEqual("https://file-examples-com.github.io/uploads/2017/02/file-sample_100kB.docx",
    doc.Frameset.ChildFramesets[0].ChildFramesets[0].FrameDefaultUrl);
Assert.True(doc.Frameset.ChildFramesets[0].ChildFramesets[0].IsFrameLinkToFile);

Assert.AreEqual("Document.docx", doc.Frameset.ChildFramesets[1].FrameDefaultUrl);
Assert.False(doc.Frameset.ChildFramesets[1].IsFrameLinkToFile);

// Change les propriétés d'un de nos frames.
doc.Frameset.ChildFramesets[0].ChildFramesets[0].FrameDefaultUrl =
    "https://github.com/aspose-words/Aspose.Words-for-.NET/blob/master/Examples/Data/Absolute%20position%20tab.docx" ;
doc.Frameset.ChildFramesets[0].ChildFramesets[0].IsFrameLinkToFile = false;
```

### Voir également

* espace de noms [Aspose.Words.Framesets](../../aspose.words.framesets/)
* Assemblée [Aspose.Words](../../)
