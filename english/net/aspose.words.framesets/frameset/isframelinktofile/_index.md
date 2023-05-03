---
title: Frameset.IsFrameLinkToFile
linktitle: IsFrameLinkToFile
second_title: Aspose.Words for .NET API Reference
description: Frameset IsFrameLinkToFile property. Gets or sets a value indicating whether the web page or document file name specified in the FrameDefaultUrl property is an external resource the frame is linked with in C#.
type: docs
weight: 40
url: /net/aspose.words.framesets/frameset/isframelinktofile/
---
## Frameset.IsFrameLinkToFile property

Gets or sets a value indicating whether the web page or document file name specified in the [`FrameDefaultUrl`](../framedefaulturl/) property is an external resource the frame is linked with.

```csharp
public bool IsFrameLinkToFile { get; set; }
```

## Examples

Shows how to access frames on-page.

```csharp
// Document contains several frames with links to other documents.
Document doc = new Document(MyDir + "Frameset.docx");

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

* class [Frameset](../)
* namespace [Aspose.Words.Framesets](../../frameset/)
* assembly [Aspose.Words](../../../)
