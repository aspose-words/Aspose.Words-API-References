---
title: ListLevelCollection Class
linktitle: ListLevelCollection
articleTitle: ListLevelCollection
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Lists.ListLevelCollection 班级. 列表中每个级别的列表格式集合 在 C#.
type: docs
weight: 3520
url: /zh/net/aspose.words.lists/listlevelcollection/
---
## ListLevelCollection class

列表中每个级别的列表格式集合。

要了解更多信息，请访问[使用列表](https://docs.aspose.com/words/net/working-with-lists/)文档文章。

```csharp
public class ListLevelCollection : IEnumerable<ListLevel>
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Count](../../aspose.words.lists/listlevelcollection/count/) { get; } | 获取此列表中的级别数。 |
| [Item](../../aspose.words.lists/listlevelcollection/item/) { get; set; } | 按索引获取列表级别。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [GetEnumerator](../../aspose.words.lists/listlevelcollection/getenumerator/)() | 获取将枚举此列表中级别的枚举器对象。 |

## 例子

演示如何创建列表样式并在文档中使用它。

```csharp
Document doc = new Document();

// 列表允许我们使用前缀符号和缩进来组织和装饰段落集。
 // 我们可以通过增加缩进级别来创建嵌套列表。
 // 我们可以使用文档构建器的“ListFormat”属性来开始和结束列表。
// 我们在列表的开头和结尾之间添加的每个段落都将成为列表中的一个项目。
// 我们可以在样式中包含整个 List 对象。
Style listStyle = doc.Styles.Add(StyleType.List, "MyListStyle");

List list1 = listStyle.List;

Assert.True(list1.IsListStyleDefinition);
Assert.False(list1.IsListStyleReference);
Assert.True(list1.IsMultiLevel);
Assert.AreEqual(listStyle, list1.Style);

// 更改列表中所有列表级别的外观。
foreach (ListLevel level in list1.ListLevels)
{
    level.Font.Name = "Verdana";
    level.Font.Color = Color.Blue;
    level.Font.Bold = true;
}

DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Using list style first time:");

// 从样式内的列表创建另一个列表。
List list2 = doc.Lists.Add(listStyle);

Assert.False(list2.IsListStyleDefinition);
Assert.True(list2.IsListStyleReference);
Assert.AreEqual(listStyle, list2.Style);

// 添加我们的列表将格式化的一些列表项。
builder.ListFormat.List = list2;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

builder.Writeln("Using list style second time:");

// 根据列表样式创建并应用另一个列表。
List list3 = doc.Lists.Add(listStyle);
builder.ListFormat.List = list3;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

builder.Document.Save(ArtifactsDir + "Lists.CreateAndUseListStyle.docx");
```

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

### 也可以看看

* class [ListLevel](../listlevel/)
* 命名空间 [Aspose.Words.Lists](../../aspose.words.lists/)
* 部件 [Aspose.Words](../../)
