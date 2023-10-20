---
title: Frameset Class
linktitle: Frameset
articleTitle: Frameset
second_title: Aspose.Words für .NET
description: Aspose.Words.Framesets.Frameset klas. Stellt eine FramesSeite oder einen einzelnen Frame auf einer FramesSeite dar in C#.
type: docs
weight: 3080
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
| [ChildFramesets](../../aspose.words.framesets/frameset/childframesets/) { get; } | Ruft die Sammlung untergeordneter Frames und Frame-Seiten ab. |
| [FrameDefaultUrl](../../aspose.words.framesets/frameset/framedefaulturl/) { get; set; } | Ruft die URL der Webseite oder den Namen der Dokumentdatei ab, die in diesem Frame angezeigt werden sollen, oder legt diese fest. |
| [IsFrameLinkToFile](../../aspose.words.framesets/frameset/isframelinktofile/) { get; set; } | Ruft einen Wert ab oder legt diesen fest, der angibt, ob der in the angegebene Webseiten- oder Dokumentdateiname verwendet wird.[`FrameDefaultUrl`](./framedefaulturl/) Eigenschaft ist eine externe Ressource, mit der der Frame verknüpft ist. |

## Bemerkungen

Wenn die[`ChildFramesets`](./childframesets/) Die Eigenschaft enthält Elemente. Diese Instanz ist eine Frames-Seite, andernfalls handelt es sich um einen einzelnen Frame.

## Beispiele

Zeigt, wie man auf Frames auf der Seite zugreift.

```csharp
// Dokument enthält mehrere Frames mit Links zu anderen Dokumenten.
Document doc = new Document(MyDir + "Frameset.docx");

// Wir können die Standard-URL (eine Webseiten-URL oder ein lokales Dokument) überprüfen oder ob der Frame eine externe Ressource ist.
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
