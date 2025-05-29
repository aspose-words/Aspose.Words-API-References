---
title: StyleCollection.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words для .NET
description: Откройте для себя метод StyleCollection Add, который позволит вам легко создавать и добавлять пользовательские стили в свою коллекцию, повышая гибкость дизайна.
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
| type | StyleType | А[`StyleType`](../../styletype/) значение, определяющее тип создаваемого стиля. |
| name | String | Имя создаваемого стиля чувствительно к регистру. |

## Примечания

Вы можете создать стиль символа, абзаца или списка.

При создании стиля списка стиль создается с форматированием нумерованного списка по умолчанию (1 \ a \ i).

Выдает исключение, если стиль с таким именем уже существует.

## Примеры

Показывает, как добавить стиль в коллекцию стилей документа.

```csharp
Document doc = new Document();

StyleCollection styles = doc.Styles;
// Устанавливаем параметры по умолчанию для новых стилей, которые мы позже можем добавить в эту коллекцию.
styles.DefaultFont.Name = "Courier New";
// Если мы добавим стиль "StyleType.Paragraph", коллекция применит значения
// его свойство "DefaultParagraphFormat" к свойству "ParagraphFormat" стиля.
styles.DefaultParagraphFormat.FirstLineIndent = 15.0;
// Добавьте стиль, а затем проверьте, что у него настройки по умолчанию.
styles.Add(StyleType.Paragraph, "MyStyle");

Assert.AreEqual("Courier New", styles[4].Font.Name);
Assert.AreEqual(15.0, styles["MyStyle"].ParagraphFormat.FirstLineIndent);
```

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

* class [Style](../../style/)
* enum [StyleType](../../styletype/)
* class [StyleCollection](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
