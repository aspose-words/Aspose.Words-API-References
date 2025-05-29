---
title: Frameset.FrameDefaultUrl
linktitle: FrameDefaultUrl
articleTitle: FrameDefaultUrl
second_title: Aspose.Words pour .NET
description: Découvrez la propriété FrameDefaultUrl du jeu de cadres pour définir facilement les URL de pages web ou de documents et obtenir un affichage fluide des cadres. Améliorez votre expérience web !
type: docs
weight: 30
url: /fr/net/aspose.words.framesets/frameset/framedefaulturl/
---
## Frameset.FrameDefaultUrl property

Obtient ou définit l'URL de la page Web ou le nom du fichier de document à afficher dans ce cadre.

```csharp
public string FrameDefaultUrl { get; set; }
```

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

* class [Frameset](../)
* espace de noms [Aspose.Words.Framesets](../../../aspose.words.framesets/)
* Assemblée [Aspose.Words](../../../)
