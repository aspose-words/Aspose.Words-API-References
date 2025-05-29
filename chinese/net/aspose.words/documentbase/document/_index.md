---
title: DocumentBase.Document
linktitle: Document
articleTitle: Document
second_title: Aspose.Words for .NET
description: 探索 DocumentBase 属性，高效管理您的文档。立即解锁无缝访问，提升您的工作流程！
type: docs
weight: 20
url: /zh/net/aspose.words/documentbase/document/
---
## DocumentBase.Document property

获取此实例。

```csharp
public override DocumentBase Document { get; }
```

## 例子

展示如何创建简单文档。

```csharp
Document doc = new Document();

// 默认情况下，新的 Document 对象带有最小的节点集
// 需要开始添加内容，例如文本和形状：一个部分、一个正文和一个段落。
doc.AppendChild(new Section(doc))
    .AppendChild(new Body(doc))
    .AppendChild(new Paragraph(doc))
    .AppendChild(new Run(doc, "Hello world!"));
```

### 也可以看看

* class [DocumentBase](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
