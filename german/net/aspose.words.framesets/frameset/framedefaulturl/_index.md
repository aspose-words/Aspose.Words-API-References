---
title: Frameset.FrameDefaultUrl
linktitle: FrameDefaultUrl
articleTitle: FrameDefaultUrl
second_title: Aspose.Words für .NET
description: Entdecken Sie die Frameset-Eigenschaft FrameDefaultUrl, um Webseiten-URLs oder Dokumentdateien einfach für die nahtlose Frame-Anzeige festzulegen. Verbessern Sie Ihr Web-Erlebnis!
type: docs
weight: 30
url: /de/net/aspose.words.framesets/frameset/framedefaulturl/
---
## Frameset.FrameDefaultUrl property

Ruft die URL der Webseite oder den Dateinamen des Dokuments ab oder legt diese fest, um sie in diesem Frame anzuzeigen.

```csharp
public string FrameDefaultUrl { get; set; }
```

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

* class [Frameset](../)
* namensraum [Aspose.Words.Framesets](../../../aspose.words.framesets/)
* Montage [Aspose.Words](../../../)
