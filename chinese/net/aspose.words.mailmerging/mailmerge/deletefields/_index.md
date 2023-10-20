---
title: MailMerge.DeleteFields
linktitle: DeleteFields
articleTitle: DeleteFields
second_title: 用于 .NET 的 Aspose.Words
description: MailMerge DeleteFields 方法. 从文档中删除与邮件合并相关的字段 在 C#.
type: docs
weight: 170
url: /zh/net/aspose.words.mailmerging/mailmerge/deletefields/
---
## MailMerge.DeleteFields method

从文档中删除与邮件合并相关的字段。

```csharp
public void DeleteFields()
```

## 评论

此方法从文档中删除 MERGEFIELD 和 NEXT 字段。

如果您的邮件合并操作并不总是需要 来填充文档中的所有字段，则此方法可能很有用。使用此方法删除所有剩余的 邮件合并字段。

## 例子

显示如何从文档中删除所有 MERGEFIELD。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Dear ");
builder.InsertField(" MERGEFIELD FirstName ");
builder.Write(" ");
builder.InsertField(" MERGEFIELD LastName ");
builder.Writeln(",");
builder.Writeln("Greetings!");

Assert.AreEqual(
    "Dear \u0013 MERGEFIELD FirstName \u0014«FirstName»\u0015 \u0013 MERGEFIELD LastName \u0014«LastName»\u0015,\rGreetings!", 
    doc.GetText().Trim());

doc.MailMerge.DeleteFields();

Assert.AreEqual("Dear  ,\rGreetings!", doc.GetText().Trim());
```

### 也可以看看

* class [MailMerge](../)
* 命名空间 [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* 部件 [Aspose.Words](../../../)
