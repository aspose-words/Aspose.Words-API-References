---
title: BuiltInDocumentProperties.Keywords
linktitle: Keywords
articleTitle: Keywords
second_title: Aspose.Words для .NET
description: Улучшите свои документы с помощью BuiltInDocumentProperties. Легко управляйте ключевыми словами, чтобы улучшить поиск и организацию для лучшей производительности.
type: docs
weight: 150
url: /ru/net/aspose.words.properties/builtindocumentproperties/keywords/
---
## BuiltInDocumentProperties.Keywords property

Получает или задает ключевые слова документа.

```csharp
public string Keywords { get; set; }
```

## Примеры

Показывает, как работать со встроенными свойствами документа в категории «Описание».

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;

// Ниже приведены четыре встроенных свойства документа, имеющие поля, значения которых могут отображаться в теле документа.
// 1 - свойство «Автор», которое мы можем отобразить с помощью поля AUTHOR:
properties.Author = "John Doe";
builder.Write("Author:\t");
builder.InsertField(FieldType.FieldAuthor, true);

// 2 - Свойство "Title", которое мы можем отобразить с помощью поля TITLE:
properties.Title = "John's Document";
builder.Write("\nDoc title:\t");
builder.InsertField(FieldType.FieldTitle, true);

// 3 - Свойство «Тема», которое мы можем отобразить с помощью поля SUBJECT:
properties.Subject = "My subject";
builder.Write("\nSubject:\t");
builder.InsertField(FieldType.FieldSubject, true);

// 4 - Свойство "Комментарии", которое мы можем отобразить с помощью поля КОММЕНТАРИИ:
properties.Comments = $"This is {properties.Author}'s document about {properties.Subject}";
builder.Write("\nComments:\t\"");
builder.InsertField(FieldType.FieldComments, true);
builder.Write("\"");

// Встроенное свойство «Категория» не имеет поля, в котором можно отобразить его значение.
properties.Category = "My category";

// Мы можем задать несколько ключевых слов для документа, разделив строковое значение свойства «Ключевые слова» точками с запятой.
properties.Keywords = "Tag 1; Tag 2; Tag 3";

// Мы можем щелкнуть правой кнопкой мыши по этому документу в проводнике Windows и найти эти свойства в разделе «Свойства» -> «Подробности».
// Встроенное свойство «Автор» находится в группе «Происхождение», а остальные — в группе «Описание».
doc.Save(ArtifactsDir + "DocumentProperties.Description.docx");
```

### Смотрите также

* class [BuiltInDocumentProperties](../)
* пространство имен [Aspose.Words.Properties](../../../aspose.words.properties/)
* сборка [Aspose.Words](../../../)
