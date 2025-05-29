---
title: Document.UnlinkFields
linktitle: UnlinkFields
articleTitle: UnlinkFields
second_title: Aspose.Words for .NET
description: 了解如何使用 UnlinkFields 方法有效地取消整个文档中的字段链接，从而增强您的编辑工作流程。
type: docs
weight: 780
url: /zh/net/aspose.words/document/unlinkfields/
---
## Document.UnlinkFields method

取消整个文档中的字段链接。

```csharp
public void UnlinkFields()
```

## 评论

将整个文档中的所有字段替换为其最新结果。

要取消文档特定部分中的字段链接，请使用[`UnlinkFields`](../../range/unlinkfields/)。

## 例子

展示如何取消文档中所有字段的链接。

```csharp
Document doc = new Document(MyDir + "Linked fields.docx");

doc.UnlinkFields();
```

### 也可以看看

* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
