---
title: FramesetCollection Class
linktitle: FramesetCollection
articleTitle: FramesetCollection
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aspose.Words FramesetCollection-Klasse, Ihre Lösung für die mühelose Verwaltung mehrerer Frameset-Instanzen bei der Dokumentverarbeitung.
type: docs
weight: 3520
url: /de/net/aspose.words.framesets/framesetcollection/
---
## FramesetCollection class

Stellt eine Sammlung von Instanzen des[`Frameset`](../frameset/) Klasse.

Um mehr zu erfahren, besuchen Sie die[Programmieren mit Dokumenten](https://docs.aspose.com/words/net/programming-with-documents/) Dokumentationsartikel.

```csharp
public class FramesetCollection : IEnumerable<Frameset>
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [FramesetCollection](framesetcollection/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Count](../../aspose.words.framesets/framesetcollection/count/) { get; } | Ruft die Anzahl der in der Sammlung enthaltenen Frames oder Frameseiten ab. |
| [Item](../../aspose.words.framesets/framesetcollection/item/) { get; } | Ruft einen Frame oder eine Frameseite am angegebenen Index ab. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [GetEnumerator](../../aspose.words.framesets/framesetcollection/getenumerator/)() | Gibt einen Enumerator zurück, der die Sammlung durchläuft. |

## Beispiele

Zeigt, wie auf Frames auf der Seite zugegriffen wird.

```csharp
// Das Dokument enthält mehrere Frames mit Links zu anderen Dokumenten.
Document doc = new Document(MyDir + "Frameset.docx");

Assert.AreEqual(3, doc.Frameset.ChildFramesets.Count);
// Wir können die Standard-URL (die URL einer Webseite oder eines lokalen Dokuments) überprüfen oder ob es sich bei dem Frame um eine externe Ressource handelt.
Assert.AreEqual("https://file-examples-com.github.io/uploads/2017/02/file-sample_100kB.docx",
    doc.Frameset.ChildFramesets[0].ChildFramesets[0].FrameDefaultUrl);
Assert.True(doc.Frameset.ChildFramesets[0].ChildFramesets[0].IsFrameLinkToFile);

Assert.AreEqual("Document.docx", doc.Frameset.ChildFramesets[1].FrameDefaultUrl);
Assert.False(doc.Frameset.ChildFramesets[1].IsFrameLinkToFile);

// Eigenschaften für einen unserer Frames ändern.
doc.Frameset.ChildFramesets[0].ChildFramesets[0].FrameDefaultUrl =
    "https://github.com/aspose-words/Aspose.Words-for-.NET/blob/master/Examples/Data/Absolute%20position%20tab.docx";
doc.Frameset.ChildFramesets[0].ChildFramesets[0].IsFrameLinkToFile = false;
```

### Siehe auch

* class [Frameset](../frameset/)
* namensraum [Aspose.Words.Framesets](../../aspose.words.framesets/)
* Montage [Aspose.Words](../../)
