---
title: Document.GetPageInfo
linktitle: GetPageInfo
articleTitle: GetPageInfo
second_title: Aspose.Words for .NET
description: 探索 GetPageInfo 方法来检索基本页面大小、方向和渲染详细信息，以优化打印和增强文档管理。
type: docs
weight: 650
url: /zh/net/aspose.words/document/getpageinfo/
---
## Document.GetPageInfo method

获取页面大小、方向和其他可能对打印或渲染有用的页面信息。

```csharp
public PageInfo GetPageInfo(int pageIndex)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| pageIndex | Int32 | 从 0 开始的页面索引。 |

## 例子

显示如何检查页面是否为彩色。

```csharp
Document doc = new Document(MyDir + "Document.docx");

// 检查文档的第一页是否没有彩色。
Assert.IsFalse(doc.GetPageInfo(0).Colored);
```

### 也可以看看

* class [PageInfo](../../../aspose.words.rendering/pageinfo/)
* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
