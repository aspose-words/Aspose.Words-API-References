---
title: BuiltInDocumentProperties.RevisionNumber
linktitle: RevisionNumber
articleTitle: RevisionNumber
second_title: Aspose.Words для .NET
description: Управляйте RevisionNumber вашего документа с помощью BuiltInDocumentProperties. Легко отслеживайте изменения и улучшайте контроль версий для лучшего сотрудничества.
type: docs
weight: 250
url: /ru/net/aspose.words.properties/builtindocumentproperties/revisionnumber/
---
## BuiltInDocumentProperties.RevisionNumber property

Возвращает или задает номер версии документа.

```csharp
public int RevisionNumber { get; set; }
```

## Примечания

Aspose.Words не обновляет это свойство.

## Примеры

Показывает, как работать с полями REVNUM.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Current revision #");

// Вставьте поле REVNUM, которое отображает текущее свойство номера редакции документа.
FieldRevNum field = (FieldRevNum)builder.InsertField(FieldType.FieldRevisionNum, true);

Assert.AreEqual(" REVNUM ", field.GetFieldCode());
Assert.AreEqual("1", field.Result);
Assert.AreEqual(1, doc.BuiltInDocumentProperties.RevisionNumber);

// Это свойство подсчитывает, сколько раз документ был сохранен в Microsoft Word,
// и не имеет отношения к отслеживаемым ревизиям. Мы можем найти его, щелкнув правой кнопкой мыши по документу в проводнике Windows
// через Свойства -> Подробности. Мы можем обновить это свойство вручную.
doc.BuiltInDocumentProperties.RevisionNumber++;
field.Update();

Assert.AreEqual("2", field.Result);
```

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
