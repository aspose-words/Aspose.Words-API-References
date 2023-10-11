---
title: Frameset.IsFrameLinkToFile
second_title: Aspose.Words per .NET API Reference
description: Frameset proprietà. Ottiene o imposta un valore che indica se il nome del file della pagina Web o del documento specificato in FrameDefaultUrl la proprietà è una risorsa esterna a cui è collegato il frame.
type: docs
weight: 40
url: /it/net/aspose.words.framesets/frameset/isframelinktofile/
---
## Frameset.IsFrameLinkToFile property

Ottiene o imposta un valore che indica se il nome del file della pagina Web o del documento specificato in [`FrameDefaultUrl`](../framedefaulturl/) la proprietà è una risorsa esterna a cui è collegato il frame.

```csharp
public bool IsFrameLinkToFile { get; set; }
```

### Esempi

Mostra come accedere ai frame sulla pagina.

```csharp
// Il documento contiene diversi frame con collegamenti ad altri documenti.
Document doc = new Document(MyDir + "Frameset.docx");

// Possiamo verificare l'URL predefinito (l'URL di una pagina Web o un documento locale) o se il frame è una risorsa esterna.
Assert.AreEqual("https://file-examples-com.github.io/uploads/2017/02/file-sample_100kB.docx",
    doc.Frameset.ChildFramesets[0].ChildFramesets[0].FrameDefaultUrl);
Assert.True(doc.Frameset.ChildFramesets[0].ChildFramesets[0].IsFrameLinkToFile);

Assert.AreEqual("Document.docx", doc.Frameset.ChildFramesets[1].FrameDefaultUrl);
Assert.False(doc.Frameset.ChildFramesets[1].IsFrameLinkToFile);

// Modifica le proprietà per uno dei nostri frame.
doc.Frameset.ChildFramesets[0].ChildFramesets[0].FrameDefaultUrl =
    "https://github.com/aspose-words/Aspose.Words-for-.NET/blob/master/Examples/Data/Absolute%20position%20tab.docx";
doc.Frameset.ChildFramesets[0].ChildFramesets[0].IsFrameLinkToFile = false;
```

### Guarda anche

* class [Frameset](../)
* spazio dei nomi [Aspose.Words.Framesets](../../frameset/)
* assemblea [Aspose.Words](../../../)


