---
title: ListTemplate Enum
linktitle: ListTemplate
articleTitle: ListTemplate
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Lists.ListTemplate 枚举. 指定 Microsoft Word 中可用的预定义列表格式之一 在 C#.
type: docs
weight: 3530
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
| BulletDefault | `0` | 默认项目符号列表有 9 个级别。第一级的项目符号是圆盘， 第二级的项目符号是圆形，第三级的项目符号是正方形。 然后对其余级别重复格式化。 |
| BulletDisk | `0` | 与...一样BulletDefault。 |
| BulletCircle | `1` | 第一级的子弹是一个圆圈。其余级别与中相同BulletDefault。 |
| BulletSquare | `2` | 第一级的子弹是一个正方形。其余级别与中相同BulletDefault。 |
| BulletDiamonds | `3` | 第一关的子弹是4钻石Wingding角色。其余级别与中相同BulletDefault。 |
| BulletArrowHead | `4` | 第一关的子弹是一个箭头Wingding字符。其余级别与中相同BulletDefault。 |
| BulletTick | `5` | 第一关的子弹是一个勾号Wingding角色。其余级别与中相同BulletDefault。 |
| NumberDefault | `6` | 默认编号列表有 9 级。第一级为阿拉伯编号（1.、2.、3.、...），第二级为 小写字母编号（a.、b.、c.、...）， 小写罗马编号（i ., ii., iii., ...) 对于第三级。 然后对其余级别重复格式化。 |
| NumberArabicDot | `6` | 与...一样NumberDefault。 |
| NumberArabicParenthesis | `7` | 第一级的编号是“1)”。其余级别与中相同NumberDefault。 |
| NumberUppercaseRomanDot | `8` | 第一级的编号是“I.”。其余级别与中相同NumberDefault。 |
| NumberUppercaseLetterDot | `9` | 第一级的编号是“A.”。其余级别与中相同NumberDefault。 |
| NumberLowercaseLetterParenthesis | `10` | 第一级的编号是“a)”。其余级别与中相同NumberDefault。 |
| NumberLowercaseLetterDot | `11` | 第一级的编号是“a.”。其余级别与中相同NumberDefault。 |
| NumberLowercaseRomanDot | `12` | 第一级的编号是“i.”。其余级别与中相同NumberDefault。 |
| OutlineNumbers | `13` | 级别编号为“1)、a)、i)、(1)、(a)、(i)、1.、a.、i.”的大纲列表。 |
| OutlineLegal | `14` | 具有级别的大纲列表编号为“1.、1.1.、1.1.1、...”。 |
| OutlineBullets | `15` | 大纲列出了不同级别的各种项目符号。 |
| OutlineHeadingsArticleSection | `16` | 具有链接到标题样式的级别的大纲列表。 |
| OutlineHeadingsLegal | `17` | 具有链接到标题样式的级别的大纲列表。 |
| OutlineHeadingsNumbers | `18` | 具有链接到标题样式的级别的大纲列表。 |
| OutlineHeadingsChapter | `19` | 具有链接到标题样式的级别的大纲列表。 |

## 评论

列表模板值用作 the 的参数[`Add`](../listcollection/add/)方法。

Aspose.Words 列表模板对应于 Microsoft Word 2003 中“项目符号和编号”对话框中的 21 个列表模板 available 。

## 例子

演示如何创建包含所有大纲标题列表模板的文档。

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

演示如何通过复制列表来重新开始列表中的编号。

```csharp
Document doc = new Document();

// 列表允许我们使用前缀符号和缩进来组织和装饰段落集。
 // 我们可以通过增加缩进级别来创建嵌套列表。
 // 我们可以使用文档构建器的“ListFormat”属性来开始和结束列表。
// 我们在列表的开头和结尾之间添加的每个段落都将成为列表中的一个项目。
// 从 Microsoft Word 模板创建列表，并自定义其第一列表级别。
List list1 = doc.Lists.Add(ListTemplate.NumberArabicParenthesis);
list1.ListLevels[0].Font.Color = Color.Red;
list1.ListLevels[0].Alignment = ListLevelAlignment.Right;

// 将我们的列表应用于某些段落。
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("List 1 starts below:");
builder.ListFormat.List = list1;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

// 我们可以将现有列表的副本添加到文档的列表集合中
// 创建一个类似的列表而不对原始列表进行更改。
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
// 我们在列表的开头和结尾之间添加的每个段落都将成为列表中的一个项目。
// 下面是我们可以使用文档生成器创建的两种类型的列表。
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
// 此列表将在每个段落之前应用缩进和项目符号（“•”）。
// 此列表的更深层次将使用不同的符号，例如“■”和“○”。
builder.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);

for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// 我们可以通过取消设置“List”标志来禁用列表格式，以不将任何后续段落格式化为列表。
builder.ListFormat.List = null;

Assert.False(builder.ListFormat.IsListItem);

doc.Save(ArtifactsDir + "Lists.SpecifyListLevel.docx");
```

### 也可以看看

* 命名空间 [Aspose.Words.Lists](../../aspose.words.lists/)
* 部件 [Aspose.Words](../../)
