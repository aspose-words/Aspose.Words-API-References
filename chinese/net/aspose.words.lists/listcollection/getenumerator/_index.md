---
title: ListCollection.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: 用于 .NET 的 Aspose.Words
description: ListCollection GetEnumerator 方法. 获取将枚举文档中列表的枚举器对象 在 C#.
type: docs
weight: 60
url: /zh/net/aspose.words.lists/listcollection/getenumerator/
---
## ListCollection.GetEnumerator method

获取将枚举文档中列表的枚举器对象。

```csharp
public IEnumerator<List> GetEnumerator()
```

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

### 也可以看看

* class [List](../../list/)
* class [ListCollection](../)
* 命名空间 [Aspose.Words.Lists](../../../aspose.words.lists/)
* 部件 [Aspose.Words](../../../)
