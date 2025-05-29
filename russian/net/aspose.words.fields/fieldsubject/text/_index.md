---
title: FieldSubject.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words для .NET
description: Управляйте свойством FieldSubject Text с легкостью — получайте или задавайте текст темы для бесперебойной обработки данных и улучшения пользовательского опыта.
type: docs
weight: 20
url: /ru/net/aspose.words.fields/fieldsubject/text/
---
## FieldSubject.Text property

Получает или задает текст темы.

```csharp
public string Text { get; set; }
```

## Примеры

Показывает, как использовать поле ТЕМА.

```csharp
Document doc = new Document();

// Задаем значение для встроенного свойства документа «Тема».
doc.BuiltInDocumentProperties.Subject = "My subject";

// Создайте поле SUBJECT для отображения значения этого встроенного свойства.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldSubject field = (FieldSubject)builder.InsertField(FieldType.FieldSubject, true);
field.Update();

Assert.AreEqual(" SUBJECT ", field.GetFieldCode());
Assert.AreEqual("My subject", field.Result);

// Если мы зададим значение свойства Text поля SUBJECT и обновим его, поле будет
// перезаписать текущее значение встроенного свойства "Тема" значением его свойства Текст,
// а затем отобразить новое значение.
field.Text = "My new subject";
field.Update();

Assert.AreEqual(" SUBJECT  \"My new subject\"", field.GetFieldCode());
Assert.AreEqual("My new subject", field.Result);

Assert.AreEqual("My new subject", doc.BuiltInDocumentProperties.Subject);

doc.Save(ArtifactsDir + "Field.SUBJECT.docx");
```

### Смотрите также

* class [FieldSubject](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
