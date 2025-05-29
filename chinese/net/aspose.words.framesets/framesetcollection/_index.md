---
title: FramesetCollection Class
linktitle: FramesetCollection
articleTitle: FramesetCollection
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words FramesetCollection 类，这是您在文档处理中轻松管理多个 Frameset 实例的首选解决方案。
type: docs
weight: 3520
url: /zh/net/aspose.words.framesets/framesetcollection/
---
## FramesetCollection class

表示[`Frameset`](../frameset/)类.

要了解更多信息，请访问[使用文档进行编程](https://docs.aspose.com/words/net/programming-with-documents/)文档文章。

```csharp
public class FramesetCollection : IEnumerable<Frameset>
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [FramesetCollection](framesetcollection/)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Count](../../aspose.words.framesets/framesetcollection/count/) { get; } | 获取集合中包含的框架数或框架页面数。 |
| [Item](../../aspose.words.framesets/framesetcollection/item/) { get; } | 获取指定索引处的一个或多个框架页面。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [GetEnumerator](../../aspose.words.framesets/framesetcollection/getenumerator/)() | 返回遍历集合的枚举器。 |

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

* class [Frameset](../frameset/)
* 命名空间 [Aspose.Words.Framesets](../../aspose.words.framesets/)
* 部件 [Aspose.Words](../../)
