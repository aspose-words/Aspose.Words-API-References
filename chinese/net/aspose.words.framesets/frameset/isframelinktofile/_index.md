---
title: Frameset.IsFrameLinkToFile
linktitle: IsFrameLinkToFile
articleTitle: IsFrameLinkToFile
second_title: 用于 .NET 的 Aspose.Words
description: Frameset IsFrameLinkToFile 财产. 获取或设置一个值该值指示是否在 中指定的网页或文档文件名FrameDefaultUrl属性是框架链接的外部资源 在 C#.
type: docs
weight: 40
url: /zh/net/aspose.words.framesets/frameset/isframelinktofile/
---
## Frameset.IsFrameLinkToFile property

获取或设置一个值，该值指示是否在 中指定的网页或文档文件名[`FrameDefaultUrl`](../framedefaulturl/)属性是框架链接的外部资源。

```csharp
public bool IsFrameLinkToFile { get; set; }
```

## 例子

显示如何访问页面上的框架。

```csharp
// 文档包含多个带有指向其他文档的链接的框架。
Document doc = new Document(MyDir + "Frameset.docx");

// 我们可以检查默认 URL（网页 URL 或本地文档）或者框架是否是外部资源。
Assert.AreEqual("https://file-examples-com.github.io/uploads/2017/02/file-sample_100kB.docx",
    doc.Frameset.ChildFramesets[0].ChildFramesets[0].FrameDefaultUrl);
Assert.True(doc.Frameset.ChildFramesets[0].ChildFramesets[0].IsFrameLinkToFile);

Assert.AreEqual("Document.docx", doc.Frameset.ChildFramesets[1].FrameDefaultUrl);
Assert.False(doc.Frameset.ChildFramesets[1].IsFrameLinkToFile);

// 更改我们其中一个框架的属性。
doc.Frameset.ChildFramesets[0].ChildFramesets[0].FrameDefaultUrl =
    "https://github.com/aspose-words/Aspose.Words-for-.NET/blob/master/Examples/Data/Absolute%20position%20tab.docx";
doc.Frameset.ChildFramesets[0].ChildFramesets[0].IsFrameLinkToFile = false;
```

### 也可以看看

* class [Frameset](../)
* 命名空间 [Aspose.Words.Framesets](../../../aspose.words.framesets/)
* 部件 [Aspose.Words](../../../)
