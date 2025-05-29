---
title: SaveOptions.UpdateLastSavedTimeProperty
linktitle: UpdateLastSavedTimeProperty
articleTitle: UpdateLastSavedTimeProperty
second_title: Aspose.Words для .NET
description: Оптимизируйте параметры сохранения с помощью свойства UpdateLastSavedTime. Контролируйте обновления LastSavedTime для эффективного управления данными и повышения производительности.
type: docs
weight: 190
url: /ru/net/aspose.words.saving/saveoptions/updatelastsavedtimeproperty/
---
## SaveOptions.UpdateLastSavedTimeProperty property

Возвращает или задает значение, определяющее, является ли[`LastSavedTime`](../../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) свойство обновляется перед сохранением.

```csharp
public bool UpdateLastSavedTimeProperty { get; set; }
```

## Примеры

Показывает, как определить, следует ли сохранять свойство документа «Время последнего сохранения» при сохранении.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Assert.AreEqual(new DateTime(2021, 5, 11, 6, 32, 0), 
    doc.BuiltInDocumentProperties.LastSavedTime);

// Когда мы сохраняем документ в формате OOXML, мы можем создать объект OoxmlSaveOptions
// а затем передаем его в метод сохранения документа, чтобы изменить способ сохранения документа.
// Установите свойство "UpdateLastSavedTimeProperty" в значение "true" для
// устанавливаем встроенное свойство «Время последнего сохранения» выходного документа на текущую дату/время.
// Установите свойство "UpdateLastSavedTimeProperty" в значение "false" для
// сохранить исходное значение встроенного свойства «Время последнего сохранения» входного документа.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
saveOptions.UpdateLastSavedTimeProperty = updateLastSavedTimeProperty;

doc.Save(ArtifactsDir + "OoxmlSaveOptions.LastSavedTime.docx", saveOptions);

doc = new Document(ArtifactsDir + "OoxmlSaveOptions.LastSavedTime.docx");
DateTime lastSavedTimeNew = doc.BuiltInDocumentProperties.LastSavedTime;

if (updateLastSavedTimeProperty)
    Assert.IsTrue((DateTime.Now - lastSavedTimeNew).Days < 1);
else
    Assert.AreEqual(new DateTime(2021, 5, 11, 6, 32, 0), 
        lastSavedTimeNew);
```

### Смотрите также

* class [SaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
