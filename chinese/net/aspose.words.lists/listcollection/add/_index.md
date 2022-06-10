---
title: Add
second_title: Aspose.Words for .NET API 参考
description: 基于预定义模板创建一个新列表并将其添加到文档中的列表集合中
type: docs
weight: 40
url: /zh/net/aspose.words.lists/listcollection/add/
---
## Add(ListTemplate) {#add}

基于预定义模板创建一个新列表并将其添加到文档中的列表集合中。

```csharp
public List Add(ListTemplate listTemplate)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| listTemplate | ListTemplate | 列表的模板。 |

### 返回值

新创建的列表。

### 评论

Aspose.Words 列表模板对应于项目符号和编号对话框中可用的 21 个列表模板 在 Microsoft Word 2003 中。

使用此方法创建的所有列表都有 9 个列表级别。

### 例子

展示如何通过将新列表格式应用于段落集合来创建列表。

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

* class [List](../../list)
* enum [ListTemplate](../../listtemplate)
* class [ListCollection](../../listcollection)
* 命名空间 [Aspose.Words.Lists](../../listcollection)
* 部件 [Aspose.Words](../../../)

---

## Add(Style) {#add_1}

创建一个引用列表样式的新列表，并将其添加到文档中的列表集合中。

```csharp
public List Add(Style listStyle)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| listStyle | Style | 列表样式。 |

### 返回值

新创建的列表。

### 评论

新创建的列表引用列表样式。如果更改列表的属性 样式，它会反映在列表的属性中。反之亦然，如果更改列表的属性 ，它会反映在列表样式的属性中。

### 例子

展示如何创建列表样式并在文档中使用它。

```csharp
Document doc = new Document();

// 列表允许我们用前缀符号和缩进组织和装饰段落集。
 // 我们可以通过增加缩进级别来创建嵌套列表。 
 // 我们可以使用文档构建器的“ListFormat”属性来开始和结束一个列表。 
 // 我们在列表开头和结尾之间添加的每个段落都将成为列表中的一个项目。
// 我们可以在一个样式中包含一个完整的 List 对象。
Style listStyle = doc.Styles.Add(StyleType.List, "MyListStyle");

List list1 = listStyle.List;

Assert.True(list1.IsListStyleDefinition);
Assert.False(list1.IsListStyleReference);
Assert.True(list1.IsMultiLevel);
Assert.AreEqual(listStyle, list1.Style);

 // 改变我们列表中所有列表级别的外观。
foreach (ListLevel level in list1.ListLevels)
{
    level.Font.Name = "Verdana";
    level.Font.Color = Color.Blue;
    level.Font.Bold = true;
}

DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Using list style first time:");

 // 从样式中的列表创建另一个列表。
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

### 也可以看看

* class [List](../../list)
* class [Style](../../../aspose.words/style)
* class [ListCollection](../../listcollection)
* 命名空间 [Aspose.Words.Lists](../../listcollection)
* 部件 [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
