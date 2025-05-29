---
title: Document.Frameset
linktitle: Frameset
articleTitle: Frameset
second_title: Aspose.Words per .NET
description: Scopri la proprietà Frameset per i documenti. Ottieni un'istanza di Frameset per una perfetta integrazione delle pagine con frame. Migliora la tua esperienza web oggi stesso!
type: docs
weight: 170
url: /it/net/aspose.words/document/frameset/
---
## Document.Frameset property

Restituisce un`Frameset` istanza se questo documento rappresenta una pagina frame.

```csharp
public Frameset Frameset { get; }
```

## Osservazioni

Se il documento non è inquadrato, la proprietà ha la`null` valore.

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

* class [Frameset](../../../aspose.words.framesets/frameset/)
* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
