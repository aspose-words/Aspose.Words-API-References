---
title: ListCollection
second_title: Aspose.Words for .NET API 参考
description: 存储和管理文档中使用的项目符号和编号列表的格式
type: docs
weight: 3220
url: /zh/net/aspose.words.lists/listcollection/
---
## ListCollection class

存储和管理文档中使用的项目符号和编号列表的格式。

```csharp
public class ListCollection : IEnumerable<List>
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Count](../../aspose.words.lists/listcollection/count) { get; } | 获取文档中编号和项目符号列表的计数。 |
| [Document](../../aspose.words.lists/listcollection/document) { get; } | 获取所有者文档。 |
| [Item](../../aspose.words.lists/listcollection/item) { get; } | 按索引获取列表。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Add](../../aspose.words.lists/listcollection/add#add)(ListTemplate) | 基于预定义模板创建一个新列表并将其添加到文档中的列表集合中。 |
| [Add](../../aspose.words.lists/listcollection/add#add_1)(Style) | 创建一个引用列表样式的新列表，并将其添加到文档中的列表集合中。 |
| [AddCopy](../../aspose.words.lists/listcollection/addcopy)(List) | 通过复制指定列表并将其添加到文档中的列表集合来创建一个新列表。 |
| [GetEnumerator](../../aspose.words.lists/listcollection/getenumerator)() | 获取将枚举文档中列表的枚举器对象。 |
| [GetListByListId](../../aspose.words.lists/listcollection/getlistbylistid)(int) | 通过列表标识符获取列表。 |

### 评论

Microsoft Word 文档中的列表是一组列表格式属性。 列表的格式分别存储在[`ListCollection`](../listcollection)集合中 与文本段落分开。

您不创建此类的对象。每个文档始终只有一个[`ListCollection`](../listcollection) 对象，可通过Lists属性。

要基于预定义列表模板或列表样式创建新列表， 使用[`Add`](./add)方法。

要创建格式与现有列表相同的新列表， 使用[`AddCopy`](./addcopy)方法。

要使段落带有项目符号或编号，您需要通过分配:::R5:T 将列表格式 应用于段落:Aspose.Words.Lists.List:::对象指向 [`List`](../listformat/list)ListFormat。

要从段落中删除列表格式，请使用[`RemoveNumbers`](../listformat/removenumbers) 方法。

如果您对 WordprocessingML 有所了解，那么您可能知道它为“列表”和“列表定义”定义了单独的概念 。这完全对应于列表格式在低级别 Microsoft Word 文档中的存储方式 。列表定义就像一个“模式”， 列表就像一个列表定义的实例。

为了简化编程模型，Aspose.Words 隐藏了列表和列表 定义之间的区别，就像 Microsoft Word 在它的用户界面。 这使您可以更专注于您希望文档的外观，而不是 构建低级对象以满足 Microsoft Word 文件格式的要求。

列表在当前版本的 Aspose.Words 中创建后就无法删除。 这类似于 Microsoft Word，其中用户无法明确控制列表定义。

### 例子

显示如何使用来自另一个文档的所有列表的样本创建文档。

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

* class [List](../list)
* 命名空间 [Aspose.Words.Lists](../../aspose.words.lists)
* 部件 [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
