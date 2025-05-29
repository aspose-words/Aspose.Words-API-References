---
title: MailMerge.TrimWhitespaces
linktitle: TrimWhitespaces
articleTitle: TrimWhitespaces
second_title: Aspose.Words for .NET
description: 使用 TrimWhitespaces 属性优化您的邮件合并过程，通过删除前导和尾随空格来确保数据干净，从而获得准确的结果。
type: docs
weight: 130
url: /zh/net/aspose.words.mailmerging/mailmerge/trimwhitespaces/
---
## MailMerge.TrimWhitespaces property

获取或设置一个值，指示是否从邮件合并值中删除尾随和前导空格。

```csharp
public bool TrimWhitespaces { get; set; }
```

## 评论

默认值为`真的`.

## 例子

展示如何在执行邮件合并时修剪数据源值中的空格。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField("MERGEFIELD myMergeField", null);

doc.MailMerge.TrimWhitespaces = trimWhitespaces;
doc.MailMerge.Execute(new[] { "myMergeField" }, new object[] { "\t hello world! " });

Assert.AreEqual(trimWhitespaces ? "hello world!\f" : "\t hello world! \f", doc.GetText());
```

### 也可以看看

* class [MailMerge](../)
* 命名空间 [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* 部件 [Aspose.Words](../../../)
