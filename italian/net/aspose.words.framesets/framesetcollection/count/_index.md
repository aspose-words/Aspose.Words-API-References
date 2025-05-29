---
title: FramesetCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words per .NET
description: Scopri la proprietà FramesetCollection Count, accedi facilmente al numero totale di frame nella tua raccolta per una gestione web efficiente.
type: docs
weight: 20
url: /it/net/aspose.words.framesets/framesetcollection/count/
---
## FramesetCollection.Count property

Ottiene il numero di frame o di pagine di frame contenute nella raccolta.

```csharp
public int Count { get; }
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

* class [FramesetCollection](../)
* spazio dei nomi [Aspose.Words.Framesets](../../../aspose.words.framesets/)
* assemblea [Aspose.Words](../../../)
