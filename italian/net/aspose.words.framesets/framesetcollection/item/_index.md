---
title: FramesetCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words per .NET
description: Accedi a frame specifici con FramesetCollection. Recupera facilmente le pagine dei frame tramite indice per una navigazione web efficiente e un'esperienza utente migliorata.
type: docs
weight: 30
url: /it/net/aspose.words.framesets/framesetcollection/item/
---
## FramesetCollection indexer

Ottiene una o più pagine frame all'indice specificato.

```csharp
public Frameset this[int index] { get; }
```

## Esempi

Mostra come accedere ai frame nella pagina.

```csharp
// Il documento contiene diversi frame con collegamenti ad altri documenti.
Document doc = new Document(MyDir + "Frameset.docx");

Assert.AreEqual(3, doc.Frameset.ChildFramesets.Count);
// Possiamo controllare l'URL predefinito (l'URL di una pagina web o un documento locale) o se il frame è una risorsa esterna.
Assert.AreEqual("https://file-examples-com.github.io/uploads/2017/02/file-sample_100kB.docx",
    doc.Frameset.ChildFramesets[0].ChildFramesets[0].FrameDefaultUrl);
Assert.True(doc.Frameset.ChildFramesets[0].ChildFramesets[0].IsFrameLinkToFile);

Assert.AreEqual("Document.docx", doc.Frameset.ChildFramesets[1].FrameDefaultUrl);
Assert.False(doc.Frameset.ChildFramesets[1].IsFrameLinkToFile);

// Modifica le proprietà di uno dei nostri frame.
doc.Frameset.ChildFramesets[0].ChildFramesets[0].FrameDefaultUrl =
    "https://github.com/aspose-words/Aspose.Words-for-.NET/blob/master/Examples/Data/Absolute%20position%20tab.docx";
doc.Frameset.ChildFramesets[0].ChildFramesets[0].IsFrameLinkToFile = false;
```

### Guarda anche

* class [Frameset](../../frameset/)
* class [FramesetCollection](../)
* spazio dei nomi [Aspose.Words.Framesets](../../../aspose.words.framesets/)
* assemblea [Aspose.Words](../../../)
