---
title: MailMergeOptions.UseNonMergeFields
linktitle: UseNonMergeFields
articleTitle: UseNonMergeFields
second_title: Aspose.Words for .NET
description: 使用 UseNonMergeFields 属性解锁高级邮件合并功能。无缝集成 MERGEFIELD 和其他字段类型，增强文档自定义功能。
type: docs
weight: 130
url: /zh/net/aspose.words.lowcode/mailmergeoptions/usenonmergefields/
---
## MailMergeOptions.UseNonMergeFields property

当`真的`，指定除了 MERGEFIELD 字段之外，邮件合并还会执行到一些其他类型的字段中，并且还会执行到“{{fieldName}}”标签中。

```csharp
public bool UseNonMergeFields { get; set; }
```

## 评论

通常情况下，邮件合并仅对 MERGEFIELD 字段执行，但一些客户使用其他字段构建了 reporting ，并以此方式创建了许多文档。为了简化迁移过程（并且由于 this 方法已被多位客户独立使用），我们引入了邮件合并到其他字段的功能。

什么时候`UseNonMergeFields`设置为`真的`，Aspose.Words 将对以下字段执行邮件合并：

MERGEFIELD 字段名称

MACROBUTTON NOMACRO 字段名称

如果 0 = 0 "{FieldName}" ""

此外，当`UseNonMergeFields`设置为`真的`，Aspose.Words 将执行邮件合并到文本 tags "{{fieldName}}"。这些不是字段，只是文本标签。

### 也可以看看

* class [MailMergeOptions](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)
