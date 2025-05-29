---
title: SaveOptions.UpdateLastPrintedProperty
linktitle: UpdateLastPrintedProperty
articleTitle: UpdateLastPrintedProperty
second_title: Aspose.Words для .NET
description: Оптимизируйте управление документами с помощью SaveOptions UpdateLastPrintedProperty. Управляйте обновлениями LastPrinted для эффективного сохранения и улучшения рабочего процесса.
type: docs
weight: 180
url: /ru/net/aspose.words.saving/saveoptions/updatelastprintedproperty/
---
## SaveOptions.UpdateLastPrintedProperty property

Возвращает или задает значение, определяющее, является ли[`LastPrinted`](../../../aspose.words.properties/builtindocumentproperties/lastprinted/) свойство обновляется перед сохранением.

```csharp
public bool UpdateLastPrintedProperty { get; set; }
```

## Примеры

Показывает, как обновить свойство документа «Последняя печать» при сохранении.

```csharp
Document doc = new Document();

DateTime lastPrinted = new DateTime(2019, 12, 20);
doc.BuiltInDocumentProperties.LastPrinted = lastPrinted;

// Этот флаг определяет, обновляется ли последняя напечатанная дата, которая является встроенным свойством.
// Если да, то дата последней операции сохранения документа
// с этим объектом SaveOptions, переданным в качестве параметра, используется как дата печати.
DocSaveOptions saveOptions = new DocSaveOptions();
saveOptions.UpdateLastPrintedProperty = isUpdateLastPrintedProperty;

// В Microsoft Word 2003 это свойство можно найти через Файл -> Свойства -> Статистика -> Напечатано.
// Его также можно отобразить в теле документа с помощью поля PRINTDATE.
doc.Save(ArtifactsDir + "DocSaveOptions.UpdateLastPrintedProperty.doc", saveOptions);

// Откройте сохраненный документ, затем проверьте значение свойства.
doc = new Document(ArtifactsDir + "DocSaveOptions.UpdateLastPrintedProperty.doc");

if (isUpdateLastPrintedProperty)
    Assert.AreNotEqual(lastPrinted, doc.BuiltInDocumentProperties.LastPrinted);
else
    Assert.AreEqual(lastPrinted, doc.BuiltInDocumentProperties.LastPrinted);
```

### Смотрите также

* class [SaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
