---
title: FormField.RemoveField
linktitle: RemoveField
articleTitle: RemoveField
second_title: 用于 .NET 的 Aspose.Words
description: FormField RemoveField 方法. 删除整个表单字段而不仅仅是表单字段特殊字符 在 C#.
type: docs
weight: 240
url: /zh/net/aspose.words.fields/formfield/removefield/
---
## FormField.RemoveField method

删除整个表单字段，而不仅仅是表单字段特殊字符。

```csharp
public void RemoveField()
```

## 评论

如果存在与表单字段关联的书签，则不会删除该书签。

## 例子

展示如何删除表单字段。

```csharp
Document doc = new Document(MyDir + "Form fields.docx");

FormField formField = doc.Range.FormFields[3];
formField.RemoveField();
```

### 也可以看看

* class [FormField](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
