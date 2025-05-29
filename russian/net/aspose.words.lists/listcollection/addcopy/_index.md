---
title: ListCollection.AddCopy
linktitle: AddCopy
articleTitle: AddCopy
second_title: Aspose.Words для .NET
description: Откройте для себя метод ListCollection AddCopy, который позволит вам легко и эффективно дублировать список и расширять коллекцию вашего документа.
type: docs
weight: 50
url: /ru/net/aspose.words.lists/listcollection/addcopy/
---
## ListCollection.AddCopy method

Создает новый список путем копирования указанного списка и добавления его в коллекцию списков в документе.

```csharp
public List AddCopy(List srcList)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| srcList | List | Список источников для копирования. |

### Возвращаемое значение

Недавно созданный список.

## Примечания

Исходный список может быть из любого документа. Если исходный список принадлежит другому документу, создается копия списка и добавляется в текущий документ.

Если исходный список является ссылкой на стиль списка или его определением, , то вновь созданный список не будет связан с исходным стилем списка.

## Примеры

Показывает, как создать документ с образцом всех списков из другого документа.

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

Показывает, как перезапустить нумерацию в списке, скопировав список.

```csharp
Document doc = new Document();

// Список позволяет нам организовывать и украшать наборы абзацев с помощью префиксных символов и отступов.
 // Мы можем создавать вложенные списки, увеличивая уровень отступа.
 // Мы можем начать и закончить список, используя свойство "ListFormat" конструктора документов.
// Каждый абзац, который мы добавляем между началом и концом списка, станет элементом в списке.
// Создайте список из шаблона Microsoft Word и настройте его первый уровень списка.
List list1 = doc.Lists.Add(ListTemplate.NumberArabicParenthesis);
list1.ListLevels[0].Font.Color = Color.Red;
list1.ListLevels[0].Alignment = ListLevelAlignment.Right;

// Применим наш список к некоторым абзацам.
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("List 1 starts below:");
builder.ListFormat.List = list1;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

// Мы можем добавить копию существующего списка в коллекцию списков документа
// чтобы создать аналогичный список, не внося изменений в оригинал.
List list2 = doc.Lists.AddCopy(list1);
list2.ListLevels[0].Font.Color = Color.Blue;
list2.ListLevels[0].StartAt = 10;

// Применяем второй список к новым абзацам.
builder.Writeln("List 2 starts below:");
builder.ListFormat.List = list2;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

doc.Save(ArtifactsDir + "Lists.RestartNumberingUsingListCopy.docx");
```

### Смотрите также

* class [List](../../list/)
* class [ListCollection](../)
* пространство имен [Aspose.Words.Lists](../../../aspose.words.lists/)
* сборка [Aspose.Words](../../../)
