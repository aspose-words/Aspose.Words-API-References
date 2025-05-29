---
title: Document.Frameset
linktitle: Frameset
articleTitle: Frameset
second_title: Aspose.Words for .NET
description: 探索文档的 Frameset 属性。获取 Frameset 实例，无缝集成框架页面。立即提升您的网络体验！
type: docs
weight: 170
url: /zh/net/aspose.words/document/frameset/
---
## Document.Frameset property

返回`Frameset`例如，如果此文档代表一个框架页面。

```csharp
public Frameset Frameset { get; }
```

## 评论

如果文档没有框架，则该属性具有`无效的`值.

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

* class [Frameset](../../../aspose.words.framesets/frameset/)
* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
