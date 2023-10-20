---
title: Style.ListFormat
linktitle: ListFormat
articleTitle: ListFormat
second_title: 用于 .NET 的 Aspose.Words
description: Style ListFormat 财产. 提供对段落样式的列表格式属性的访问 在 C#.
type: docs
weight: 110
url: /zh/net/aspose.words/style/listformat/
---
## Style.ListFormat property

提供对段落样式的列表格式属性的访问。

```csharp
public ListFormat ListFormat { get; }
```

## 评论

此属性仅对段落样式有效。 对于此属性返回的其他样式类型`无效的`。

## 例子

演示如何创建和使用具有列表格式的段落样式。

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

// 将段落样式应用到文档生成器的当前段落，然后添加一些文本。
builder.ParagraphFormat.Style = style;
builder.Writeln("Hello World: MyStyle1, bulleted list.");

// 将文档生成器的样式更改为没有列表格式的样式并编写另一段。
builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Writeln("Hello World: Normal.");

builder.Document.Save(ArtifactsDir + "Styles.ParagraphStyleBulletedList.docx");
```

### 也可以看看

* class [ListFormat](../../../aspose.words.lists/listformat/)
* class [Style](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
