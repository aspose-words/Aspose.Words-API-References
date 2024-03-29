---
title: Document.ExtractPages
linktitle: ExtractPages
articleTitle: ExtractPages
second_title: 用于 .NET 的 Aspose.Words
description: Document ExtractPages 方法. 返回Document代表指定页面范围的对象 在 C#.
type: docs
weight: 600
url: /zh/net/aspose.words/document/extractpages/
---
## Document.ExtractPages method

返回[`Document`](../)代表指定页面范围的对象。

```csharp
public Document ExtractPages(int index, int count)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | Int32 | 要提取的第一页的从零开始的索引。 |
| count | Int32 | 要提取的页数。 |

## 评论

生成的文档应该看起来像 MS Word 中的文档，就好像我们执行了“打印特定页面”一样 – 编号、 页眉/页脚和交叉表布局将被保留。 但由于存在大量细微差别，出现在减少页数的同时，布局的完全匹配是一项安静而复杂的任务，需要付出大量努力。 根据文档的复杂性，与源文档相比，生成的文档内容布局可能会略有不同。 任何反馈都会不胜感激。

## 例子

演示如何从文档中获取指定范围的页面。

```csharp
Document doc = new Document(MyDir + "Layout entities.docx");

doc = doc.ExtractPages(0, 2);

doc.Save(ArtifactsDir + "Document.ExtractPages.docx");
```

### 也可以看看

* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
