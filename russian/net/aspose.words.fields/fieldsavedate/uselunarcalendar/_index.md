---
title: FieldSaveDate.UseLunarCalendar
linktitle: UseLunarCalendar
articleTitle: UseLunarCalendar
second_title: Aspose.Words для .NET
description: Свойство UseLunarCalendar объекта FieldSaveDate позволяет легко переключаться между лунным календарем Хиджры и еврейским лунным календарем для удобного управления датами.
type: docs
weight: 20
url: /ru/net/aspose.words.fields/fieldsavedate/uselunarcalendar/
---
## FieldSaveDate.UseLunarCalendar property

Возвращает или задает, использовать ли лунный календарь Хиджры или еврейский лунный календарь.

```csharp
public bool UseLunarCalendar { get; set; }
```

## Примеры

Показывает, как использовать поле SAVEDATE для отображения даты/времени последней операции сохранения документа, выполненной с помощью Microsoft Word.

```csharp
Document doc = new Document(MyDir + "Document.docx");
DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.Writeln(" Date this document was last saved:");

// Мы можем использовать поле SAVEDATE для отображения даты и времени последней операции сохранения в документе.
// Операция сохранения, на которую ссылаются эти поля, — это ручное сохранение в приложении, например Microsoft Word,
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

// Поля SAVEDATE берут свои значения даты/времени из встроенного свойства LastSavedTime.
// Метод Save документа не обновит это значение, но мы все равно можем обновить его вручную.
doc.BuiltInDocumentProperties.LastSavedTime = DateTime.Now;

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.SAVEDATE.docx");
```

### Смотрите также

* class [FieldSaveDate](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
