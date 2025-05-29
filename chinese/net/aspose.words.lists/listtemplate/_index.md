---
title: ListTemplate Enum
linktitle: ListTemplate
articleTitle: ListTemplate
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Lists.ListTemplate 枚举，它具有预定义的 Microsoft Word 列表格式，可轻松增强文档的呈现效果。
type: docs
weight: 3980
url: /zh/net/aspose.words.lists/listtemplate/
---
## ListTemplate enumeration

指定 Microsoft Word 中可用的预定义列表格式之一。

```csharp
public enum ListTemplate
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| BulletDefault | `0` | 默认项目符号列表共 9 级。第一级项目符号为圆盘形， 第二级项目符号为圆形，第三级项目符号为正方形。 然后，对剩余级别重复此格式化操作。 |
| BulletDisk | `0` | 与……相同BulletDefault。 |
| BulletCircle | `1` | 第一级的子弹是圆形的。其余级别与BulletDefault。 |
| BulletSquare | `2` | 第一级的子弹是正方形。其余级别与BulletDefault。 |
| BulletDiamonds | `3` | 第一级的子弹是4钻石的Wingding角色。其余级别与BulletDefault。 |
| BulletArrowHead | `4` | 第一级的子弹是箭头形的Wingding字符。其余级别与BulletDefault。 |
| BulletTick | `5` | 第一级的子弹是勾选的Wingding字符。其余级别与BulletDefault。 |
| NumberDefault | `6` | 默认编号列表共 9 级。第一级使用阿拉伯数字 (1., 2., 3., ...)，第二级使用小写字母数字 (a., b., c., ...)，第三级使用小写罗马数字 (i., ii., iii., ...)。其余级别重复此格式。 |
| NumberArabicDot | `6` | 与……相同NumberDefault。 |
| NumberArabicParenthesis | `7` | 第一级的编号为“1)”。其余级别与NumberDefault。 |
| NumberUppercaseRomanDot | `8` | 第一级的编号为“I”。其余级别与NumberDefault。 |
| NumberUppercaseLetterDot | `9` | 第一级的编号为“A”。其余级别与NumberDefault。 |
| NumberLowercaseLetterParenthesis | `10` | 第一级的编号为“a)”。其余级别与NumberDefault。 |
| NumberLowercaseLetterDot | `11` | 第一级的编号为“a”。其余级别与NumberDefault。 |
| NumberLowercaseRomanDot | `12` | 第一级的编号为“i”。其余级别与NumberDefault。 |
| OutlineNumbers | `13` | 带有级别编号“1),a),i),(1),(a),(i),1.,a.,i.”的大纲列表。 |
| OutlineLegal | `14` | 具有级别的大纲列表编号为“1.，1.1.，1.1.1，...”。 |
| OutlineBullets | `15` | 大纲列出了不同级别的各种项目符号。 |
| OutlineHeadingsArticleSection | `16` | 具有与标题样式相链接的级别的大纲列表。 |
| OutlineHeadingsLegal | `17` | 具有与标题样式相链接的级别的大纲列表。 |
| OutlineHeadingsNumbers | `18` | 具有与标题样式相链接的级别的大纲列表。 |
| OutlineHeadingsChapter | `19` | 具有与标题样式相链接的级别的大纲列表。 |

## 评论

列表模板值作为参数传入 [`Add`](../listcollection/add/)方法。

Aspose.Words 列表模板对应于 Microsoft Word 2003 中项目符号和编号对话框中的 21 个可用列表模板 。

## 例子

展示如何创建包含所有大纲标题列表模板的文档。

```csharp
public void OutlineHeadingTemplates()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    List list = doc.Lists.Add(ListTemplate.OutlineHeadingsArticleSection);
    AddOutlineHeadingParagraphs(builder, list, "Aspose.Words Outline - \"Article Section\"");

    list = doc.Lists.Add(ListTemplate.OutlineHeadingsLegal);
    AddOutlineHeadingParagraphs(builder, list, "Aspose.Words Outline - \"Legal\"");

    builder.InsertBreak(BreakType.PageBreak);

    list = doc.Lists.Add(ListTemplate.OutlineHeadingsNumbers);
    AddOutlineHeadingParagraphs(builder, list, "Aspose.Words Outline - \"Numbers\"");

    list = doc.Lists.Add(ListTemplate.OutlineHeadingsChapter);
    AddOutlineHeadingParagraphs(builder, list, "Aspose.Words Outline - \"Chapters\"");

    doc.Save(ArtifactsDir + "Lists.OutlineHeadingTemplates.docx");
}

private static void AddOutlineHeadingParagraphs(DocumentBuilder builder, List list, string title)
{
    builder.ParagraphFormat.ClearFormatting();
    builder.Writeln(title);

    for (int i = 0; i < 9; i++)
    {
        builder.ListFormat.List = list;
        builder.ListFormat.ListLevelNumber = i;

        string styleName = "Heading " + (i + 1);
        builder.ParagraphFormat.StyleName = styleName;
        builder.Writeln(styleName);
    }

    builder.ListFormat.RemoveNumbers();
}
```

展示如何通过复制列表重新开始列表中的编号。

```csharp
Document doc = new Document();

// 列表允许我们使用前缀符号和缩进来组织和装饰段落集。
 // 我们可以通过增加缩进级别来创建嵌套列表。
 // 我们可以使用文档构建器的“ListFormat”属性来开始和结束列表。
// 我们在列表的开始和结束之间添加的每个段落都将成为列表中的一个项目。
// 从 Microsoft Word 模板创建列表，并自定义其第一个列表级别。
List list1 = doc.Lists.Add(ListTemplate.NumberArabicParenthesis);
list1.ListLevels[0].Font.Color = Color.Red;
list1.ListLevels[0].Alignment = ListLevelAlignment.Right;

// 将我们的列表应用到一些段落。
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("List 1 starts below:");
builder.ListFormat.List = list1;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

// 我们可以将现有列表的副本添加到文档的列表集合中
// 创建类似的列表而不更改原始列表。
List list2 = doc.Lists.AddCopy(list1);
list2.ListLevels[0].Font.Color = Color.Blue;
list2.ListLevels[0].StartAt = 10;

// 将第二个列表应用于新段落。
builder.Writeln("List 2 starts below:");
builder.ListFormat.List = list2;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

doc.Save(ArtifactsDir + "Lists.RestartNumberingUsingListCopy.docx");
```

展示如何使用列表级别。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.False(builder.ListFormat.IsListItem);

// 列表允许我们使用前缀符号和缩进来组织和装饰段落集。
 // 我们可以通过增加缩进级别来创建嵌套列表。
 // 我们可以使用文档构建器的“ListFormat”属性来开始和结束列表。
// 我们在列表的开始和结束之间添加的每个段落都将成为列表中的一个项目。
// 以下是我们可以使用文档构建器创建的两种类型的列表。
// 1 - 编号列表：
// 编号列表通过对每个项目进行编号来为其段落创建逻辑顺序。
builder.ListFormat.List = doc.Lists.Add(ListTemplate.NumberDefault);

Assert.True(builder.ListFormat.IsListItem);

// 通过设置“ListLevelNumber”属性，我们可以增加列表级别
// 在当前列表项处开始一个独立的子列表。
// 名为“NumberDefault”的 Microsoft Word 列表模板使用数字为第一个列表级别创建列表级别。
 // 更深的列表级别使用字母和小写罗马数字。
for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// 2 - 项目符号列表：
// 此列表将在每个段落前应用缩进和项目符号（“•”）。
// 此列表的更深级别将使用不同的符号，例如“■”和“○”。
builder.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);

for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// 我们可以通过取消设置“列表”标志来禁用列表格式，以免将任何后续段落格式化为列表。
builder.ListFormat.List = null;

Assert.False(builder.ListFormat.IsListItem);

doc.Save(ArtifactsDir + "Lists.SpecifyListLevel.docx");
```

### 也可以看看

* 命名空间 [Aspose.Words.Lists](../../aspose.words.lists/)
* 部件 [Aspose.Words](../../)
