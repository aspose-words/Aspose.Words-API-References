---
title: ListLevel.NumberStyle
linktitle: NumberStyle
articleTitle: NumberStyle
second_title: 用于 .NET 的 Aspose.Words
description: ListLevel NumberStyle 财产. 返回或设置此列表级别的数字样式 在 C#.
type: docs
weight: 90
url: /zh/net/aspose.words.lists/listlevel/numberstyle/
---
## ListLevel.NumberStyle property

返回或设置此列表级别的数字样式。

```csharp
public NumberStyle NumberStyle { get; set; }
```

## 例子

演示如何在使用 DocumentBuilder 时将自定义列表格式应用于段落。

```csharp
Document doc = new Document();

// 列表允许我们使用前缀符号和缩进来组织和装饰段落集。
 // 我们可以通过增加缩进级别来创建嵌套列表。
 // 我们可以使用文档构建器的“ListFormat”属性来开始和结束列表。
// 我们在列表的开头和结尾之间添加的每个段落都将成为列表中的一个项目。
// 从 Microsoft Word 模板创建列表，并自定义其列表的前两个级别。
List list = doc.Lists.Add(ListTemplate.NumberDefault);

ListLevel listLevel = list.ListLevels[0];
listLevel.Font.Color = Color.Red;
listLevel.Font.Size = 24;
listLevel.NumberStyle = NumberStyle.OrdinalText;
listLevel.StartAt = 21;
listLevel.NumberFormat = "\x0000";

listLevel.NumberPosition = -36;
listLevel.TextPosition = 144;
listLevel.TabPosition = 144;

listLevel = list.ListLevels[1];
listLevel.Alignment = ListLevelAlignment.Right;
listLevel.NumberStyle = NumberStyle.Bullet;
listLevel.Font.Name = "Wingdings";
listLevel.Font.Color = Color.Blue;
listLevel.Font.Size = 24;

// 此 NumberFormat 值将创建星形项目符号列表符号。
listLevel.NumberFormat = "\xf0af";
listLevel.TrailingCharacter = ListTrailingCharacter.Space;
listLevel.NumberPosition = 144;

// 创建段落并将自定义列表格式的两个列表级别应用到它们。
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ListFormat.List = list;
builder.Writeln("The quick brown fox...");
builder.Writeln("The quick brown fox...");

builder.ListFormat.ListIndent();
builder.Writeln("jumped over the lazy dog.");
builder.Writeln("jumped over the lazy dog.");

builder.ListFormat.ListOutdent();
builder.Writeln("The quick brown fox...");

builder.ListFormat.RemoveNumbers();

builder.Document.Save(ArtifactsDir + "Lists.CreateCustomList.docx");
```

显示自定义列表标签的高级方法。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 列表允许我们使用前缀符号和缩进来组织和装饰段落集。
 // 我们可以通过增加缩进级别来创建嵌套列表。
 // 我们可以使用文档构建器的“ListFormat”属性来开始和结束列表。
// 我们在列表的开头和结尾之间添加的每个段落都将成为列表中的一个项目。
List list = doc.Lists.Add(ListTemplate.NumberDefault);

// 1 级标签将根据“标题 1”段落样式进行格式化，并具有前缀。
// 这些看起来像“附录 A”、“附录 B”...
list.ListLevels[0].NumberFormat = "Appendix \x0000";
list.ListLevels[0].NumberStyle = NumberStyle.UppercaseLetter;
list.ListLevels[0].LinkedStyle = doc.Styles["Heading 1"];

// 2 级标签将显示第一和第二列表级别的当前编号，并有前导零。
// 如果第一个列表级别为 1，则这些列表标签将类似于“Section (1.01)”、“Section (1.02)”...
list.ListLevels[1].NumberFormat = "Section (\x0000.\x0001)";
list.ListLevels[1].NumberStyle = NumberStyle.LeadingZero;

// 请注意，更高级别使用大写字母编号。
// 我们可以设置“IsLegal”属性以使用阿拉伯数字表示较高的列表级别。
list.ListLevels[1].IsLegal = true;
list.ListLevels[1].RestartAfterLevel = 0;

// 3 级标签将是带有前缀和后缀的大写罗马数字，并将在每个列表 1 级项目处重新启动。
// 这些列表标签看起来像“-I-”、“-II-”...
list.ListLevels[2].NumberFormat = "-\x0002-";
list.ListLevels[2].NumberStyle = NumberStyle.UppercaseRoman;
list.ListLevels[2].RestartAfterLevel = 1;

// 将所有列表级别的标签设为粗体。
foreach (ListLevel level in list.ListLevels)
    level.Font.Bold = true;

// 将列表格式应用于当前段落。
builder.ListFormat.List = list;

// 创建将显示所有三个列表级别的列表项。
for (int n = 0; n < 2; n++)
{
    for (int i = 0; i < 3; i++)
    {
        builder.ListFormat.ListLevelNumber = i;
        builder.Writeln("Level " + i);
    }
}

builder.ListFormat.RemoveNumbers();

doc.Save(ArtifactsDir + "Lists.CreateListRestartAfterHigher.docx");
```

### 也可以看看

* enum [NumberStyle](../../../aspose.words/numberstyle/)
* class [ListLevel](../)
* 命名空间 [Aspose.Words.Lists](../../../aspose.words.lists/)
* 部件 [Aspose.Words](../../../)
