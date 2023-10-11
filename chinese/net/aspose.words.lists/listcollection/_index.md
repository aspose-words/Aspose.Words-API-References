---
title: Class ListCollection
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Lists.ListCollection 班级. 存储和管理文档中使用的项目符号列表和编号列表的格式
type: docs
weight: 3470
url: /zh/net/aspose.words.lists/listcollection/
---
## ListCollection class

存储和管理文档中使用的项目符号列表和编号列表的格式。

要了解更多信息，请访问[使用列表](https://docs.aspose.com/words/net/working-with-lists/)文档文章。

```csharp
public class ListCollection : IEnumerable<List>
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Count](../../aspose.words.lists/listcollection/count/) { get; } | 获取文档中编号列表和项目符号列表的计数。 |
| [Document](../../aspose.words.lists/listcollection/document/) { get; } | 获取所有者文档。 |
| [Item](../../aspose.words.lists/listcollection/item/) { get; } | 按索引获取列表。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Add](../../aspose.words.lists/listcollection/add/#add)(ListTemplate) | 根据预定义模板创建新列表并将其添加到文档中的列表集合中。 |
| [Add](../../aspose.words.lists/listcollection/add/#add_1)(Style) | 创建引用列表样式的新列表并将其添加到文档中的列表集合中。 |
| [AddCopy](../../aspose.words.lists/listcollection/addcopy/)(List) | 通过复制指定列表并将其添加到文档中的列表集合中来创建新列表。 |
| [GetEnumerator](../../aspose.words.lists/listcollection/getenumerator/)() | 获取将枚举文档中列表的枚举器对象。 |
| [GetListByListId](../../aspose.words.lists/listcollection/getlistbylistid/)(int) | 通过列表标识符获取列表。 |

### 评论

Microsoft Word 文档中的列表是一组列表格式属性。 列表的格式存储在`ListCollection`从文本段落中分别收集 。

您不创建此类的对象。永远只有一个`ListCollection`每个文档 对象，可以通过[`Lists`](../../aspose.words/documentbase/lists/)财产。

要基于预定义列表模板或基于列表样式创建新列表， 使用[`Add`](./add/)方法。

要创建格式与现有列表相同的新列表， 使用[`AddCopy`](./addcopy/)方法。

要使段落带有项目符号或编号，您需要通过分配一个列表格式 到段落[`List`](../list/)反对 [`List`](../listformat/list/)的财产[`ListFormat`](../listformat/)。

要从段落中删除列表格式，请使用[`RemoveNumbers`](../listformat/removenumbers/) 方法。

如果您对 WordprocessingML 了解一点，那么您可能知道它为“列表”和“列表定义”定义了单独的概念 。这与 Microsoft Word 文档中低级别的列表格式存储 的方式完全一致。列表定义就像一个“模式”，而 列表就像列表定义的实例。

为了简化编程模型，Aspose.Words 隐藏了列表和列表 定义之间的区别，就像 Microsoft Word 在其用户界面中隐藏这一点一样。 这使您可以更加专注于您希望文档的外观，而不是 构建低级对象以满足 Microsoft Word 文件格式的要求。

一旦列表在当前版本的 Aspose.Words. 中创建，就无法删除列表，这类似于 Microsoft Word，用户对列表定义没有明确的控制权。

### 例子

演示如何使用另一个文档中的所有列表的示例创建文档。

```csharp
public void PrintOutAllLists()
{
    Document srcDoc = new Document(MyDir + "Rendering.docx");

    Document dstDoc = new Document();
    DocumentBuilder builder = new DocumentBuilder(dstDoc);

    foreach (List srcList in srcDoc.Lists)
    {
        List dstList = dstDoc.Lists.AddCopy(srcList);
        AddListSample(builder, dstList);
    }

    dstDoc.Save(ArtifactsDir + "Lists.PrintOutAllLists.docx");
}

private static void AddListSample(DocumentBuilder builder, List list)
{
    builder.Writeln("Sample formatting of list with ListId:" + list.ListId);
    builder.ListFormat.List = list;
    for (int i = 0; i < list.ListLevels.Count; i++)
    {
        builder.ListFormat.ListLevelNumber = i;
        builder.Writeln("Level " + i);
    }

    builder.ListFormat.RemoveNumbers();
    builder.Writeln();
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

* class [List](../list/)
* 命名空间 [Aspose.Words.Lists](../../aspose.words.lists/)
* 部件 [Aspose.Words](../../)


