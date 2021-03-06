---
title: IsListStyleDefinition
second_title: Справочник по API Aspose.Words для .NET
description: Возвращает true если этот список является определением стиля списка.
type: docs
weight: 20
url: /ru/net/aspose.words.lists/list/isliststyledefinition/
---
## List.IsListStyleDefinition property

Возвращает true, если этот список является определением стиля списка.

```csharp
public bool IsListStyleDefinition { get; }
```

### Примечания

Когда это свойство истинно,[`Style`](../style)Свойство возвращает стиль списка, который определяет этот список.

Изменяя свойства списка, определяющего стиль списка, вы изменяете properties стиля списка.

Список, являющийся определением стиля списка, нельзя применить непосредственно к параграфам , чтобы сделать их нумерованными.

### Примеры

Показывает, как создать стиль списка и использовать его в документе.

```csharp
Document doc = new Document();

// Список позволяет нам организовывать и оформлять наборы абзацев префиксными символами и отступами.
// Мы можем создавать вложенные списки, увеличивая уровень отступа. 
// Мы можем начать и закончить список, используя свойство "ListFormat" конструктора документов. 
// Каждый абзац, который мы добавляем между началом и концом списка, станет элементом списка.
// Мы можем содержать весь объект List в стиле.
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

// Создать другой список из списка в стиле.
List list2 = doc.Lists.Add(listStyle);

Assert.False(list2.IsListStyleDefinition);
Assert.True(list2.IsListStyleReference);
Assert.AreEqual(listStyle, list2.Style);

// Добавляем несколько элементов списка, которые будут отформатированы в нашем списке.
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

* class [List](../../list)
* пространство имен [Aspose.Words.Lists](../../list)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
