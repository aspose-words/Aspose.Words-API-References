---
title: FramesetCollection Class
linktitle: FramesetCollection
articleTitle: FramesetCollection
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words FramesetCollection class, your go-to solution for managing multiple Frameset instances effortlessly in document processing.
type: docs
weight: 3510
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

* class [Frameset](../frameset/)
* namespace [Aspose.Words.Framesets](../../aspose.words.framesets/)
* assembly [Aspose.Words](../../)
