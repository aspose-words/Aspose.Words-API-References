---
title: FramesetCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words for .NET
description: 发现 FramesetCollection Count 属性，轻松访问集合中的总帧数，实现高效的网络管理。
type: docs
weight: 20
url: /zh/net/aspose.words.framesets/framesetcollection/count/
---
## FramesetCollection.Count property

获取集合中包含的框架数或框架页面数。

```csharp
public int Count { get; }
```

## 例子

显示如何访问页面上的框架。

```csharp
// 文档包含几个带有指向其他文档的链接的框架。
Document doc = new Document(MyDir + "Frameset.docx");

Assert.AreEqual(3, doc.Frameset.ChildFramesets.Count);
// 我们可以检查默认 URL（网页 URL 或本地文档）或者框架是否是外部资源。
Assert.AreEqual("https://file-examples-com.github.io/uploads/2017/02/file-sample_100kB.docx",
    doc.Frameset.ChildFramesets[0].ChildFramesets[0].FrameDefaultUrl);
Assert.True(doc.Frameset.ChildFramesets[0].ChildFramesets[0].IsFrameLinkToFile);

Assert.AreEqual("Document.docx", doc.Frameset.ChildFramesets[1].FrameDefaultUrl);
Assert.False(doc.Frameset.ChildFramesets[1].IsFrameLinkToFile);

// 更改其中一个框架的属性。
doc.Frameset.ChildFramesets[0].ChildFramesets[0].FrameDefaultUrl =
    "https://github.com/aspose-words/Aspose.Words-for-.NET/blob/master/Examples/Data/Absolute%20position%20tab.docx”；
doc.Frameset.ChildFramesets[0].ChildFramesets[0].IsFrameLinkToFile = false;
```

### 也可以看看

* class [FramesetCollection](../)
* 命名空间 [Aspose.Words.Framesets](../../../aspose.words.framesets/)
* 部件 [Aspose.Words](../../../)
