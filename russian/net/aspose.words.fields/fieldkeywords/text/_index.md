---
title: FieldKeywords.Text
second_title: Справочник по API Aspose.Words для .NET
description: FieldKeywords свойство. Получает или задает текст ключевых слов.
type: docs
weight: 20
url: /ru/net/aspose.words.fields/fieldkeywords/text/
---
## FieldKeywords.Text property

Получает или задает текст ключевых слов.

```csharp
public string Text { get; set; }
```

### Примеры

Показывает, что нужно вставить поле КЛЮЧЕВЫЕ СЛОВА.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Добавьте несколько ключевых слов, также называемых «тегами» в проводнике.
doc.BuiltInDocumentProperties.Keywords = "Keyword1, Keyword2";

// Поле KEYWORDS отображает значение этого свойства.
FieldKeywords field = (FieldKeywords)builder.InsertField(FieldType.FieldKeyword, true);
field.Update();

Assert.AreEqual(" KEYWORDS ", field.GetFieldCode());
Assert.AreEqual("Keyword1, Keyword2", field.Result);

// Установка значения свойства Text поля,
// а затем обновление поля также перезапишет соответствующее встроенное свойство новым значением.
field.Text = "OverridingKeyword";
field.Update();

Assert.AreEqual(" KEYWORDS  OverridingKeyword", field.GetFieldCode());
Assert.AreEqual("OverridingKeyword", field.Result);
Assert.AreEqual("OverridingKeyword", doc.BuiltInDocumentProperties.Keywords);

doc.Save(ArtifactsDir + "Field.KEYWORDS.docx");
```

### Смотрите также

* class [FieldKeywords](../)
* пространство имен [Aspose.Words.Fields](../../fieldkeywords/)
* сборка [Aspose.Words](../../../)


