---
title: BuiltInDocumentProperties.Manager
linktitle: Manager
articleTitle: Manager
second_title: Aspose.Words для .NET
description: Легко управляйте BuiltInDocumentProperties с помощью нашего интуитивно понятного инструмента. Легко получайте или устанавливайте свойства, чтобы улучшить свой опыт работы с документами.
type: docs
weight: 210
url: /ru/net/aspose.words.properties/builtindocumentproperties/manager/
---
## BuiltInDocumentProperties.Manager property

Получает или задает свойство менеджера.

```csharp
public string Manager { get; set; }
```

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
