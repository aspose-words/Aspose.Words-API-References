---
title: FieldOptions.DefaultDocumentAuthor
linktitle: DefaultDocumentAuthor
articleTitle: DefaultDocumentAuthor
second_title: 用于 .NET 的 Aspose.Words
description: FieldOptions DefaultDocumentAuthor 财产. 获取或设置默认文档作者姓名如果内置文档属性中已指定作者姓名则 不考虑此选项 在 C#.
type: docs
weight: 70
url: /zh/net/aspose.words.fields/fieldoptions/defaultdocumentauthor/
---
## FieldOptions.DefaultDocumentAuthor property

获取或设置默认文档作者姓名。如果内置文档属性中已指定作者姓名，则 不考虑此选项。

```csharp
public string DefaultDocumentAuthor { get; set; }
```

## 例子

演示如何使用 AUTHOR 字段来显示文档创建者的姓名。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// AUTHOR 字段的结果来自名为“Author”的内置文档属性。
// 如果我们在 Microsoft Word 中创建并保存文档，
// 它将在该属性中包含我们的用户名。
// 但是，如果我们使用 Aspose.Words 以编程方式创建文档，
// 默认情况下，“Author”属性将为空字符串。
Assert.AreEqual(string.Empty, doc.BuiltInDocumentProperties.Author);

// 设置备用作者姓名供 AUTHOR 字段使用
// 如果“Author”属性包含空字符串。
doc.FieldOptions.DefaultDocumentAuthor = "Joe Bloggs";

builder.Write("This document was created by ");
FieldAuthor field = (FieldAuthor)builder.InsertField(FieldType.FieldAuthor, true);
field.Update();

Assert.AreEqual(" AUTHOR ", field.GetFieldCode());
Assert.AreEqual("Joe Bloggs", field.Result);

// 更新包含值的 AUTHOR 字段
// 将该值应用于“Author”内置属性。
Assert.AreEqual("Joe Bloggs", doc.BuiltInDocumentProperties.Author);

// 更改此属性，然后更新 AUTHOR 字段会将此值应用于该字段。
doc.BuiltInDocumentProperties.Author = "John Doe";      
field.Update();

Assert.AreEqual(" AUTHOR ", field.GetFieldCode());
Assert.AreEqual("John Doe", field.Result);

// 如果我们在更改“Name”属性后更新 AUTHOR 字段，
// 然后该字段将显示新名称并将新名称应用于内置属性。
field.AuthorName = "Jane Doe";
field.Update();

Assert.AreEqual(" AUTHOR  \"Jane Doe\"", field.GetFieldCode());
Assert.AreEqual("Jane Doe", field.Result);

// AUTHOR 字段不影响 DefaultDocumentAuthor 属性。
Assert.AreEqual("Jane Doe", doc.BuiltInDocumentProperties.Author);
Assert.AreEqual("Joe Bloggs", doc.FieldOptions.DefaultDocumentAuthor);

doc.Save(ArtifactsDir + "Field.AUTHOR.docx");
```

### 也可以看看

* class [FieldOptions](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
