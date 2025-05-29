---
title: FramesetCollection Class
linktitle: FramesetCollection
articleTitle: FramesetCollection
second_title: Aspose.Words per .NET
description: Scopri la classe FramesetCollection di Aspose.Words, la soluzione ideale per gestire senza problemi più istanze di Frameset nell'elaborazione dei documenti.
type: docs
weight: 3520
url: /it/net/aspose.words.framesets/framesetcollection/
---
## FramesetCollection class

Rappresenta una raccolta di istanze di[`Frameset`](../frameset/) classe.

Per saperne di più, visita il[Programmazione con documenti](https://docs.aspose.com/words/net/programming-with-documents/) articolo di documentazione.

```csharp
public class FramesetCollection : IEnumerable<Frameset>
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [FramesetCollection](framesetcollection/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Count](../../aspose.words.framesets/framesetcollection/count/) { get; } | Ottiene il numero di frame o di pagine di frame contenute nella raccolta. |
| [Item](../../aspose.words.framesets/framesetcollection/item/) { get; } | Ottiene una o più pagine frame all'indice specificato. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [GetEnumerator](../../aspose.words.framesets/framesetcollection/getenumerator/)() | Restituisce un enumeratore che scorre la raccolta. |

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

* class [Frameset](../frameset/)
* spazio dei nomi [Aspose.Words.Framesets](../../aspose.words.framesets/)
* assemblea [Aspose.Words](../../)
