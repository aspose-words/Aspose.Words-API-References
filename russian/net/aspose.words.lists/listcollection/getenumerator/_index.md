---
title: ListCollection.GetEnumerator
second_title: Справочник по API Aspose.Words для .NET
description: ListCollection метод. Получает объект перечислителя который будет перечислять списки в документе.
type: docs
weight: 60
url: /ru/net/aspose.words.lists/listcollection/getenumerator/
---
## ListCollection.GetEnumerator method

Получает объект перечислителя, который будет перечислять списки в документе.

```csharp
public IEnumerator<List> GetEnumerator()
```

### Примеры

Показывает, как создать документ с выборкой всех списков из другого документа.

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

### Смотрите также

* class [List](../../list/)
* class [ListCollection](../)
* пространство имен [Aspose.Words.Lists](../../listcollection/)
* сборка [Aspose.Words](../../../)


