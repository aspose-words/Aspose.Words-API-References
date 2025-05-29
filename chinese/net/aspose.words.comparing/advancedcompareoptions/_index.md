---
title: AdvancedCompareOptions Class
linktitle: AdvancedCompareOptions
articleTitle: AdvancedCompareOptions
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.AdvancedCompareOptions 类，实现强大的文档比较功能。自定义设置，获得精确的结果并提高工作效率。
type: docs
weight: 460
url: /zh/net/aspose.words.comparing/advancedcompareoptions/
---
## AdvancedCompareOptions class

允许设置高级比较选项。

```csharp
public class AdvancedCompareOptions
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [AdvancedCompareOptions](advancedcompareoptions/)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [IgnoreDmlUniqueId](../../aspose.words.comparing/advancedcompareoptions/ignoredmluniqueid/) { get; set; } | 指定是否忽略 DrawingML 唯一 ID 的差异。 |
| [IgnoreStoreItemId](../../aspose.words.comparing/advancedcompareoptions/ignorestoreitemid/) { get; set; } | 指定是否忽略 StructuredDocumentTag 存储项目 Id 中的差异。 |

## 评论

这些选项在 Microsoft Word 中没有等效选项，可能有助于产生更精确的比较结果。

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

* 命名空间 [Aspose.Words.Comparing](../../aspose.words.comparing/)
* 部件 [Aspose.Words](../../)
