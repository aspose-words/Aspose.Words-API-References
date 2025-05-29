---
title: FieldComments.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words для .NET
description: Управляйте своими комментариями без усилий с помощью свойства FieldComments Text — легко получайте или задавайте текст комментария для улучшенного взаимодействия с пользователем.
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

// Задаем значение для встроенного свойства документа «Комментарии».
doc.BuiltInDocumentProperties.Comments = "My comment.";

// Создайте поле КОММЕНТАРИИ для отображения значения этого встроенного свойства.
FieldComments field = (FieldComments)builder.InsertField(FieldType.FieldComments, true);
field.Update();

Assert.AreEqual(" COMMENTS ", field.GetFieldCode());
Assert.AreEqual("My comment.", field.Result);

// Если мы зададим значение свойства Text поля COMMENTS и обновим его, поле будет
// перезаписать текущее значение встроенного свойства «Комментарии» значением его свойства Text,
// а затем отобразить новое значение.
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
