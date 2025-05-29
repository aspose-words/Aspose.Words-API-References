---
title: FieldKeywords.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words для .NET
description: Управляйте своими FieldKeywords с легкостью! Получайте доступ и настраивайте текст ключевых слов для оптимальной производительности SEO и улучшения видимости.
type: docs
weight: 20
url: /ru/net/aspose.words.fields/fieldkeywords/text/
---
## FieldKeywords.Text property

Получает или задает текст ключевых слов.

```csharp
public string Text { get; set; }
```

## Примеры

Показывает, как вставить поле КЛЮЧЕВЫЕ СЛОВА.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Добавьте несколько ключевых слов, также называемых «тегами» в Проводнике.
doc.BuiltInDocumentProperties.Keywords = "Keyword1, Keyword2";

// Поле КЛЮЧЕВЫЕ СЛОВА отображает значение этого свойства.
FieldKeywords field = (FieldKeywords)builder.InsertField(FieldType.FieldKeyword, true);
field.Update();

Assert.AreEqual(" KEYWORDS ", field.GetFieldCode());
Assert.AreEqual("Keyword1, Keyword2", field.Result);

// Установка значения для свойства Text поля,
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
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
