---
title: Document.UpdateFields
linktitle: UpdateFields
articleTitle: UpdateFields
second_title: 用于 .NET 的 Aspose.Words
description: Document UpdateFields 方法. 更新整个文档中的字段值 在 C#.
type: docs
weight: 750
url: /zh/net/aspose.words/document/updatefields/
---
## Document.UpdateFields method

更新整个文档中的字段值。

```csharp
public void UpdateFields()
```

## 评论

当您打开、修改和保存文档时，Aspose.Words 不会自动更新字段，它会保持原样。 因此，如果您以编程方式修改了 document ，通常需要在保存之前调用此方法并确保正确的（计算的）字段值出现在保存的文档中。

执行邮件合并后不需要更新字段，因为邮件合并是一种字段 update 并自动更新文档中的所有字段。

此方法不会更新所有字段类型。有关支持的字段类型的详细列表，请参阅程序员指南。

此方法不会更新与页面布局算法相关的字段（例如 PAGE、PAGES、PAGEREF）。 渲染文档或调用时更新与页面布局相关的字段[`UpdatePageLayout`](../updatepagelayout/).

使用[`NormalizeFieldTypes`](../normalizefieldtypes/)如果存在影响字段类型的文档更改，则字段更新之前的方法。

要更新文档特定部分中的字段，请使用[`UpdateFields`](../../range/updatefields/).

## 例子

显示使用 QUOTE 字段。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入一个 QUOTE 字段，它将显示其 Text 属性的值。
FieldQuote field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
field.Text = "\"Quoted text\"";

Assert.AreEqual(" QUOTE  \"\\\"Quoted text\\\"\"", field.GetFieldCode());

// 插入一个 QUOTE 字段并在其中嵌套一个 DATE 字段。
// 每次我们使用 Microsoft Word 打开文档时，DATE 字段的值都会更新为当前日期。
// 像这样在 QUOTE 字段中嵌套 DATE 字段将冻结其值
// 到我们创建文档的日期。
builder.Write("\nDocument creation date: ");
field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
builder.MoveTo(field.Separator);
builder.InsertField(FieldType.FieldDate, true);

Assert.AreEqual(" QUOTE \u0013 DATE \u0014" + DateTime.Now.Date.ToShortDateString() + "\u0015", field.GetFieldCode());

// 更新所有字段以显示其正确结果。
doc.UpdateFields();

Assert.AreEqual("\"Quoted text\"", doc.Range.Fields[0].Result);

doc.Save(ArtifactsDir + "Field.QUOTE.docx");
```

显示如何设置用户详细信息，并使用字段显示它们。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 创建一个 UserInformation 对象，并将其设置为显示用户信息的字段的数据源。
UserInformation userInformation = new UserInformation
{
    Name = "John Doe",
    Initials = "J. D.",
    Address = "123 Main Street"
};
doc.FieldOptions.CurrentUser = userInformation;

// 插入 USERNAME、USERINITIALS 和 USERADDRESS 字段，它们显示的值
// 我们在上面创建的 UserInformation 对象的各个属性。 
Assert.AreEqual(userInformation.Name, builder.InsertField(" USERNAME ").Result);
Assert.AreEqual(userInformation.Initials, builder.InsertField(" USERINITIALS ").Result);
Assert.AreEqual(userInformation.Address, builder.InsertField(" USERADDRESS ").Result);

// 字段选项对象还有一个静态默认用户，所有文档的字段都可以引用。
UserInformation.DefaultUser.Name = "Default User";
UserInformation.DefaultUser.Initials = "D. U.";
UserInformation.DefaultUser.Address = "One Microsoft Way";
doc.FieldOptions.CurrentUser = UserInformation.DefaultUser;

Assert.AreEqual("Default User", builder.InsertField(" USERNAME ").Result);
Assert.AreEqual("D. U.", builder.InsertField(" USERINITIALS ").Result);
Assert.AreEqual("One Microsoft Way", builder.InsertField(" USERADDRESS ").Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + "FieldOptions.CurrentUser.docx");
```

演示如何使用标题样式作为条目将目录 (TOC) 插入到文档中。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 为文档的第一页插入目录。
// 配置表格以拾取具有 1 到 3 级标题的段落。
// 此外，将其条目设置为将带我们的超链接
// 在 Microsoft Word 中左键单击时指向标题的位置。
builder.InsertTableOfContents("\\o \"1-3\" \\h \\z \\u");
builder.InsertBreak(BreakType.PageBreak);

// 通过添加带有标题样式的段落来填充目录。
// 每个级别在 1 到 3 之间的标题都会在表中创建一个条目。
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("Heading 2");
builder.Writeln("Heading 3");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 3.1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;
builder.Writeln("Heading 3.1.1");
builder.Writeln("Heading 3.1.2");
builder.Writeln("Heading 3.1.3");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading4;
builder.Writeln("Heading 3.1.3.1");
builder.Writeln("Heading 3.1.3.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 3.2");
builder.Writeln("Heading 3.3");

// 目录是需要更新以显示最新结果的类型的字段。
doc.UpdateFields();
doc.Save(ArtifactsDir + "DocumentBuilder.InsertToc.docx");
```

### 也可以看看

* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
