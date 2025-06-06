---
title: FieldSubject.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words for .NET
description: 轻松管理 FieldSubject Text 属性 - 获取或设置主题文本，实现无缝数据处理和增强用户体验。
type: docs
weight: 20
url: /zh/net/aspose.words.fields/fieldsubject/text/
---
## FieldSubject.Text property

获取或设置主题的文本。

```csharp
public string Text { get; set; }
```

## 例子

显示如何使用 SUBJECT 字段。

```csharp
Document doc = new Document();

// 为文档的“主题”内置属性设置一个值。
doc.BuiltInDocumentProperties.Subject = "My subject";

// 创建一个 SUBJECT 字段来显示该内置属性的值。
DocumentBuilder builder = new DocumentBuilder(doc);
FieldSubject field = (FieldSubject)builder.InsertField(FieldType.FieldSubject, true);
field.Update();

Assert.AreEqual(" SUBJECT ", field.GetFieldCode());
Assert.AreEqual("My subject", field.Result);

// 如果我们给出 SUBJECT 字段的 Text 属性值并更新它，该字段将
// 用其 Text 属性的值覆盖“Subject”内置属性的当前值，
// 然后显示新值。
field.Text = "My new subject";
field.Update();

Assert.AreEqual(" SUBJECT  \"My new subject\"", field.GetFieldCode());
Assert.AreEqual("My new subject", field.Result);

Assert.AreEqual("My new subject", doc.BuiltInDocumentProperties.Subject);

doc.Save(ArtifactsDir + "Field.SUBJECT.docx");
```

### 也可以看看

* class [FieldSubject](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
