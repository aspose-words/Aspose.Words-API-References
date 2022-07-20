---
title: ExtractPages
second_title: Aspose.Words for .NET API 参考
description: 返回Documentaspose.words/document表示指定页面范围的对象
type: docs
weight: 580
url: /zh/net/aspose.words/document/extractpages/
---
## Document.ExtractPages method

返回[`Document`](../../document)表示指定页面范围的对象。

```csharp
public Document ExtractPages(int index, int count)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | Int32 | 要提取的第一页的从零开始的索引。 |
| count | Int32 | 要提取的页数。 |

### 评论

生成的文档应该看起来像 MS Word 中的文档，就像我们执行了“打印特定页面”一样 - 编号、 页眉/页脚和交叉表布局将被保留。 但由于存在大量细微差别，出现在减少页数的同时，完全匹配布局是一项安静而复杂的任务，需要付出很多努力。 根据文档的复杂性，生成的文档内容布局与源文档相比可能会略有不同。 任何反馈都会不胜感激。

### 例子

显示如何从文档中获取指定范围的页面。

```csharp
Document doc = new Document(MyDir + "Layout entities.docx");

doc = doc.ExtractPages(0, 2);

doc.Save(ArtifactsDir + "Document.ExtractPages.docx");
```

### 也可以看看

* class [Document](../../document)
* 命名空间 [Aspose.Words](../../document)
* 部件 [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->