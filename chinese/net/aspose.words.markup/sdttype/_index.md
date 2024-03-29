---
title: SdtType Enum
linktitle: SdtType
articleTitle: SdtType
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Markup.SdtType 枚举. 指定结构化文档标记 SDT 节点的类型 在 C#.
type: docs
weight: 4040
url: /zh/net/aspose.words.markup/sdttype/
---
## SdtType enumeration

指定结构化文档标记 (SDT) 节点的类型。

```csharp
public enum SdtType
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| None | `0` | 没有为 SDT 分配类型。 |
| Bibliography | `1` | SDT 表示参考书目条目。 |
| Citation | `2` | SDT 代表引用。 |
| Equation | `3` | SDT 表示一个方程。 |
| DropDownList | `4` | SDT 在文档中显示时表示下拉列表。 |
| ComboBox | `5` | SDT 在文档中显示时表示组合框。 |
| Date | `6` | SDT 在文档中显示时表示日期选择器。 |
| BuildingBlockGallery | `7` | SDT 代表构建块图库类型。 |
| DocPartObj | `8` | SDT 表示文档部分类型。 |
| Group | `9` | SDT 在文档中显示时表示受限分组。 |
| Picture | `10` | SDT 表示文档中显示的图片。 |
| RichText | `11` | SDT 在文档中显示时表示富文本框。 |
| PlainText | `12` | SDT 在文档中显示时表示纯文本框。 |
| Checkbox | `13` | SDT 在文档中显示时表示复选框。 |
| RepeatingSection | `14` | SDT 表示在文档中显示时的重复节类型。 |
| RepeatingSectionItem | `15` | SDT 表示重复节项。 |
| EntityPicker | `16` | SDT 表示一个实体选择器，允许用户选择外部内容类型的实例。 |

## 例子

展示如何在行级别创建组结构化文档标签。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();

// 在行级别创建组结构化文档标签。
StructuredDocumentTag groupSdt = new StructuredDocumentTag(doc, SdtType.Group, MarkupLevel.Row);
table.AppendChild(groupSdt);
groupSdt.IsShowingPlaceholderText = false;
groupSdt.RemoveAllChildren();

// 创建结构化文档标签的子行。
Row row = new Row(doc);
groupSdt.AppendChild(row);

Cell cell = new Cell(doc);
row.AppendChild(cell);

builder.EndTable();

// 插入单元格内容。
cell.EnsureMinimum();
builder.MoveTo(cell.LastParagraph);
builder.Write("Lorem ipsum dolor.");

// 在表格后面插入文本。
builder.MoveTo(table.NextSibling);
builder.Write("Nulla blandit nisi.");

doc.Save(ArtifactsDir + "StructuredDocumentTag.SdtAtRowLevel.docx");
```

展示如何使用内容控制元素的样式。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 下面是将文档样式应用到结构化文档标签的两种方法。
// 1 - 从文档的样式集合中应用样式对象：
Style quoteStyle = doc.Styles[StyleIdentifier.Quote];
StructuredDocumentTag sdtPlainText =
    new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline) { Style = quoteStyle };

// 2 - 按名称引用文档中的样式：
StructuredDocumentTag sdtRichText =
    new StructuredDocumentTag(doc, SdtType.RichText, MarkupLevel.Inline) { StyleName = "Quote" };

builder.InsertNode(sdtPlainText);
builder.InsertNode(sdtRichText);

Assert.AreEqual(NodeType.StructuredDocumentTag, sdtPlainText.NodeType);

NodeCollection tags = doc.GetChildNodes(NodeType.StructuredDocumentTag, true);

foreach (Node node in tags)
{
    StructuredDocumentTag sdt = (StructuredDocumentTag)node;

    Console.WriteLine(sdt.WordOpenXMLMinimal);

    Assert.AreEqual(StyleIdentifier.Quote, sdt.Style.StyleIdentifier);
    Assert.AreEqual("Quote", sdt.StyleName);
}
```

演示如何使用 XML 部件中的数据填充表。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

CustomXmlPart xmlPart = doc.CustomXmlParts.Add("Books",
    "<books>" +
        "<book>" +
            "<title>Everyday Italian</title>" +
            "<author>Giada De Laurentiis</author>" +
        "</book>" +
        "<book>" +
            "<title>The C Programming Language</title>" +
            "<author>Brian W. Kernighan, Dennis M. Ritchie</author>" +
        "</book>" +
        "<book>" +
            "<title>Learning XML</title>" +
            "<author>Erik T. Ray</author>" +
        "</book>" +
    "</books>");

// 为 XML 内容中的数据创建标头。
Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Title");
builder.InsertCell();
builder.Write("Author");
builder.EndRow();
builder.EndTable();

// 创建一个表，其中包含重复部分。
StructuredDocumentTag repeatingSectionSdt =
    new StructuredDocumentTag(doc, SdtType.RepeatingSection, MarkupLevel.Row);
repeatingSectionSdt.XmlMapping.SetMapping(xmlPart, "/books[1]/book", string.Empty);
table.AppendChild(repeatingSectionSdt);

// 在重复节中添加重复节项并将其标记为一行。
// 该表对于我们可以在 XML 文档中找到的每个元素都有一行
// 使用“/books[1]/book”XPath，其中共有三个。
StructuredDocumentTag repeatingSectionItemSdt =
    new StructuredDocumentTag(doc, SdtType.RepeatingSectionItem, MarkupLevel.Row);
repeatingSectionSdt.AppendChild(repeatingSectionItemSdt);

Row row = new Row(doc);
repeatingSectionItemSdt.AppendChild(row);

// 使用为每本书的标题和作者创建的表格单元格来映射 XML 数据。
StructuredDocumentTag titleSdt =
    new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Cell);
titleSdt.XmlMapping.SetMapping(xmlPart, "/books[1]/book[1]/title[1]", string.Empty);
row.AppendChild(titleSdt);

StructuredDocumentTag authorSdt =
    new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Cell);
authorSdt.XmlMapping.SetMapping(xmlPart, "/books[1]/book[1]/author[1]", string.Empty);
row.AppendChild(authorSdt);

doc.Save(ArtifactsDir + "StructuredDocumentTag.RepeatingSectionItem.docx");
```

### 也可以看看

* 命名空间 [Aspose.Words.Markup](../../aspose.words.markup/)
* 部件 [Aspose.Words](../../)
