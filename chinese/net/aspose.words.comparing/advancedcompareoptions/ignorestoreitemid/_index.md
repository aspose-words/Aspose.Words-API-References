---
title: AdvancedCompareOptions.IgnoreStoreItemId
linktitle: IgnoreStoreItemId
articleTitle: IgnoreStoreItemId
second_title: Aspose.Words for .NET
description: 了解 AdvancedCompareOptions IgnoreStoreItemId 属性如何通过忽略 StructuredDocumentTag ID 差异来增强文档比较，从而提高准确性。
type: docs
weight: 30
url: /zh/net/aspose.words.comparing/advancedcompareoptions/ignorestoreitemid/
---
## AdvancedCompareOptions.IgnoreStoreItemId property

指定是否忽略 StructuredDocumentTag 存储项目 Id 中的差异。

```csharp
public bool IgnoreStoreItemId { get; set; }
```

## 评论

默认值为`错误的`.

## 例子

展示如何比较内容相同但商店商品 ID 不同的 SDT。

```csharp
Document docA = new Document(MyDir + "Document with SDT 1.docx");
Document docB = new Document(MyDir + "Document with SDT 2.docx");

// 配置选项以比较具有相同内容但不同商店商品 ID 的 SDT。
CompareOptions compareOptions = new CompareOptions();
compareOptions.AdvancedOptions.IgnoreStoreItemId = false;

docA.Compare(docB, "user", DateTime.Now, compareOptions);
Assert.AreEqual(8, docA.Revisions.Count);

compareOptions.AdvancedOptions.IgnoreStoreItemId = true;

docA.Revisions.RejectAll();
docA.Compare(docB, "user", DateTime.Now, compareOptions);
Assert.AreEqual(0, docA.Revisions.Count);
```

### 也可以看看

* class [AdvancedCompareOptions](../)
* 命名空间 [Aspose.Words.Comparing](../../../aspose.words.comparing/)
* 部件 [Aspose.Words](../../../)
