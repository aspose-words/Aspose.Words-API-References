---
title: FramesetCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words for .NET
description: Discover the FramesetCollection Count property, easily access the total number of frames in your collection for efficient web management.
type: docs
weight: 20
url: /net/aspose.words.framesets/framesetcollection/count/
---
## FramesetCollection.Count property

Gets the number of frames or frames pages contained in the collection.

```csharp
public int Count { get; }
```

## Examples

Shows how to access frames on-page.

```csharp
// Document contains several frames with links to other documents.
Document doc = new Document(MyDir + "Frameset.docx");

Assert.AreEqual(3, doc.Frameset.ChildFramesets.Count);
// We can check the default URL (a web page URL or local document) or if the frame is an external resource.
Assert.AreEqual("https://file-examples-com.github.io/uploads/2017/02/file-sample_100kB.docx",
    doc.Frameset.ChildFramesets[0].ChildFramesets[0].FrameDefaultUrl);
Assert.True(doc.Frameset.ChildFramesets[0].ChildFramesets[0].IsFrameLinkToFile);

Assert.AreEqual("Document.docx", doc.Frameset.ChildFramesets[1].FrameDefaultUrl);
Assert.False(doc.Frameset.ChildFramesets[1].IsFrameLinkToFile);

// Change properties for one of our frames.
doc.Frameset.ChildFramesets[0].ChildFramesets[0].FrameDefaultUrl =
    "https://github.com/aspose-words/Aspose.Words-for-.NET/blob/master/Examples/Data/Absolute%20position%20tab.docx";
doc.Frameset.ChildFramesets[0].ChildFramesets[0].IsFrameLinkToFile = false;
```

### See Also

* class [FramesetCollection](../)
* namespace [Aspose.Words.Framesets](../../../aspose.words.framesets/)
* assembly [Aspose.Words](../../../)
