---
title: Frameset.FrameDefaultUrl
linktitle: FrameDefaultUrl
articleTitle: FrameDefaultUrl
second_title: Aspose.Words für .NET
description: Frameset FrameDefaultUrl eigendom. Ruft die URL der Webseite oder den Namen der Dokumentdatei ab die in diesem Frame angezeigt werden sollen oder legt diese fest in C#.
type: docs
weight: 30
url: /de/net/aspose.words.framesets/frameset/framedefaulturl/
---
## Frameset.FrameDefaultUrl property

Ruft die URL der Webseite oder den Namen der Dokumentdatei ab, die in diesem Frame angezeigt werden sollen, oder legt diese fest.

```csharp
public string FrameDefaultUrl { get; set; }
```

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

* class [Frameset](../)
* namensraum [Aspose.Words.Framesets](../../../aspose.words.framesets/)
* Montage [Aspose.Words](../../../)
