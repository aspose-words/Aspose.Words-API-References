---
title: ParagraphFormat
second_title: Aspose.Words for .NET API 参考
description: 获取样式的段落格式
type: docs
weight: 130
url: /zh/net/aspose.words/style/paragraphformat/
---
## Style.ParagraphFormat property

获取样式的段落格式。

```csharp
public ParagraphFormat ParagraphFormat { get; }
```

### 评论

对于字符和列表样式，此属性返回 null。

### 例子

展示如何使用列表格式创建和使用段落样式。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 创建自定义段落样式。
Style style = doc.Styles.Add(StyleType.Paragraph, "MyStyle1");
style.Font.Size = 24;
style.Font.Name = "Verdana";
style.ParagraphFormat.SpaceAfter = 12;

// 创建一个列表并确保使用此样式的段落将使用此列表。
style.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);
style.ListFormat.ListLevelNumber = 0;

// 将段落样式应用到文档构建器的当前段落，然后添加一些文本。
builder.ParagraphFormat.Style = style;
builder.Writeln("Hello World: MyStyle1, bulleted list.");

// 将文档构建器的样式更改为没有列表格式的样式并编写另一个段落。
builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Writeln("Hello World: Normal.");

builder.Document.Save(ArtifactsDir + "Styles.ParagraphStyleBulletedList.docx");
```

### 也可以看看

* class [ParagraphFormat](../../paragraphformat)
* class [Style](../../style)
* 命名空间 [Aspose.Words](../../style)
* 部件 [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->