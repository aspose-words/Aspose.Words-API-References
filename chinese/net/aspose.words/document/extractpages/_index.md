---
title: Document.ExtractPages
linktitle: ExtractPages
articleTitle: ExtractPages
second_title: Aspose.Words for .NET
description: 发现 Document ExtractPages 方法可以轻松检索特定页面范围，从而增强文档管理和效率。
type: docs
weight: 640
url: /zh/net/aspose.words/document/extractpages/
---
## Document.ExtractPages method

返回[`Document`](../)表示指定页面范围的对象。

```csharp
public Document ExtractPages(int index, int count)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | Int32 | 要提取的第一页的从零开始的索引。 |
| count | Int32 | 要提取的页数。 |

## 评论

生成的文档应该看起来像 MS Word 中的文档，就像我们执行了“打印特定页面”一样 - 编号、 页眉/页脚和交叉表布局将被保留。 但由于在减少页数的同时出现了大量细微差别，布局的完全匹配是一项相当复杂的任务，需要付出很多努力。 根据文档的复杂程度，生成的文档内容布局与源文档可能会有细微的差别。 如有任何反馈，我们将不胜感激。

## 例子

显示如何从文档中获取指定范围的页面。

```csharp
Document doc = new Document(MyDir + "Layout entities.docx");

doc = doc.ExtractPages(0, 2);

doc.Save(ArtifactsDir + "Document.ExtractPages.docx");
```

### 也可以看看

* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
