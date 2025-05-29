---
title: ListLevel.IsLegal
linktitle: IsLegal
articleTitle: IsLegal
second_title: Aspose.Words for .NET
description: 探索 ListLevel IsLegal 规则。轻松控制继承的数字样式。选择阿拉伯数字可呈现现代风格，或保留原始样式，打造经典风格。
type: docs
weight: 50
url: /zh/net/aspose.words.lists/listlevel/islegal/
---
## ListLevel.IsLegal property

如果级别将所有继承的数字转换为阿拉伯数字，则为 True；如果保留其数字样式，则为 false。

```csharp
public bool IsLegal { get; set; }
```

## 例子

展示自定义列表标签的先进方法。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 列表允许我们使用前缀符号和缩进来组织和装饰段落集。
 // 我们可以通过增加缩进级别来创建嵌套列表。
 // 我们可以使用文档构建器的“ListFormat”属性来开始和结束列表。
// 我们在列表的开始和结束之间添加的每个段落都将成为列表中的一个项目。
List list = doc.Lists.Add(ListTemplate.NumberDefault);

// 1 级标签将根据“标题 1”段落样式进行格式化，并带有前缀。
// 这些看起来像“附录 A”、“附录 B”……
list.ListLevels[0].NumberFormat = "Appendix \x0000";
list.ListLevels[0].NumberStyle = NumberStyle.UppercaseLetter;
list.ListLevels[0].LinkedStyle = doc.Styles["Heading 1"];

// 2 级标签将显示第一和第二个列表级别的当前编号，并以零为前导。
// 如果第一个列表级别为 1，则这些列表的标签将类似于“第 (1.01) 节”、“第 (1.02) 节”...
list.ListLevels[1].NumberFormat = "Section (\x0000.\x0001)";
list.ListLevels[1].NumberStyle = NumberStyle.LeadingZero;

// 请注意，更高级别使用大写字母编号。
// 我们可以设置“IsLegal”属性，以便对较高列表级别使用阿拉伯数字。
list.ListLevels[1].IsLegal = true;
list.ListLevels[1].RestartAfterLevel = 0;

// 3 级标签将是带有前缀和后缀的大写罗马数字，并将在每个列表 1 级项目处重新开始。
// 这些列表标签看起来像“-I-”，“-II-”...
list.ListLevels[2].NumberFormat = "-\x0002-";
list.ListLevels[2].NumberStyle = NumberStyle.UppercaseRoman;
list.ListLevels[2].RestartAfterLevel = 1;

// 使所有列表级别的标签变为粗体。
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

* class [ListLevel](../)
* 命名空间 [Aspose.Words.Lists](../../../aspose.words.lists/)
* 部件 [Aspose.Words](../../../)
