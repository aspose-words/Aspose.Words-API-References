---
title: ToaCategories.DefaultCategories
linktitle: DefaultCategories
articleTitle: DefaultCategories
second_title: Aspose.Words для .NET
description: ToaCategories DefaultCategories свойство. Получает таблицу категорий полномочий по умолчанию на С#.
type: docs
weight: 20
url: /ru/net/aspose.words.fields/toacategories/defaultcategories/
---
## ToaCategories.DefaultCategories property

Получает таблицу категорий полномочий по умолчанию.

```csharp
public static ToaCategories DefaultCategories { get; }
```

## Примечания

Используйте[`ToaCategories`](../../fieldoptions/toacategories/) свойство для указания таблицы категорий полномочий для одного документа.

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

// Вставляем 2 поля TOA. Поля TOA создают запись для каждого поля TA в документе.
// Используйте переключатель «\c», чтобы выбрать индекс категории из нашей коллекции.
// С помощью этого переключателя поле TOA будет выбирать только записи из полей TA, которые
// также есть переключатель "\c" с соответствующим индексом категории. В каждом поле TOA также будет отображаться
// имя категории, на которую указывает переключатель "\c".
builder.InsertField("TOA \\c 1 \\h", null);
builder.InsertField("TOA \\c 2 \\h", null);
builder.InsertBreak(BreakType.PageBreak);

// Вставляем записи TOA в две категории. Наше первое поле TOA получит одну запись:
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

* class [ToaCategories](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
