---
title: ListTemplate
second_title: Aspose.Words for .NET API 参考
description: 指定 Microsoft Word 中可用的预定义列表格式之一
type: docs
weight: 3280
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
| BulletDefault | `0` | 默认项目符号列表有 9 个级别。第一级子弹是圆盘， 第二级子弹是圆形，第三级子弹是方形。 然后对其余级别重复格式化。 |
| BulletDisk | `0` | 与 BulletDefault 相同。 |
| BulletCircle | `1` | 第一级的子弹是一个圆圈。其余级别与 BulletDefault 中的相同。 |
| BulletSquare | `2` | 第一级的子弹是正方形。其余级别与 BulletDefault 中的相同。 |
| BulletDiamonds | `3` | 第一级的子弹是一个4钻的Wingding字符。其余级别与 BulletDefault 中的相同。 |
| BulletArrowHead | `4` | 第一级的子弹是箭头Wingding字符。其余级别与 BulletDefault 中的相同。 |
| BulletTick | `5` | 第一级的子弹是一个打勾的Wingding字符。其余级别与 BulletDefault 中的相同。 |
| NumberDefault | `6` | 默认编号列表，有 9 个级别。第一级阿拉伯编号（1., 2., 3., ...），第二级 小写字母编号（a., b., c., ...）， 第三级的小写罗马编号（i., ii., iii., ...）。 然后对其余级别重复格式化。 |
| NumberArabicDot | `6` | 与 NumberDefault 相同。 |
| NumberArabicParenthesis | `7` | 第一级数为“1)”。其余级别与 NumberDefault 中的相同。 |
| NumberUppercaseRomanDot | `8` | 第一级的数字是“I.”。其余级别与 NumberDefault 中的相同。 |
| NumberUppercaseLetterDot | `9` | 第一级的编号是“A.”。其余级别与 NumberDefault 中的相同。 |
| NumberLowercaseLetterParenthesis | `10` | 第一级的编号是“a)”。其余级别与 NumberDefault 中的相同。 |
| NumberLowercaseLetterDot | `11` | 第一级的数字是“a.”。其余级别与 NumberDefault 中的相同。 |
| NumberLowercaseRomanDot | `12` | 第一层的编号是“i.”。其余级别与 NumberDefault 中的相同。 |
| OutlineNumbers | `13` | 等级编号为“1), a), i), (1), (a), (i), 1., a.,一世。”。 |
| OutlineLegal | `14` | 带有级别的大纲列表编号为“1., 1.1., 1.1.1, ...”。 |
| OutlineBullets | `15` | 大纲列出了不同级别的各种项目符号。 |
| OutlineHeadingsArticleSection | `16` | 与标题样式相关的级别的大纲列表。 |
| OutlineHeadingsLegal | `17` | 与标题样式相关的级别的大纲列表。 |
| OutlineHeadingsNumbers | `18` | 与标题样式相关的级别的大纲列表。 |
| OutlineHeadingsChapter | `19` | 与标题样式相关的级别的大纲列表。 |

### 评论

列表模板值用作 的参数[`Add`](../listcollection/add)方法。

Aspose.Words 列表模板对应于 Microsoft Word 2003 的项目符号和编号对话框中的 21 个可用列表模板 。

### 例子

显示如何创建包含所有大纲标题列表模板的文档。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.False(builder.ListFormat.IsListItem);

// 列表允许我们用前缀符号和缩进组织和装饰段落集。
 // 我们可以通过增加缩进级别来创建嵌套列表。 
 // 我们可以使用文档构建器的“ListFormat”属性来开始和结束一个列表。 
 // 我们在列表开头和结尾之间添加的每个段落都将成为列表中的一个项目。
 // 下面是我们可以使用文档构建器创建的两种类型的列表。
 // 1 - 编号列表：
 // 编号列表通过为每个项目编号来为其段落创建逻辑顺序。
builder.ListFormat.List = doc.Lists.Add(ListTemplate.NumberDefault);

Assert.True(builder.ListFormat.IsListItem);

 // 通过设置“ListLevelNumber”属性，我们可以增加列表级别
 // 在当前列表项开始一个自包含的子列表。
 // 名为“NumberDefault”的 Microsoft Word 列表模板使用数字为第一个列表级别创建列表级别。
// 更深的列表级别使用字母和小写罗马数字。 
for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

 // 2 - 项目符号列表：
 // 此列表将在每个段落之前应用缩进和项目符号 ("•")。
 // 此列表的更深层次将使用不同的符号，例如“■”和“○”。
builder.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);

for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

 // 我们可以通过取消设置“列表”标志来禁用列表格式，以不将任何后续段落格式化为列表。
builder.ListFormat.List = null;

Assert.False(builder.ListFormat.IsListItem);

doc.Save(ArtifactsDir + "Lists.SpecifyListLevel.docx");
```

显示如何通过复制列表重新开始编号。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.False(builder.ListFormat.IsListItem);

// 列表允许我们用前缀符号和缩进组织和装饰段落集。
 // 我们可以通过增加缩进级别来创建嵌套列表。 
 // 我们可以使用文档构建器的“ListFormat”属性来开始和结束一个列表。 
 // 我们在列表开头和结尾之间添加的每个段落都将成为列表中的一个项目。
 // 下面是我们可以使用文档构建器创建的两种类型的列表。
 // 1 - 编号列表：
 // 编号列表通过为每个项目编号来为其段落创建逻辑顺序。
builder.ListFormat.List = doc.Lists.Add(ListTemplate.NumberDefault);

Assert.True(builder.ListFormat.IsListItem);

 // 通过设置“ListLevelNumber”属性，我们可以增加列表级别
 // 在当前列表项开始一个自包含的子列表。
 // 名为“NumberDefault”的 Microsoft Word 列表模板使用数字为第一个列表级别创建列表级别。
// 更深的列表级别使用字母和小写罗马数字。 
for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

 // 2 - 项目符号列表：
 // 此列表将在每个段落之前应用缩进和项目符号 ("•")。
 // 此列表的更深层次将使用不同的符号，例如“■”和“○”。
builder.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);

for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

 // 我们可以通过取消设置“列表”标志来禁用列表格式，以不将任何后续段落格式化为列表。
builder.ListFormat.List = null;

Assert.False(builder.ListFormat.IsListItem);

doc.Save(ArtifactsDir + "Lists.SpecifyListLevel.docx");
```

显示如何使用列表级别。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.False(builder.ListFormat.IsListItem);

// 列表允许我们用前缀符号和缩进组织和装饰段落集。
 // 我们可以通过增加缩进级别来创建嵌套列表。 
 // 我们可以使用文档构建器的“ListFormat”属性来开始和结束一个列表。 
 // 我们在列表开头和结尾之间添加的每个段落都将成为列表中的一个项目。
 // 下面是我们可以使用文档构建器创建的两种类型的列表。
 // 1 - 编号列表：
 // 编号列表通过为每个项目编号来为其段落创建逻辑顺序。
builder.ListFormat.List = doc.Lists.Add(ListTemplate.NumberDefault);

Assert.True(builder.ListFormat.IsListItem);

 // 通过设置“ListLevelNumber”属性，我们可以增加列表级别
 // 在当前列表项开始一个自包含的子列表。
 // 名为“NumberDefault”的 Microsoft Word 列表模板使用数字为第一个列表级别创建列表级别。
// 更深的列表级别使用字母和小写罗马数字。 
for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

 // 2 - 项目符号列表：
 // 此列表将在每个段落之前应用缩进和项目符号 ("•")。
 // 此列表的更深层次将使用不同的符号，例如“■”和“○”。
builder.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);

for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

 // 我们可以通过取消设置“列表”标志来禁用列表格式，以不将任何后续段落格式化为列表。
builder.ListFormat.List = null;

Assert.False(builder.ListFormat.IsListItem);

doc.Save(ArtifactsDir + "Lists.SpecifyListLevel.docx");
```

### 也可以看看

* namespace [Aspose.Words.Lists](../../aspose.words.lists)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
