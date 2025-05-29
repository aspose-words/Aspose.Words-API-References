---
title: Frameset Class
linktitle: Frameset
articleTitle: Frameset
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Framesets.Frameset pour une gestion fluide des cadres dans vos documents. Améliorez vos pages web grâce à une intégration efficace des cadres !
type: docs
weight: 3510
url: /fr/net/aspose.words.framesets/frameset/
---
## Frameset class

Représente une page de cadres ou un seul cadre sur une page de cadres.

Pour en savoir plus, visitez le[Programmation avec des documents](https://docs.aspose.com/words/net/programming-with-documents/) article de documentation.

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
| [IsFrameLinkToFile](../../aspose.words.framesets/frameset/isframelinktofile/) { get; set; } | Obtient ou définit une valeur indiquant si le nom du fichier de page Web ou de document spécifié dans le [`FrameDefaultUrl`](./framedefaulturl/) la propriété est une ressource externe à laquelle le cadre est lié. |

## Remarques

Si le[`ChildFramesets`](./childframesets/) la propriété contient des éléments, cette instance est une page de cadres, sinon il s'agit d'un seul cadre.

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

* espace de noms [Aspose.Words.Framesets](../../aspose.words.framesets/)
* Assemblée [Aspose.Words](../../)
