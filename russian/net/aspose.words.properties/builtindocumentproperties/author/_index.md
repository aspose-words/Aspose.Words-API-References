---
title: BuiltInDocumentProperties.Author
second_title: Справочник по API Aspose.Words для .NET
description: BuiltInDocumentProperties свойство. Получает или задает имя автора документа.
type: docs
weight: 10
url: /ru/net/aspose.words.properties/builtindocumentproperties/author/
---
## BuiltInDocumentProperties.Author property

Получает или задает имя автора документа.

```csharp
public string Author { get; set; }
```

### Примеры

Показывает, как работать со встроенными свойствами документа в категории «Описание».

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;

// Ниже приведены четыре встроенных свойства документа, у которых есть поля, которые могут отображать свои значения в теле документа.
// 1 - свойство "Автор", которое мы можем отобразить с помощью поля AUTHOR:
properties.Author = "John Doe";
builder.Write("Author:\t");
builder.InsertField(FieldType.FieldAuthor, true);

// 2 - свойство "Название", которое мы можем отобразить с помощью поля TITLE:
properties.Title = "John's Document";
builder.Write("\nDoc title:\t");
builder.InsertField(FieldType.FieldTitle, true);

// 3 - свойство «Тема», которое мы можем отобразить с помощью поля ТЕМА:
properties.Subject = "My subject";
builder.Write("\nSubject:\t");
builder.InsertField(FieldType.FieldSubject, true);

// 4 - свойство "Комментарии", которое мы можем отобразить с помощью поля КОММЕНТАРИИ:
properties.Comments = $"This is {properties.Author}'s document about {properties.Subject}";
builder.Write("\nComments:\t\"");
builder.InsertField(FieldType.FieldComments, true);
builder.Write("\"");

// Встроенное свойство «Категория» не имеет поля, в котором можно отображать его значение.
properties.Category = "My category";

// Мы можем установить несколько ключевых слов для документа, разделив строковое значение свойства «Ключевые слова» точкой с запятой.
properties.Keywords = "Tag 1; Tag 2; Tag 3";

// Мы можем щелкнуть этот документ правой кнопкой мыши в проводнике Windows и найти эти свойства в «Свойствах» -> gt; "Подробности".
// Встроенное свойство «Автор» находится в группе «Происхождение», остальные — в группе «Описание».
doc.Save(ArtifactsDir + "DocumentProperties.Description.docx");
```

### Смотрите также

* class [BuiltInDocumentProperties](../)
* пространство имен [Aspose.Words.Properties](../../builtindocumentproperties/)
* сборка [Aspose.Words](../../../)


