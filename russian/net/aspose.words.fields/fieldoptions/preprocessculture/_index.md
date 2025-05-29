---
title: FieldOptions.PreProcessCulture
linktitle: PreProcessCulture
articleTitle: PreProcessCulture
second_title: Aspose.Words для .NET
description: Узнайте, как FieldOptions PreProcessCulture улучшает обработку данных, настраивая культуры значений полей для повышения точности и эффективности.
type: docs
weight: 170
url: /ru/net/aspose.words.fields/fieldoptions/preprocessculture/
---
## FieldOptions.PreProcessCulture property

Возвращает или задает культуру для предварительной обработки значений полей.

```csharp
public CultureInfo PreProcessCulture { get; set; }
```

## Примечания

В настоящее время это свойство влияет только на стоимость[`FieldDocProperty`](../../fielddocproperty/) поле.

Значение по умолчанию:`нулевой` . Когда это свойство установлено в`нулевой` ,[`FieldDocProperty`](../../fielddocproperty/) Значение поля preprocessed с региональными параметрами, контролируемыми[`FieldUpdateCultureSource`](../fieldupdateculturesource/) свойство.

## Примеры

Показывает, как настроить культуру предварительной обработки.

```csharp
Document doc = new Document(MyDir + "Document.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

// Установите культуру, в соответствии с которой некоторые поля будут форматировать отображаемые значения.
doc.FieldOptions.PreProcessCulture = new CultureInfo("de-DE");

Field field = builder.InsertField(" DOCPROPERTY CreateTime");

// Поле DOCPROPERTY отобразит результат, отформатированный в соответствии с культурой предварительной обработки
// мы установили немецкий. Поле будет отображать дату/время в формате "dd.mm.yyyy hh:mm".
Assert.IsTrue(Regex.Match(field.Result, @"\d{2}[.]\d{2}[.]\d{4} \d{2}[:]\d{2}").Success);

doc.FieldOptions.PreProcessCulture = CultureInfo.InvariantCulture;
field.Update();

// После переключения на инвариантную культуру поле DOCPROPERTY будет использовать формат «мм/дд/гггг чч:мм».
Assert.IsTrue(Regex.Match(field.Result, @"\d{2}[/]\d{2}[/]\d{4} \d{2}[:]\d{2}").Success);
```

### Смотрите также

* class [FieldOptions](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
