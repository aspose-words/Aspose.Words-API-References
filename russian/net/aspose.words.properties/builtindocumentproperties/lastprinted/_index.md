---
title: BuiltInDocumentProperties.LastPrinted
linktitle: LastPrinted
articleTitle: LastPrinted
second_title: Aspose.Words для .NET
description: Откройте для себя функцию BuiltInDocumentProperties LastPrinted, чтобы легко отслеживать дату последней печати вашего документа в формате UTC. Улучшите свой рабочий процесс сегодня!
type: docs
weight: 160
url: /ru/net/aspose.words.properties/builtindocumentproperties/lastprinted/
---
## BuiltInDocumentProperties.LastPrinted property

Возвращает или задает дату последней печати документа в формате UTC.

```csharp
public DateTime LastPrinted { get; set; }
```

## Примечания

Для документов в формате RTF это свойство возвращает локальное время последней операции печати.

Если документ никогда не был напечатан, это свойство вернет DateTime.MinValue.

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

### Смотрите также

* class [BuiltInDocumentProperties](../)
* пространство имен [Aspose.Words.Properties](../../../aspose.words.properties/)
* сборка [Aspose.Words](../../../)
