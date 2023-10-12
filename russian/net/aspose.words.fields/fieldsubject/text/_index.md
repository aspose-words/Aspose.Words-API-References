---
title: FieldSubject.Text
second_title: Справочник по API Aspose.Words для .NET
description: FieldSubject свойство. Получает или задает текст темы.
type: docs
weight: 20
url: /ru/net/aspose.words.fields/fieldsubject/text/
---
## FieldSubject.Text property

Получает или задает текст темы.

```csharp
public string Text { get; set; }
```

### Примеры

Показывает, как использовать поле ТЕМА.

```csharp
Document doc = new Document();

// Установите значение для встроенного свойства документа «Тема».
doc.BuiltInDocumentProperties.Subject = "My subject";

// Создайте поле SUBJECT для отображения значения этого встроенного свойства.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldSubject field = (FieldSubject)builder.InsertField(FieldType.FieldSubject, true);
field.Update();

Assert.AreEqual(" SUBJECT ", field.GetFieldCode());
Assert.AreEqual("My subject", field.Result);

// Если мы зададим значение свойства Text поля SUBJECT и обновим его, поле будет
// перезаписываем текущее значение встроенного свойства «Тема» значением его свойства Text,
// и затем отображаем новое значение.
field.Text = "My new subject";
field.Update();

Assert.AreEqual(" SUBJECT  \"My new subject\"", field.GetFieldCode());
Assert.AreEqual("My new subject", field.Result);

Assert.AreEqual("My new subject", doc.BuiltInDocumentProperties.Subject);

doc.Save(ArtifactsDir + "Field.SUBJECT.docx");
```

### Смотрите также

* class [FieldSubject](../)
* пространство имен [Aspose.Words.Fields](../../fieldsubject/)
* сборка [Aspose.Words](../../../)


