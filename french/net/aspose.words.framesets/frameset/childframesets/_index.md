---
title: Frameset.ChildFramesets
linktitle: ChildFramesets
articleTitle: ChildFramesets
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Frameset ChildFramesets pour accéder et gérer facilement des collections de cadres et de pages enfants pour une conception Web améliorée.
type: docs
weight: 20
url: /fr/net/aspose.words.framesets/frameset/childframesets/
---
## Frameset.ChildFramesets property

Obtient la collection de cadres enfants et de pages de cadres.

```csharp
public FramesetCollection ChildFramesets { get; }
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

* class [FramesetCollection](../../framesetcollection/)
* class [Frameset](../)
* espace de noms [Aspose.Words.Framesets](../../../aspose.words.framesets/)
* Assemblée [Aspose.Words](../../../)
