---
title: FieldAuthor.AuthorName
linktitle: AuthorName
articleTitle: AuthorName
second_title: Aspose.Words для .NET
description: Управляйте авторами документов без усилий с помощью FieldAuthor AuthorName. Легко получайте или устанавливайте имена авторов, чтобы повысить надежность и организацию вашего контента.
type: docs
weight: 20
url: /ru/net/aspose.words.fields/fieldauthor/authorname/
---
## FieldAuthor.AuthorName property

Возвращает или задает имя автора документа.

```csharp
public string AuthorName { get; set; }
```

## Примеры

Показывает, как использовать поле AUTHOR для отображения имени создателя документа.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Поля AUTHOR берут свои результаты из встроенного свойства документа под названием «Автор».
// Если мы создадим и сохраним документ в Microsoft Word,
// в этом свойстве будет наше имя пользователя.
// Однако, если мы создадим документ программно с помощью Aspose.Words,
// свойство «Автор» по умолчанию будет пустой строкой.
Assert.AreEqual(string.Empty, doc.BuiltInDocumentProperties.Author);

// Задайте резервное имя автора для полей AUTHOR для использования
// если свойство «Автор» содержит пустую строку.
doc.FieldOptions.DefaultDocumentAuthor = "Joe Bloggs";

builder.Write("This document was created by ");
FieldAuthor field = (FieldAuthor)builder.InsertField(FieldType.FieldAuthor, true);
field.Update();

Assert.AreEqual(" AUTHOR ", field.GetFieldCode());
Assert.AreEqual("Joe Bloggs", field.Result);

// Обновление поля AUTHOR, содержащего значение
// применит это значение к встроенному свойству «Автор».
Assert.AreEqual("Joe Bloggs", doc.BuiltInDocumentProperties.Author);

// Изменение этого свойства и последующее обновление поля AUTHOR применит это значение к полю.
doc.BuiltInDocumentProperties.Author = "John Doe";
field.Update();

Assert.AreEqual(" AUTHOR ", field.GetFieldCode());
Assert.AreEqual("John Doe", field.Result);

// Если мы обновим поле AUTHOR после изменения его свойства «Имя»,
// тогда поле отобразит новое имя и применит новое имя к встроенному свойству.
field.AuthorName = "Jane Doe";
field.Update();

Assert.AreEqual(" AUTHOR  \"Jane Doe\"", field.GetFieldCode());
Assert.AreEqual("Jane Doe", field.Result);

// Поля AUTHOR не влияют на свойство DefaultDocumentAuthor.
Assert.AreEqual("Jane Doe", doc.BuiltInDocumentProperties.Author);
Assert.AreEqual("Joe Bloggs", doc.FieldOptions.DefaultDocumentAuthor);

doc.Save(ArtifactsDir + "Field.AUTHOR.docx");
```

### Смотрите также

* class [FieldAuthor](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
