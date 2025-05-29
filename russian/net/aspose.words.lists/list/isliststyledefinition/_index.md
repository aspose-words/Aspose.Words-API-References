---
title: List.IsListStyleDefinition
linktitle: IsListStyleDefinition
articleTitle: IsListStyleDefinition
second_title: Aspose.Words для .NET
description: Узнайте, определяет ли свойство List IsListStyleDefinition стиль списка. Откройте расширенные возможности стилизации для ваших списков сегодня!
type: docs
weight: 20
url: /ru/net/aspose.words.lists/list/isliststyledefinition/
---
## List.IsListStyleDefinition property

Возврат`истинный` если этот список является определением стиля списка.

```csharp
public bool IsListStyleDefinition { get; }
```

## Примечания

Когда это свойство`истинный` ,[`Style`](../style/) свойство возвращает стиль списка, который определяет этот список.

Изменяя свойства списка, определяющего стиль списка, вы изменяете свойства стиля списка.

Список, являющийся определением стиля списка, нельзя напрямую применить к paragraphs , чтобы сделать их нумерованными.

## Примеры

Показывает, как создать стиль списка и использовать его в документе.

```csharp
Document doc = new Document();

// Список позволяет нам организовывать и украшать наборы абзацев с помощью префиксных символов и отступов.
 // Мы можем создавать вложенные списки, увеличивая уровень отступа.
 // Мы можем начать и закончить список, используя свойство "ListFormat" конструктора документов.
// Каждый абзац, который мы добавляем между началом и концом списка, станет элементом в списке.
// Мы можем поместить целый объект List в стиль.
Style listStyle = doc.Styles.Add(StyleType.List, "MyListStyle");

List list1 = listStyle.List;

Assert.True(list1.IsListStyleDefinition);
Assert.False(list1.IsListStyleReference);
Assert.True(list1.IsMultiLevel);
Assert.AreEqual(listStyle, list1.Style);

// Изменить внешний вид всех уровней списка в нашем списке.
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

// Добавьте несколько элементов списка, которые будут форматировать наш список.
builder.ListFormat.List = list2;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

builder.Writeln("Using list style second time:");

// Создаем и применяем другой список на основе стиля списка.
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
