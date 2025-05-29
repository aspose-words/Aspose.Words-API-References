---
title: Document.UpdateFields
linktitle: UpdateFields
articleTitle: UpdateFields
second_title: Aspose.Words for .NET
description: 使用 UpdateFields 方法修改您的文档 - 有效刷新所有字段值以增强准确性和无缝编辑。
type: docs
weight: 810
url: /zh/net/aspose.words/document/updatefields/
---
## Document.UpdateFields method

更新整个文档中字段的值。

```csharp
public void UpdateFields()
```

## 评论

当您打开、修改然后保存文档时，Aspose.Words 不会自动更新字段，而是保持它们完好无损。 因此，如果您以编程方式修改了文档 并希望确保正确（计算）的字段值出现在保存的文档中，则通常需要在保存之前调用此方法。

执行邮件合并后无需更新字段，因为邮件合并是一种字段 update ，会自动更新文档中的所有字段。

此方法不会更新所有字段类型。有关受支持的字段类型的详细列表，请参阅《程序员指南》。

此方法不会更新与页面布局算法相关的字段（例如 PAGE、PAGES、PAGEREF）。 当您呈现文档或调用时，页面布局相关的字段会更新[`UpdatePageLayout`](../updatepagelayout/)。

使用[`NormalizeFieldTypes`](../normalizefieldtypes/)如果文档更改影响了字段类型，则在字段更新之前使用方法。

要更新文档特定部分中的字段，请使用[`UpdateFields`](../../range/updatefields/)。

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
// 每次我们使用 Microsoft Word 打开文档时，DATE 字段都会将其值更新为当前日期。
// 像这样将 DATE 字段嵌套在 QUOTE 字段中将冻结其值
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

展示如何设置用户详细信息并使用字段显示它们。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 创建一个 UserInformation 对象并将其设置为显示用户信息字段的数据源。
UserInformation userInformation = new UserInformation
{
    Name = "John Doe",
    Initials = "J. D.",
    Address = "123 Main Street"
};
doc.FieldOptions.CurrentUser = userInformation;

// 插入 USERNAME、USERINITIALS 和 USERADDRESS 字段，显示以下值
// 我们上面创建的 UserInformation 对象的各个属性。
Assert.AreEqual(userInformation.Name, builder.InsertField(" USERNAME ").Result);
Assert.AreEqual(userInformation.Initials, builder.InsertField(" USERINITIALS ").Result);
Assert.AreEqual(userInformation.Address, builder.InsertField(" USERADDRESS ").Result);

// 字段选项对象还具有静态默认用户，所有文档中的字段都可以引用。
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

展示如何使用标题样式作为条目将目录 (TOC) 插入到文档中。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入文档第一页的目录。
// 配置表格以选取标题级别为 1 至 3 的段落。
// 另外，将其条目设置为超链接，以便
// 在 Microsoft Word 中单击鼠标左键时移动到标题的位置。
builder.InsertTableOfContents("\\o \"1-3\" \\h \\z \\u");
builder.InsertBreak(BreakType.PageBreak);

// 通过添加具有标题样式的段落来填充目录。
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

// 目录是一种需要更新以显示最新结果的字段。
doc.UpdateFields();
doc.Save(ArtifactsDir + "DocumentBuilder.InsertToc.docx");
```

### 也可以看看

* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
