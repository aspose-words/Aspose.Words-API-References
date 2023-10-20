---
title: StyleCollection.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words для .NET
description: StyleCollection Add метод. Создает новый пользовательский стиль и добавляет его в коллекцию на С#.
type: docs
weight: 60
url: /ru/net/aspose.words/stylecollection/add/
---
## StyleCollection.Add method

Создает новый пользовательский стиль и добавляет его в коллекцию.

```csharp
public Style Add(StyleType type, string name)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| type | StyleType | А[`StyleType`](../../styletype/) значение, указывающее тип создаваемого стиля. |
| name | String | Имя создаваемого стиля с учетом регистра. |

## Примечания

Вы можете создать стиль символа, абзаца или списка.

При создании стиля списка стиль создается с форматированием нумерованного списка по умолчанию (1 \ a \ i).

Выдает исключение, если стиль с таким именем уже существует.

## Примеры

Показывает, как добавить стиль в коллекцию стилей документа.

```csharp
Document doc = new Document();

StyleCollection styles = doc.Styles;
// Устанавливаем параметры по умолчанию для новых стилей, которые мы можем позже добавить в эту коллекцию.
styles.DefaultFont.Name = "Courier New";
// Если мы добавим стиль StyleType.Paragraph, коллекция применит значения
// его свойство "DefaultParagraphFormat" к свойству стиля "ParagraphFormat".
styles.DefaultParagraphFormat.FirstLineIndent = 15.0;
// Добавляем стиль и проверяем, что для него заданы настройки по умолчанию.
styles.Add(StyleType.Paragraph, "MyStyle");

Assert.AreEqual("Courier New", styles[4].Font.Name);
Assert.AreEqual(15.0, styles["MyStyle"].ParagraphFormat.FirstLineIndent);
```

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

* class [Style](../../style/)
* enum [StyleType](../../styletype/)
* class [StyleCollection](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
