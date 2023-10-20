---
title: FieldSaveDate.UseLunarCalendar
linktitle: UseLunarCalendar
articleTitle: UseLunarCalendar
second_title: Aspose.Words для .NET
description: FieldSaveDate UseLunarCalendar свойство. Получает или задает следует ли использовать лунный календарь Хиджры или еврейский лунный календарь на С#.
type: docs
weight: 20
url: /ru/net/aspose.words.fields/fieldsavedate/uselunarcalendar/
---
## FieldSaveDate.UseLunarCalendar property

Получает или задает, следует ли использовать лунный календарь Хиджры или еврейский лунный календарь.

```csharp
public bool UseLunarCalendar { get; set; }
```

## Примеры

Показывает, как использовать поле SAVEDATE для отображения даты и времени последней операции сохранения документа, выполненной с помощью Microsoft Word.

```csharp
Document doc = new Document(MyDir + "Document.docx");
DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.Writeln(" Date this document was last saved:");

// Мы можем использовать поле SAVEDATE для отображения даты и времени последней операции сохранения в документе.
// Операция сохранения, на которую ссылаются эти поля, представляет собой сохранение вручную в таком приложении, как Microsoft Word,
// не метод Save документа.
// Ниже приведены три различных типа календаря, в соответствии с которыми поле SAVEDATE может отображать дату/время.
// 1 - Исламский лунный календарь:
builder.Write("According to the Lunar Calendar - ");
FieldSaveDate field = (FieldSaveDate)builder.InsertField(FieldType.FieldSaveDate, true);
field.UseLunarCalendar = true;

Assert.AreEqual(" SAVEDATE  \\h", field.GetFieldCode());

// 2 - Календарь Умм аль-Кура:
builder.Write("\nAccording to the Umm al-Qura calendar - ");
field = (FieldSaveDate)builder.InsertField(FieldType.FieldSaveDate, true);
field.UseUmAlQuraCalendar = true;

Assert.AreEqual(" SAVEDATE  \\u", field.GetFieldCode());

// 3 - Индийский национальный календарь:
builder.Write("\nAccording to the Indian National calendar - ");
field = (FieldSaveDate)builder.InsertField(FieldType.FieldSaveDate, true);
field.UseSakaEraCalendar = true;

Assert.AreEqual(" SAVEDATE  \\s", field.GetFieldCode());

// Поля SAVEDATE получают значения даты и времени из встроенного свойства LastSavedTime.
// Метод Save документа не обновит это значение, но мы все равно можем обновить его вручную.
doc.BuiltInDocumentProperties.LastSavedTime = DateTime.Now;

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.SAVEDATE.docx");
```

### Смотрите также

* class [FieldSaveDate](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
