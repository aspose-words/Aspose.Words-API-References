---
title: Frameset Class
linktitle: Frameset
articleTitle: Frameset
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Framesets.Frameset 类，实现文档中框架的无缝管理。通过高效的框架集成增强您的网页效果！
type: docs
weight: 3510
url: /zh/net/aspose.words.framesets/frameset/
---
## Frameset class

表示框架页面或框架页面上的单个框架。

要了解更多信息，请访问[使用文档进行编程](https://docs.aspose.com/words/net/programming-with-documents/)文档文章。

```csharp
public class Frameset
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [Frameset](frameset/)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [ChildFramesets](../../aspose.words.framesets/frameset/childframesets/) { get; } | 获取子框架和框架页面的集合。 |
| [FrameDefaultUrl](../../aspose.words.framesets/frameset/framedefaulturl/) { get; set; } | 获取或设置在此框架中显示的网页 URL 或文档文件名。 |
| [IsFrameLinkToFile](../../aspose.words.framesets/frameset/isframelinktofile/) { get; set; } | 获取或设置一个值，指示是否在 中指定的网页或文档文件名[`FrameDefaultUrl`](./framedefaulturl/)属性是框架链接的外部资源。 |

## 评论

如果[`ChildFramesets`](./childframesets/)属性包含项目，则此实例是一个框架页面，否则它是 单个框架。

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

* 命名空间 [Aspose.Words.Framesets](../../aspose.words.framesets/)
* 部件 [Aspose.Words](../../)
