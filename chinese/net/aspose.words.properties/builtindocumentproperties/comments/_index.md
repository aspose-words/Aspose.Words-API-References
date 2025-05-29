---
title: BuiltInDocumentProperties.Comments
linktitle: Comments
articleTitle: Comments
second_title: Aspose.Words for .NET
description: 使用 BuiltInDocumentProperties 轻松管理文档注释。轻松获取或设置注释，增强协作，提升清晰度。
type: docs
weight: 60
url: /zh/net/aspose.words.properties/builtindocumentproperties/comments/
---
## BuiltInDocumentProperties.Comments property

获取或设置文档注释。

```csharp
public string Comments { get; set; }
```

## 例子

展示如何使用“描述”类别中的内置文档属性。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;

// 下面是四个内置文档属性，它们具有可以在文档正文中显示其值的字段。
// 1 - “作者”属性，我们可以使用 AUTHOR 字段显示：
properties.Author = "John Doe";
builder.Write("Author:\t");
builder.InsertField(FieldType.FieldAuthor, true);

// 2 - “标题”属性，我们可以使用 TITLE 字段显示它：
properties.Title = "John's Document";
builder.Write("\nDoc title:\t");
builder.InsertField(FieldType.FieldTitle, true);

// 3 - “主题”属性，我们可以使用 SUBJECT 字段显示：
properties.Subject = "My subject";
builder.Write("\nSubject:\t");
builder.InsertField(FieldType.FieldSubject, true);

// 4 - “评论”属性，我们可以使用评论字段显示它：
properties.Comments = $"This is {properties.Author}'s document about {properties.Subject}";
builder.Write("\nComments:\t\"");
builder.InsertField(FieldType.FieldComments, true);
builder.Write("\"");

// “Category”内置属性没有可以显示其值的字段。
properties.Category = "My category";

// 我们可以通过用分号分隔“Keywords”属性的字符串值为文档设置多个关键字。
properties.Keywords = "Tag 1; Tag 2; Tag 3";

// 我们可以在 Windows 资源管理器中右键单击该文档，然后在“属性”->“详细信息”中找到这些属性。
// “Author”内置属性位于“Origin”组中，其他属性位于“Description”组中。
doc.Save(ArtifactsDir + "DocumentProperties.Description.docx");
```

### 也可以看看

* class [BuiltInDocumentProperties](../)
* 命名空间 [Aspose.Words.Properties](../../../aspose.words.properties/)
* 部件 [Aspose.Words](../../../)
