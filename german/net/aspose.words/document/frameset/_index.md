---
title: Document.Frameset
linktitle: Frameset
articleTitle: Frameset
second_title: Aspose.Words für .NET
description: Document Frameset eigendom. Gibt a zurückFramesetBeispiel wenn dieses Dokument eine FramesSeite darstellt in C#.
type: docs
weight: 160
url: /de/net/aspose.words/document/frameset/
---
## Document.Frameset property

Gibt a zurück`Frameset`Beispiel, wenn dieses Dokument eine Frames-Seite darstellt.

```csharp
public Frameset Frameset { get; }
```

## Bemerkungen

Wenn das Dokument nicht gerahmt ist, hat die Eigenschaft das`Null` value.

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

* class [Frameset](../../../aspose.words.framesets/frameset/)
* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
