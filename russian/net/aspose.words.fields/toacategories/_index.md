---
title: ToaCategories Class
linktitle: ToaCategories
articleTitle: ToaCategories
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Fields.ToaCategories для эффективного управления категориями таблиц авторитетов в ваших документах. Улучшите структурирование ваших документов!
type: docs
weight: 3190
url: /ru/net/aspose.words.fields/toacategories/
---
## ToaCategories class

Представляет таблицу категорий органов власти.

Чтобы узнать больше, посетите[Работа с полями](https://docs.aspose.com/words/net/working-with-fields/) документальная статья.

```csharp
public class ToaCategories
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [ToaCategories](toacategories/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| static [DefaultCategories](../../aspose.words.fields/toacategories/defaultcategories/) { get; } | Получает таблицу категорий органов власти по умолчанию. |
| [Item](../../aspose.words.fields/toacategories/item/) { get; set; } | Получает или задает заголовок категории по номеру категории. |

## Примеры

Показывает, как указать набор категорий для полей TOA.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Поля TOA могут фильтровать свои записи по категориям, определенным в этой коллекции.
ToaCategories toaCategories = new ToaCategories();
doc.FieldOptions.ToaCategories = toaCategories;

// Эта коллекция категорий имеет значения по умолчанию, которые мы можем перезаписать пользовательскими значениями.
Assert.AreEqual("Cases", toaCategories[1]);
Assert.AreEqual("Statutes", toaCategories[2]);

toaCategories[1] = "My Category 1";
toaCategories[2] = "My Category 2";

// Мы всегда можем получить доступ к значениям по умолчанию через эту коллекцию.
Assert.AreEqual("Cases", ToaCategories.DefaultCategories[1]);
Assert.AreEqual("Statutes", ToaCategories.DefaultCategories[2]);

// Вставить 2 поля TOA. Поля TOA создают запись для каждого поля TA в документе.
// Используйте переключатель "\c" для выбора индекса категории из нашей коллекции.
// С этим переключателем поле TOA будет выбирать только записи из полей TA, которые
// также есть переключатель "\c" с соответствующим индексом категории. Каждое поле TOA также будет отображать
// имя категории, на которую указывает переключатель "\c".
builder.InsertField("TOA \\c 1 \\h", null);
builder.InsertField("TOA \\c 2 \\h", null);
builder.InsertBreak(BreakType.PageBreak);

// Вставьте записи TOA в 2 категории. Наше первое поле TOA получит одну запись,
// из второго поля TA, переключатель "\c" которого также указывает на первую категорию.
// Второе поле TOA будет содержать две записи из двух других полей TA.
builder.InsertField("TA \\c 2 \\l \"entry 1\"");
builder.InsertBreak(BreakType.PageBreak);
builder.InsertField("TA \\c 1 \\l \"entry 2\"");
builder.InsertBreak(BreakType.PageBreak);
builder.InsertField("TA \\c 2 \\l \"entry 3\"");

doc.UpdateFields();
doc.Save(ArtifactsDir + "FieldOptions.TOA.Categories.docx");
```

### Смотрите также

* пространство имен [Aspose.Words.Fields](../../aspose.words.fields/)
* сборка [Aspose.Words](../../)
