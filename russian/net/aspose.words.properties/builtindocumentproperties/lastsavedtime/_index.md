---
title: BuiltInDocumentProperties.LastSavedTime
linktitle: LastSavedTime
articleTitle: LastSavedTime
second_title: Aspose.Words для .NET
description: Откройте для себя свойство BuiltInDocumentProperties LastSavedTime, чтобы легко отслеживать время последнего сохранения вашего документа в формате UTC. Улучшите управление документами сегодня!
type: docs
weight: 180
url: /ru/net/aspose.words.properties/builtindocumentproperties/lastsavedtime/
---
## BuiltInDocumentProperties.LastSavedTime property

Возвращает или задает время последнего сохранения в формате UTC.

```csharp
public DateTime LastSavedTime { get; set; }
```

## Примечания

Для документов, созданных в формате RTF, это свойство возвращает локальное время последней операции сохранения.

Aspose.Words не обновляет это свойство.

## Примеры

Показывает, как работать со свойствами документа в категории «Источник».

```csharp
// Открываем документ, который мы создали и отредактировали с помощью Microsoft Word.
Document doc = new Document(MyDir + "Properties.docx");
BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;

// Следующие встроенные свойства содержат информацию, касающуюся создания и редактирования этого документа.
// Мы можем щелкнуть правой кнопкой мыши этот документ в проводнике Windows и найти
// эти свойства через категорию «Свойства» -> «Подробности» -> «Происхождение».
// Такие поля, как PRINTDATE и EDITTIME, могут отображать эти значения в теле документа.
Console.WriteLine($"Created using {properties.NameOfApplication}, on {properties.CreatedTime}");
Console.WriteLine($"Minutes spent editing: {properties.TotalEditingTime}");
Console.WriteLine($"Date/time last printed: {properties.LastPrinted}");
Console.WriteLine($"Template document: {properties.Template}");

// Мы также можем изменять значения встроенных свойств.
properties.Company = "Doe Ltd.";
properties.Manager = "Jane Doe";
properties.Version = 5;
properties.RevisionNumber++;

// Microsoft Word автоматически обновляет следующие свойства при сохранении документа.
// Чтобы использовать эти свойства с Aspose.Words, нам нужно будет задать для них значения вручную.
properties.LastSavedBy = "John Doe";
properties.LastSavedTime = DateTime.Now;

// Мы можем щелкнуть правой кнопкой мыши этот документ в проводнике Windows и найти these properties in "Properties" -> "Details" -> "Origin".
doc.Save(ArtifactsDir + "DocumentProperties.Origin.docx");
```

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

* class [BuiltInDocumentProperties](../)
* пространство имен [Aspose.Words.Properties](../../../aspose.words.properties/)
* сборка [Aspose.Words](../../../)
