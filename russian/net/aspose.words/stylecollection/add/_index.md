---
title: StyleCollection.Add
second_title: Справочник по API Aspose.Words для .NET
description: StyleCollection метод. Создает новый пользовательский стиль и добавляет его в коллекцию.
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
| name | String | Регистрозависимое имя создаваемого стиля. |

### Примечания

Вы можете создать символ, абзац или стиль списка.

При создании стиля списка стиль создается с форматированием нумерованного списка по умолчанию (1 \ a \ i).

Выдает исключение, если стиль с таким именем уже существует.

### Примеры

Показывает, как добавить стиль в коллекцию стилей документа.

```csharp
Document doc = new Document();
StyleCollection styles = doc.Styles;

// Задаем параметры по умолчанию для новых стилей, которые позже мы можем добавить в эту коллекцию.
styles.DefaultFont.Name = "Courier New";

// Если мы добавим стиль "StyleType.Paragraph", коллекция применит значения
// его свойство "DefaultParagraphFormat" к свойству "ParagraphFormat" стиля.
styles.DefaultParagraphFormat.FirstLineIndent = 15.0;

// Добавьте стиль, а затем убедитесь, что он имеет настройки по умолчанию.
styles.Add(StyleType.Paragraph, "MyStyle");

Assert.AreEqual("Courier New", styles[4].Font.Name);
Assert.AreEqual(15.0, styles["MyStyle"].ParagraphFormat.FirstLineIndent);
```

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

* class [Style](../../style/)
* enum [StyleType](../../styletype/)
* class [StyleCollection](../)
* пространство имен [Aspose.Words](../../stylecollection/)
* сборка [Aspose.Words](../../../)


