---
title: Document.Frameset
linktitle: Frameset
articleTitle: Frameset
second_title: Aspose.Words für .NET
description: Entdecken Sie die Frameset-Eigenschaft für Dokumente. Holen Sie sich eine Frameset-Instanz für die nahtlose Integration von Frame-Seiten. Verbessern Sie Ihr Web-Erlebnis noch heute!
type: docs
weight: 170
url: /de/net/aspose.words/document/frameset/
---
## Document.Frameset property

Gibt einen`Frameset` Instanz, wenn dieses Dokument eine Frames-Seite darstellt.

```csharp
public Frameset Frameset { get; }
```

## Bemerkungen

Wenn das Dokument nicht gerahmt ist, hat die Eigenschaft die`null` Wert.

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

* class [Frameset](../../../aspose.words.framesets/frameset/)
* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
