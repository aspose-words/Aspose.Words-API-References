---
title: Frameset.ChildFramesets
second_title: Référence de l'API Aspose.Words pour .NET
description: Frameset propriété. Obtient la collection de cadres enfants et de pages de cadres.
type: docs
weight: 20
url: /fr/net/aspose.words.framesets/frameset/childframesets/
---
## Frameset.ChildFramesets property

Obtient la collection de cadres enfants et de pages de cadres.

```csharp
public FramesetCollection ChildFramesets { get; }
```

### Exemples

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

* class [FramesetCollection](../../framesetcollection/)
* class [Frameset](../)
* espace de noms [Aspose.Words.Framesets](../../frameset/)
* Assemblée [Aspose.Words](../../../)


