---
title: FieldComments.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words для .NET
description: FieldComments Text свойство. Получает или задает текст комментариев на С#.
type: docs
weight: 20
url: /ru/net/aspose.words.fields/fieldcomments/text/
---
## FieldComments.Text property

Получает или задает текст комментариев.

```csharp
public string Text { get; set; }
```

## Примеры

Показывает, как использовать поле КОММЕНТАРИИ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Устанавливаем значение для встроенного свойства документа «Комментарии».
doc.BuiltInDocumentProperties.Comments = "My comment.";

// Создайте поле КОММЕНТАРИЙ для отображения значения этого встроенного свойства.
FieldComments field = (FieldComments)builder.InsertField(FieldType.FieldComments, true);
field.Update();

Assert.AreEqual(" COMMENTS ", field.GetFieldCode());
Assert.AreEqual("My comment.", field.Result);

// Если мы зададим значение свойства Text поля COMMENTS и обновим его, поле будет
// перезаписываем текущее значение встроенного свойства «Комментарии» значением его свойства Text,
// и затем отображаем новое значение.
field.Text = "My overriding comment.";
field.Update();

Assert.AreEqual(" COMMENTS  \"My overriding comment.\"", field.GetFieldCode());
Assert.AreEqual("My overriding comment.", field.Result);

doc.Save(ArtifactsDir + "Field.COMMENTS.docx");
```

### Смотрите также

* class [FieldComments](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
