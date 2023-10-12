---
title: Frameset.IsFrameLinkToFile
second_title: Aspose.Words for .NET API 参考
description: Frameset 财产. 获取或设置一个值该值指示 中指定的网页或文档文件名FrameDefaultUrl属性是框架所链接的外部资源
type: docs
weight: 40
url: /zh/net/aspose.words.framesets/frameset/isframelinktofile/
---
## Frameset.IsFrameLinkToFile property

获取或设置一个值，该值指示 中指定的网页或文档文件名[`FrameDefaultUrl`](../framedefaulturl/)属性是框架所链接的外部资源。

```csharp
public bool IsFrameLinkToFile { get; set; }
```

### 例子

展示如何访问页面上的框架。

```csharp
// 文档包含多个带有其他文档链接的框架。
Document doc = new Document(MyDir + "Frameset.docx");

// 我们可以检查默认 URL（网页 URL 或本地文档）或者框架是否是外部资源。
Assert.AreEqual("https://file-examples-com.github.io/uploads/2017/02/file-sample_100kB.docx",
    doc.Frameset.ChildFramesets[0].ChildFramesets[0].FrameDefaultUrl);
Assert.True(doc.Frameset.ChildFramesets[0].ChildFramesets[0].IsFrameLinkToFile);

Assert.AreEqual("Document.docx", doc.Frameset.ChildFramesets[1].FrameDefaultUrl);
Assert.False(doc.Frameset.ChildFramesets[1].IsFrameLinkToFile);

// 更改我们的框架之一的属性。
doc.Frameset.ChildFramesets[0].ChildFramesets[0].FrameDefaultUrl =
    "https://github.com/aspose-words/Aspose.Words-for-.NET/blob/master/Examples/Data/Absolute%20position%20tab.docx";
doc.Frameset.ChildFramesets[0].ChildFramesets[0].IsFrameLinkToFile = false;
```

### 也可以看看

* class [Frameset](../)
* 命名空间 [Aspose.Words.Framesets](../../frameset/)
* 部件 [Aspose.Words](../../../)


