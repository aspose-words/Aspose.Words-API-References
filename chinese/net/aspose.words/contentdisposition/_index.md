---
title: ContentDisposition Enum
linktitle: ContentDisposition
articleTitle: ContentDisposition
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.ContentDisposition 枚举. 枚举在客户端浏览器上呈现文档的不同方式 在 C#.
type: docs
weight: 340
url: /zh/net/aspose.words/contentdisposition/
---
## ContentDisposition enumeration

枚举在客户端浏览器上呈现文档的不同方式。

```csharp
public enum ContentDisposition
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Attachment | `0` | 将文档发送到浏览器，并提供将文档保存到磁盘或在与文档扩展名关联的应用程序 中打开的选项。 |
| Inline | `1` | 将文档发送到浏览器并提供将文档保存到磁盘或在浏览器中打开的选项。 |

## 评论

请注意，客户端浏览器上的实际行为可能会受到浏览器安全配置的影响。

## 例子

演示如何执行邮件合并，然后将文档保存到客户端浏览器。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" MERGEFIELD FullName ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD Company ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD Address ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD City ");

doc.MailMerge.Execute(new string[] { "FullName", "Company", "Address", "City" },
    new object[] { "James Bond", "MI5 Headquarters", "Milbank", "London" });

// 将文档发送到客户端浏览器。
Assert.That(() => doc.Save(response, "Artifacts/MailMerge.ExecuteArray.docx", ContentDisposition.Inline, null),
    Throws.TypeOf<ArgumentNullException>()); //由于测试中HttpResponse为null而抛出。

// 我们需要手动关闭此响应，以确保保存后不会向文档添加任何多余的内容。
Assert.That(() => response.End(), Throws.TypeOf<NullReferenceException>());
```

### 也可以看看

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
