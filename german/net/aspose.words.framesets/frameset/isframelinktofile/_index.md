---
title: Frameset.IsFrameLinkToFile
linktitle: IsFrameLinkToFile
articleTitle: IsFrameLinkToFile
second_title: Aspose.Words für .NET
description: Frameset IsFrameLinkToFile eigendom. Ruft einen Wert ab oder legt diesen fest der angibt ob der in the angegebene Webseiten oder Dokumentdateiname verwendet wird.FrameDefaultUrl Eigenschaft ist eine externe Ressource mit der der Frame verknüpft ist in C#.
type: docs
weight: 40
url: /de/net/aspose.words.framesets/frameset/isframelinktofile/
---
## Frameset.IsFrameLinkToFile property

Ruft einen Wert ab oder legt diesen fest, der angibt, ob der in the angegebene Webseiten- oder Dokumentdateiname verwendet wird.[`FrameDefaultUrl`](../framedefaulturl/) Eigenschaft ist eine externe Ressource, mit der der Frame verknüpft ist.

```csharp
public bool IsFrameLinkToFile { get; set; }
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
