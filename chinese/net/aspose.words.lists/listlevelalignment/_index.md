---
title: ListLevelAlignment Enum
linktitle: ListLevelAlignment
articleTitle: ListLevelAlignment
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Lists.ListLevelAlignment 枚举，实现最佳列表数量和项目符号对齐。轻松增强文档格式！
type: docs
weight: 3960
url: /zh/net/aspose.words.lists/listlevelalignment/
---
## ListLevelAlignment enumeration

指定列表编号或项目符号的对齐方式。

```csharp
public enum ListLevelAlignment
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Left | `0` | 列表标签与数字位置左侧对齐。 |
| Center | `1` | 列表标签以数字位置为中心。 |
| Right | `2` | 此列表标签与数字位置右侧对齐。 |

## 评论

用作[`Alignment`](../listlevel/alignment/)财产。

## 例子

展示如何在使用 DocumentBuilder 时将自定义列表格式应用于段落。

```csharp
Document doc = new Document();

// 列表允许我们使用前缀符号和缩进来组织和装饰段落集。
 // 我们可以通过增加缩进级别来创建嵌套列表。
 // 我们可以使用文档构建器的“ListFormat”属性来开始和结束列表。
// 我们在列表的开始和结束之间添加的每个段落都将成为列表中的一个项目。
// 从 Microsoft Word 模板创建列表，并自定义其列表级别的前两个。
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

// 创建段落并将我们的自定义列表格式的两个列表级别应用于它们。
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

### 也可以看看

* 命名空间 [Aspose.Words.Lists](../../aspose.words.lists/)
* 部件 [Aspose.Words](../../)
