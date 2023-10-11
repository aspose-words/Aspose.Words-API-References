---
title: FieldOptions.PreProcessCulture
second_title: Справочник по API Aspose.Words для .NET
description: FieldOptions свойство. Получает или задает язык и региональные параметры для предварительной обработки значений полей.
type: docs
weight: 170
url: /ru/net/aspose.words.fields/fieldoptions/preprocessculture/
---
## FieldOptions.PreProcessCulture property

Получает или задает язык и региональные параметры для предварительной обработки значений полей.

```csharp
public CultureInfo PreProcessCulture { get; set; }
```

### Примечания

В настоящее время это свойство влияет только на стоимость[`FieldDocProperty`](../../fielddocproperty/) поле.

Значение по умолчанию:`нулевой` . Когда для этого свойства установлено значение`нулевой` ,[`FieldDocProperty`](../../fielddocproperty/)значение поля — preprocessed с культурой, контролируемой[`FieldUpdateCultureSource`](../fieldupdateculturesource/) свойство.

### Примеры

Показывает, как установить культуру предварительной обработки.

```csharp
Document doc = new Document(MyDir + "Document.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

// Установите культуру, в соответствии с которой некоторые поля будут форматировать отображаемые значения.
doc.FieldOptions.PreProcessCulture = new CultureInfo("de-DE");

Field field = builder.InsertField(" DOCPROPERTY CreateTime");

// Поле DOCPROPERTY отобразит результат, отформатированный в соответствии с культурой предварительной обработки.
// мы установили немецкий язык. В поле будет отображаться дата/время в формате «дд.мм.гггг чч:мм».
Assert.IsTrue(Regex.Match(field.Result, @"\d{2}[.]\d{2}[.]\d{4} \d{2}[:]\d{2}").Success);

doc.FieldOptions.PreProcessCulture = CultureInfo.InvariantCulture;
field.Update();

// После переключения на инвариантный язык и региональные параметры поле DOCPROPERTY будет использовать формат «мм/дд/гггг чч:мм».
Assert.IsTrue(Regex.Match(field.Result, @"\d{2}[/]\d{2}[/]\d{4} \d{2}[:]\d{2}").Success);
```

### Смотрите также

* class [FieldOptions](../)
* пространство имен [Aspose.Words.Fields](../../fieldoptions/)
* сборка [Aspose.Words](../../../)


