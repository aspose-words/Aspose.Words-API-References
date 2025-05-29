---
title: Frameset Class
linktitle: Frameset
articleTitle: Frameset
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Framesets.Frameset per una gestione fluida dei frame nei documenti. Migliora le tue pagine web con un'integrazione efficiente dei frame!
type: docs
weight: 3510
url: /it/net/aspose.words.framesets/frameset/
---
## Frameset class

Rappresenta una pagina frame o un singolo frame su una pagina frame.

Per saperne di più, visita il[Programmazione con documenti](https://docs.aspose.com/words/net/programming-with-documents/) articolo di documentazione.

```csharp
public class Frameset
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [Frameset](frameset/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [ChildFramesets](../../aspose.words.framesets/frameset/childframesets/) { get; } | Ottiene la raccolta di frame figlio e pagine di frame. |
| [FrameDefaultUrl](../../aspose.words.framesets/frameset/framedefaulturl/) { get; set; } | Ottiene o imposta l'URL della pagina web o il nome del file del documento da visualizzare in questo frame. |
| [IsFrameLinkToFile](../../aspose.words.framesets/frameset/isframelinktofile/) { get; set; } | Ottiene o imposta un valore che indica se la pagina web o il nome del file del documento specificato in [`FrameDefaultUrl`](./framedefaulturl/) la proprietà è una risorsa esterna a cui è collegato il frame. |

## Osservazioni

Se il[`ChildFramesets`](./childframesets/) la proprietà contiene elementi, questa istanza è una pagina frame, altrimenti è un singolo frame.

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

* spazio dei nomi [Aspose.Words.Framesets](../../aspose.words.framesets/)
* assemblea [Aspose.Words](../../)
