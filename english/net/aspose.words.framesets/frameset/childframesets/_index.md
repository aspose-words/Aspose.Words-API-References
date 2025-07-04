---
title: Frameset.ChildFramesets
linktitle: ChildFramesets
articleTitle: ChildFramesets
second_title: Aspose.Words for .NET
description: Discover the Frameset ChildFramesets property to easily access and manage collections of child frames and pages for enhanced web design.
type: docs
weight: 20
url: /net/aspose.words.framesets/frameset/childframesets/
---
## Frameset.ChildFramesets property

Gets the collection of child frames and frames pages.

```csharp
public FramesetCollection ChildFramesets { get; }
```

## Examples

Shows how to access frames on-page.

```csharp
// Document contains several frames with links to other documents.
Document doc = new Document(MyDir + "Frameset.docx");

Assert.That(doc.Frameset.ChildFramesets.Count, Is.EqualTo(3));
// We can check the default URL (a web page URL or local document) or if the frame is an external resource.
Assert.That(doc.Frameset.ChildFramesets[0].ChildFramesets[0].FrameDefaultUrl, Is.EqualTo("https://file-examples-com.github.io/uploads/2017/02/file-sample_100kB.docx"));
Assert.That(doc.Frameset.ChildFramesets[0].ChildFramesets[0].IsFrameLinkToFile, Is.True);

Assert.That(doc.Frameset.ChildFramesets[1].FrameDefaultUrl, Is.EqualTo("Document.docx"));
Assert.That(doc.Frameset.ChildFramesets[1].IsFrameLinkToFile, Is.False);

// Change properties for one of our frames.
doc.Frameset.ChildFramesets[0].ChildFramesets[0].FrameDefaultUrl =
    "https://github.com/aspose-words/Aspose.Words-for-.NET/blob/master/Examples/Data/Absolute%20position%20tab.docx";
doc.Frameset.ChildFramesets[0].ChildFramesets[0].IsFrameLinkToFile = false;
```

### See Also

* class [FramesetCollection](../../framesetcollection/)
* class [Frameset](../)
* namespace [Aspose.Words.Framesets](../../../aspose.words.framesets/)
* assembly [Aspose.Words](../../../)
