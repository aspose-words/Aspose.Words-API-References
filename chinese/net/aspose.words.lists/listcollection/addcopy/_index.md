---
title: ListCollection.AddCopy
linktitle: AddCopy
articleTitle: AddCopy
second_title: 用于 .NET 的 Aspose.Words
description: ListCollection AddCopy 方法. 通过复制指定列表并将其添加到文档中的列表集合中来创建新列表 在 C#.
type: docs
weight: 50
url: /zh/net/aspose.words.lists/listcollection/addcopy/
---
## ListCollection.AddCopy method

通过复制指定列表并将其添加到文档中的列表集合中来创建新列表。

```csharp
public List AddCopy(List srcList)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| srcList | List | 要复制的源列表。 |

### 返回值

新创建的列表。

## 评论

源列表可以来自任何文档。如果源列表属于不同的文档，则会创建 列表的副本并将其添加到当前文档中。

如果源列表是列表样式的引用或定义，则 新创建的列表与原始列表样式无关。

## 例子

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

### 也可以看看

* class [List](../../list/)
* class [ListCollection](../)
* 命名空间 [Aspose.Words.Lists](../../../aspose.words.lists/)
* 部件 [Aspose.Words](../../../)
