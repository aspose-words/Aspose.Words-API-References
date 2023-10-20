---
title: FieldTitle.Text
linktitle: Text
articleTitle: Text
second_title: 用于 .NET 的 Aspose.Words
description: FieldTitle Text 财产. 获取或设置标题文本 在 C#.
type: docs
weight: 20
url: /zh/net/aspose.words.fields/fieldtitle/text/
---
## FieldTitle.Text property

获取或设置标题文本。

```csharp
public string Text { get; set; }
```

## 例子

展示如何使用 TITLE 字段。

```csharp
Document doc = new Document();

 // 为“Title”内置文档属性设置一个值。
doc.BuiltInDocumentProperties.Title = "My Title";

// 我们可以使用 TITLE 字段在文档中显示该属性的值。
DocumentBuilder builder = new DocumentBuilder(doc);
FieldTitle field = (FieldTitle)builder.InsertField(FieldType.FieldTitle, false);
field.Update();

Assert.AreEqual(" TITLE ", field.GetFieldCode());
Assert.AreEqual("My Title", field.Result);

// 设置字段的 Text 属性的值，
// 然后更新字段也会用新值覆盖相应的内置属性。
builder.Writeln();
field = (FieldTitle)builder.InsertField(FieldType.FieldTitle, false);
field.Text = "My New Title";
field.Update();

Assert.AreEqual(" TITLE  \"My New Title\"", field.GetFieldCode());
Assert.AreEqual("My New Title", field.Result);
Assert.AreEqual("My New Title", doc.BuiltInDocumentProperties.Title);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.TITLE.docx");
```

### 也可以看看

* class [FieldTitle](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
