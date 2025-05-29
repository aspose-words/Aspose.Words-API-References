---
title: List.Style
linktitle: Style
articleTitle: Style
second_title: Aspose.Words для .NET
description: Откройте для себя свойство List Style, чтобы эффективно определять и настраивать ваши списки. Улучшите свой веб-дизайн с помощью уникальных вариантов стилей!
type: docs
weight: 80
url: /ru/net/aspose.words.lists/list/style/
---
## List.Style property

Получает стиль списка, на который ссылается или который определяет этот список.

```csharp
public Style Style { get; }
```

## Примечания

Если этот список не связан со стилем списка, свойство вернет`нулевой`.

Список может быть ссылкой на стиль списка, в данном случае[`IsListStyleReference`](../isliststylereference/) будет`истинный`.

Список может быть определением стиля списка, в данном случае[`IsListStyleDefinition`](../isliststyledefinition/) будет`истинный`. Такой список нельзя применить к абзацам документа напрямую.

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

* class [Style](../../../aspose.words/style/)
* class [List](../)
* пространство имен [Aspose.Words.Lists](../../../aspose.words.lists/)
* сборка [Aspose.Words](../../../)
