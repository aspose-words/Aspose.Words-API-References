---
title: FieldOptions.PreProcessCulture
second_title: Справочник по API Aspose.Words для .NET
description: FieldOptions свойство. Получает или задает культуру для предварительной обработки значений поля.
type: docs
weight: 150
url: /ru/net/aspose.words.fields/fieldoptions/preprocessculture/
---
## FieldOptions.PreProcessCulture property

Получает или задает культуру для предварительной обработки значений поля.

```csharp
public CultureInfo PreProcessCulture { get; set; }
```

### Примечания

В настоящее время это свойство влияет только на значение[`FieldDocProperty`](../../fielddocproperty/) поле.

Значение по умолчанию **нулевой** . Когда это свойство установлено в **нулевой** ,[`FieldDocProperty`](../../fielddocproperty/) значение поля предварительно обработано с культурой, контролируемой[`FieldUpdateCultureSource`](../fieldupdateculturesource/) имущество.

### Примеры

Показывает, как установить культуру предварительной обработки.

```csharp
Document doc = new Document(MyDir + "Document.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

// Установите культуру, в соответствии с которой некоторые поля будут форматировать отображаемые значения.
doc.FieldOptions.PreProcessCulture = new CultureInfo("de-DE");

Field field = builder.InsertField(" DOCPROPERTY CreateTime");

// В поле DOCPROPERTY отобразится результат, отформатированный в соответствии с культурой предварительной обработки
// мы установили немецкий язык. Поле будет отображать дату/время в формате «дд.мм.гггг чч:мм».
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


