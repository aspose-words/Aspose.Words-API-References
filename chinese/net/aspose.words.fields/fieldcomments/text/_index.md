---
title: FieldComments.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words for .NET
description: 使用 FieldComments Text 属性轻松管理您的评论 - 轻松获取或设置评论文本以增强用户交互。
type: docs
weight: 20
url: /zh/net/aspose.words.fields/fieldcomments/text/
---
## FieldComments.Text property

获取或设置评论的文本。

```csharp
public string Text { get; set; }
```

## 例子

展示如何使用 COMMENTS 字段。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 为文档的“评论”内置属性设置一个值。
doc.BuiltInDocumentProperties.Comments = "My comment.";

// 创建一个 COMMENTS 字段来显示该内置属性的值。
FieldComments field = (FieldComments)builder.InsertField(FieldType.FieldComments, true);
field.Update();

Assert.AreEqual(" COMMENTS ", field.GetFieldCode());
Assert.AreEqual("My comment.", field.Result);

// 如果我们给出 COMMENTS 字段的 Text 属性值并更新它，该字段将
// 用其 Text 属性的值覆盖“Comments”内置属性的当前值，
// 然后显示新值。
field.Text = "My overriding comment.";
field.Update();

Assert.AreEqual(" COMMENTS  \"My overriding comment.\"", field.GetFieldCode());
Assert.AreEqual("My overriding comment.", field.Result);

doc.Save(ArtifactsDir + "Field.COMMENTS.docx");
```

### 也可以看看

* class [FieldComments](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
