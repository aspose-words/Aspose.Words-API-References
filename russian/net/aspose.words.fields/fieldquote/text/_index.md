---
title: FieldQuote.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words для .NET
description: FieldQuote Text свойство. Получает или задает извлекаемый текст на С#.
type: docs
weight: 20
url: /ru/net/aspose.words.fields/fieldquote/text/
---
## FieldQuote.Text property

Получает или задает извлекаемый текст.

```csharp
public string Text { get; set; }
```

## Примеры

Показывает использование поля ЦИТАТЫ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставляем поле ЦИТАТЫ, в котором будет отображаться значение свойства Text.
FieldQuote field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
field.Text = "\"Quoted text\"";

Assert.AreEqual(" QUOTE  \"\\\"Quoted text\\\"\"", field.GetFieldCode());

// Вставляем поле ЦИТАТЫ и вставляем в него поле ДАТЫ.
// Поля ДАТА обновляют свое значение до текущей даты каждый раз, когда мы открываем документ с помощью Microsoft Word.
// Вложение поля ДАТА в поле ЦИТАТЫ, подобное этому, заморозит его значение
// к дате создания документа.
builder.Write("\nDocument creation date: ");
field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
builder.MoveTo(field.Separator);
builder.InsertField(FieldType.FieldDate, true);

Assert.AreEqual(" QUOTE \u0013 DATE \u0014" + DateTime.Now.Date.ToShortDateString() + "\u0015", field.GetFieldCode());

// Обновляем все поля, чтобы отображать правильные результаты.
doc.UpdateFields();

Assert.AreEqual("\"Quoted text\"", doc.Range.Fields[0].Result);

doc.Save(ArtifactsDir + "Field.QUOTE.docx");
```

### Смотрите также

* class [FieldQuote](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
