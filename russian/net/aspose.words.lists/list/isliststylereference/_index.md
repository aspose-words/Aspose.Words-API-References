---
title: List.IsListStyleReference
linktitle: IsListStyleReference
articleTitle: IsListStyleReference
second_title: Aspose.Words для .NET
description: List IsListStyleReference свойство. Возвращаетистинный если этот список является ссылкой на стиль списка на С#.
type: docs
weight: 30
url: /ru/net/aspose.words.lists/list/isliststylereference/
---
## List.IsListStyleReference property

Возвращает`истинный` если этот список является ссылкой на стиль списка.

```csharp
public bool IsListStyleReference { get; }
```

## Примечания

Обратите внимание, что изменение свойств списка, который является ссылкой на стиль списка, не имеет никакого эффекта. Форматирование списка, указанное в самом стиле списка, всегда имеет приоритет.

## Примеры

Показывает, как создать стиль списка и использовать его в документе.

```csharp
Document doc = new Document();

// Список позволяет нам организовывать и украшать наборы абзацев префиксными символами и отступами.
 // Мы можем создавать вложенные списки, увеличивая уровень отступа.
 // Мы можем начать и закончить список, используя свойство ListFormat конструктора документов.
// Каждый абзац, который мы добавляем между началом и концом списка, станет элементом списка.
// Мы можем содержать целый объект List внутри стиля.
Style listStyle = doc.Styles.Add(StyleType.List, "MyListStyle");

List list1 = listStyle.List;

Assert.True(list1.IsListStyleDefinition);
Assert.False(list1.IsListStyleReference);
Assert.True(list1.IsMultiLevel);
Assert.AreEqual(listStyle, list1.Style);

// Изменяем внешний вид всех уровней списка в нашем списке.
foreach (ListLevel level in list1.ListLevels)
{
    level.Font.Name = "Verdana";
    level.Font.Color = Color.Blue;
    level.Font.Bold = true;
}

DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Using list style first time:");

// Создать еще один список из списка внутри стиля.
List list2 = doc.Lists.Add(listStyle);

Assert.False(list2.IsListStyleDefinition);
Assert.True(list2.IsListStyleReference);
Assert.AreEqual(listStyle, list2.Style);

// Добавляем несколько элементов списка, которые наш список будет форматировать.
builder.ListFormat.List = list2;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

builder.Writeln("Using list style second time:");

// Создать и применить другой список на основе стиля списка.
List list3 = doc.Lists.Add(listStyle);
builder.ListFormat.List = list3;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

builder.Document.Save(ArtifactsDir + "Lists.CreateAndUseListStyle.docx");
```

### Смотрите также

* class [List](../)
* пространство имен [Aspose.Words.Lists](../../../aspose.words.lists/)
* сборка [Aspose.Words](../../../)
