---
title: FramesetCollection Class
linktitle: FramesetCollection
articleTitle: FramesetCollection
second_title: Aspose.Words for .NET
description: Aspose.Words.Framesets.FramesetCollection class. Represents a collection of instances of the Frameset class in C#.
type: docs
weight: 3350
url: /net/aspose.words.framesets/framesetcollection/
---
## FramesetCollection class

Represents a collection of instances of the [`Frameset`](../frameset/) class.

To learn more, visit the [Programming with Documents](https://docs.aspose.com/words/net/programming-with-documents/) documentation article.

```csharp
public class FramesetCollection : IEnumerable<Frameset>
```

## Constructors

| Name | Description |
| --- | --- |
| [FramesetCollection](framesetcollection/)() | The default constructor. |

## Properties

| Name | Description |
| --- | --- |
| [Count](../../aspose.words.framesets/framesetcollection/count/) { get; } | Gets the number of frames or frames pages contained in the collection. |
| [Item](../../aspose.words.framesets/framesetcollection/item/) { get; } | Gets a frame or frames page at the specified index. |

## Methods

| Name | Description |
| --- | --- |
| [GetEnumerator](../../aspose.words.framesets/framesetcollection/getenumerator/)() | Returns an enumerator that iterates through the collection. |

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

* class [Frameset](../frameset/)
* namespace [Aspose.Words.Framesets](../../aspose.words.framesets/)
* assembly [Aspose.Words](../../)
