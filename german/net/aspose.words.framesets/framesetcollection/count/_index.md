---
title: FramesetCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „FramesetCollection Count“ und greifen Sie für eine effiziente Webverwaltung einfach auf die Gesamtzahl der Frames in Ihrer Sammlung zu.
type: docs
weight: 20
url: /de/net/aspose.words.framesets/framesetcollection/count/
---
## FramesetCollection.Count property

Ruft die Anzahl der in der Sammlung enthaltenen Frames oder Frameseiten ab.

```csharp
public int Count { get; }
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

* class [FramesetCollection](../)
* namensraum [Aspose.Words.Framesets](../../../aspose.words.framesets/)
* Montage [Aspose.Words](../../../)
