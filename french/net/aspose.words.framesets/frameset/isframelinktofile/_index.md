---
title: Frameset.IsFrameLinkToFile
linktitle: IsFrameLinkToFile
articleTitle: IsFrameLinkToFile
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété Frameset IsFrameLinkToFile améliore la conception de votre site web en reliant facilement des ressources externes. Optimisez vos cadres pour de meilleures performances !
type: docs
weight: 40
url: /fr/net/aspose.words.framesets/frameset/isframelinktofile/
---
## Frameset.IsFrameLinkToFile property

Obtient ou définit une valeur indiquant si le nom du fichier de page Web ou de document spécifié dans le [`FrameDefaultUrl`](../framedefaulturl/) la propriété est une ressource externe à laquelle le cadre est lié.

```csharp
public bool IsFrameLinkToFile { get; set; }
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
