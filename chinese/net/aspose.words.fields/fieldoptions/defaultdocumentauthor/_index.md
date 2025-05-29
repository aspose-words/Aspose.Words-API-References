---
title: FieldOptions.DefaultDocumentAuthor
linktitle: DefaultDocumentAuthor
articleTitle: DefaultDocumentAuthor
second_title: Aspose.Words for .NET
description: 管理DefaultDocumentAuthor属性，轻松设置或更新文档作者的姓名，增强组织和文档管理效率。
type: docs
weight: 70
url: /zh/net/aspose.words.fields/fieldoptions/defaultdocumentauthor/
---
## FieldOptions.DefaultDocumentAuthor property

获取或设置默认文档作者的姓名。如果作者姓名已在内置文档属性中指定，则不考虑此选项。

```csharp
public string DefaultDocumentAuthor { get; set; }
```

## 例子

展示如何使用 AUTHOR 字段显示文档创建者的姓名。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// AUTHOR 字段从名为“Author”的内置文档属性中获取结果。
// 如果我们在 Microsoft Word 中创建并保存一个文档，
// 它将在该属性中包含我们的用户名。
// 但是，如果我们使用 Aspose.Words 以编程方式创建文档，
// 默认情况下，“Author”属性为空字符串。
Assert.AreEqual(string.Empty, doc.BuiltInDocumentProperties.Author);

// 设置 AUTHOR 字段使用的备份作者姓名
// 如果“Author”属性包含一个空字符串。
doc.FieldOptions.DefaultDocumentAuthor = "Joe Bloggs";

builder.Write("This document was created by ");
FieldAuthor field = (FieldAuthor)builder.InsertField(FieldType.FieldAuthor, true);
field.Update();

Assert.AreEqual(" AUTHOR ", field.GetFieldCode());
Assert.AreEqual("Joe Bloggs", field.Result);

// 更新包含值的 AUTHOR 字段
// 将该值应用于“Author”内置属性。
Assert.AreEqual("Joe Bloggs", doc.BuiltInDocumentProperties.Author);

// 更改此属性，然后更新 AUTHOR 字段将把此值应用到该字段。
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
