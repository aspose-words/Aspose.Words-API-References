---
title: FieldStyleRef.SearchFromBottom
second_title: Aspose.Words for .NET API 参考
description: FieldStyleRef 财产. 获取或设置是否从当前页面底部搜索而不是从顶部搜索
type: docs
weight: 60
url: /zh/net/aspose.words.fields/fieldstyleref/searchfrombottom/
---
## FieldStyleRef.SearchFromBottom property

获取或设置是否从当前页面底部搜索，而不是从顶部搜索。

```csharp
public bool SearchFromBottom { get; set; }
```

### 例子

显示如何使用 STYLEREF 字段。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 使用 Microsoft Word 列表模板创建一个列表。
Aspose.Words.Lists.List list = doc.Lists.Add(Aspose.Words.Lists.ListTemplate.NumberDefault);

// 这个生成的列表将显示“1.a )”。
 // 括号前的空格是非分隔符，我们可以将其隐藏。
list.ListLevels[0].NumberFormat = "\x0000.";
list.ListLevels[1].NumberFormat = "\x0001 )";

// 添加文本并应用 STYLEREF 字段将引用的段落样式。
builder.ListFormat.List = list;
builder.ListFormat.ListIndent();
builder.ParagraphFormat.Style = doc.Styles["List Paragraph"];
builder.Writeln("Item 1");
builder.ParagraphFormat.Style = doc.Styles["Quote"];
builder.Writeln("Item 2");
builder.ParagraphFormat.Style = doc.Styles["List Paragraph"];
builder.Writeln("Item 3");
builder.ListFormat.RemoveNumbers();
builder.ParagraphFormat.Style = doc.Styles["Normal"];

// 在标题中放置一个 STYLEREF 字段，并在文档中显示第一个“列表段落”样式的文本。
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
FieldStyleRef field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "List Paragraph";

// 在页脚中放置一个 STYLEREF 字段，并让它显示最后的文本。
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "List Paragraph";
field.SearchFromBottom = true;

builder.MoveToDocumentEnd();

// 我们也可以使用 STYLEREF 字段来引用列表的列表编号。
builder.Write("\nParagraph number: ");
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "Quote";
field.InsertParagraphNumber = true;

builder.Write("\nParagraph number, relative context: ");
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "Quote";
field.InsertParagraphNumberInRelativeContext = true;

builder.Write("\nParagraph number, full context: ");
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "Quote";
field.InsertParagraphNumberInFullContext = true;

builder.Write("\nParagraph number, full context, non-delimiter chars suppressed: ");
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "Quote";
field.InsertParagraphNumberInFullContext = true;
field.SuppressNonDelimiters = true;

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.STYLEREF.docx");
```

### 也可以看看

* class [FieldStyleRef](../)
* 命名空间 [Aspose.Words.Fields](../../fieldstyleref/)
* 部件 [Aspose.Words](../../../)


