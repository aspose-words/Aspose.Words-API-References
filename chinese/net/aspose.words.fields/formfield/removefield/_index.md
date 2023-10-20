---
title: FormField.RemoveField
linktitle: RemoveField
articleTitle: RemoveField
second_title: 用于 .NET 的 Aspose.Words
description: FormField RemoveField 方法. 删除完整的表单域而不仅仅是表单域特殊字符 在 C#.
type: docs
weight: 240
url: /zh/net/aspose.words.fields/formfield/removefield/
---
## FormField.RemoveField method

删除完整的表单域，而不仅仅是表单域特殊字符。

```csharp
public void RemoveField()
```

## 评论

如果有与表单域相关的书签，则不会删除该书签。

## 例子

显示如何删除表单域。

```csharp
Document doc = new Document(MyDir + "Form fields.docx");

FormField formField = doc.Range.FormFields[3];
formField.RemoveField();
```

### 也可以看看

* class [FormField](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
