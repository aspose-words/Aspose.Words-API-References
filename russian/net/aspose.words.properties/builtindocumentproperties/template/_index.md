---
title: BuiltInDocumentProperties.Template
linktitle: Template
articleTitle: Template
second_title: Aspose.Words для .NET
description: Откройте для себя функцию шаблона BuiltInDocumentProperties, которая позволит легко управлять информационным названием документа для лучшей организации и эффективности.
type: docs
weight: 300
url: /ru/net/aspose.words.properties/builtindocumentproperties/template/
---
## BuiltInDocumentProperties.Template property

Возвращает или задает информационное имя шаблона документа.

```csharp
public string Template { get; set; }
```

## Примечания

В Microsoft Word это свойство предназначено только для информационных целей, а обычно содержит только имя файла шаблона без пути.

Пустая строка означает, что документ прикреплен к шаблону Normal.

Чтобы получить или задать фактическое имя прикрепленного шаблона, используйте the [`AttachedTemplate`](../../../aspose.words/document/attachedtemplate/) свойство.

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
