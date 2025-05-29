---
title: ToaCategories.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words для .NET
description: Управляйте своими элементами ToaCategories без усилий. Легко устанавливайте и извлекайте заголовки категорий по номеру для упрощенной организации и эффективности.
type: docs
weight: 30
url: /ru/net/aspose.words.fields/toacategories/item/
---
## ToaCategories indexer

Получает или задает заголовок категории по номеру категории.

```csharp
public string this[int number] { get; set; }
```

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

* class [ToaCategories](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
