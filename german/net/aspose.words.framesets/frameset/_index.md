---
title: Frameset Class
linktitle: Frameset
articleTitle: Frameset
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Framesets.Frameset für nahtloses Frame-Management in Dokumenten. Verbessern Sie Ihre Webseiten mit effizienter Frame-Integration!
type: docs
weight: 3510
url: /de/net/aspose.words.framesets/frameset/
---
## Frameset class

Stellt eine Frames-Seite oder einen einzelnen Frame auf einer Frames-Seite dar.

Um mehr zu erfahren, besuchen Sie die[Programmieren mit Dokumenten](https://docs.aspose.com/words/net/programming-with-documents/) Dokumentationsartikel.

```csharp
public class Frameset
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [Frameset](frameset/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [ChildFramesets](../../aspose.words.framesets/frameset/childframesets/) { get; } | Ruft die Sammlung untergeordneter Frames und Frameseiten ab. |
| [FrameDefaultUrl](../../aspose.words.framesets/frameset/framedefaulturl/) { get; set; } | Ruft die URL der Webseite oder den Dateinamen des Dokuments ab oder legt diese fest, um sie in diesem Frame anzuzeigen. |
| [IsFrameLinkToFile](../../aspose.words.framesets/frameset/isframelinktofile/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob der in der Datei angegebene Name der Webseite oder des Dokuments[`FrameDefaultUrl`](./framedefaulturl/) Eigenschaft ist eine externe Ressource, mit der der Frame verknüpft ist. |

## Bemerkungen

Wenn die[`ChildFramesets`](./childframesets/) Eigenschaft enthält Elemente, diese Instanz ist eine Frames-Seite, andernfalls ist es ein einzelner Frame.

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

* namensraum [Aspose.Words.Framesets](../../aspose.words.framesets/)
* Montage [Aspose.Words](../../)
