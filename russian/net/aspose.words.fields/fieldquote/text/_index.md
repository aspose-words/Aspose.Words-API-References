---
title: FieldQuote.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words для .NET
description: Свойство FieldQuote Text. Легко извлекайте или устанавливайте текст для улучшенного управления данными. Оптимизируйте свой рабочий процесс с помощью этой мощной функции!
type: docs
weight: 20
url: /ru/net/aspose.words.fields/fieldquote/text/
---
## FieldQuote.Text property

Получает или задает текст для извлечения.

```csharp
public string Text { get; set; }
```

## Примеры

Показывает, как использовать поле ЦИТАТА.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте поле QUOTE, которое будет отображать значение его свойства Text.
FieldQuote field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
field.Text = "\"Quoted text\"";

Assert.AreEqual(" QUOTE  \"\\\"Quoted text\\\"\"", field.GetFieldCode());

// Вставьте поле ЦИТАТА и вложите в него поле ДАТА.
// Поля ДАТА обновляют свои значения на текущую дату каждый раз, когда мы открываем документ с помощью Microsoft Word.
// Вложение поля ДАТА в поле ЦИТАТА таким образом зафиксирует его значение
// на дату создания документа.
builder.Write("\nDocument creation date: ");
field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
builder.MoveTo(field.Separator);
builder.InsertField(FieldType.FieldDate, true);

Assert.AreEqual(" QUOTE \u0013 DATE \u0014" + DateTime.Now.Date.ToShortDateString() + "\u0015", field.GetFieldCode());

// Обновите все поля, чтобы отобразить правильные результаты.
doc.UpdateFields();

Assert.AreEqual("\"Quoted text\"", doc.Range.Fields[0].Result);

doc.Save(ArtifactsDir + "Field.QUOTE.docx");
```

### Смотрите также

* class [FieldQuote](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
