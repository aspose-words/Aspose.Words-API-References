---
title: SaveOptions.UpdateLastPrintedProperty
linktitle: UpdateLastPrintedProperty
articleTitle: UpdateLastPrintedProperty
second_title: Aspose.Words для .NET
description: SaveOptions UpdateLastPrintedProperty свойство. Получает или задает значение определяющее будет лиLastPrinted свойство обновляется перед сохранением на С#.
type: docs
weight: 170
url: /ru/net/aspose.words.saving/saveoptions/updatelastprintedproperty/
---
## SaveOptions.UpdateLastPrintedProperty property

Получает или задает значение, определяющее, будет ли[`LastPrinted`](../../../aspose.words.properties/builtindocumentproperties/lastprinted/) свойство обновляется перед сохранением.

```csharp
public bool UpdateLastPrintedProperty { get; set; }
```

## Примеры

Показывает, как обновить свойство CreatedTime документа при сохранении.

```csharp
Document doc = new Document();
doc.BuiltInDocumentProperties.CreatedTime = new DateTime(2019, 12, 20);

// Этот флаг определяет, обновляется ли созданное время, которое является встроенным свойством.
// Если да, то дата последней операции сохранения документа
// с этим объектом SaveOptions, переданным в качестве параметра, используется как созданное время.
DocSaveOptions saveOptions = new DocSaveOptions();
saveOptions.UpdateCreatedTimeProperty = isUpdateCreatedTimeProperty;

doc.Save(ArtifactsDir + "DocSaveOptions.UpdateCreatedTimeProperty.docx", saveOptions);

// Открываем сохраненный документ, затем проверяем значение свойства.
doc = new Document(ArtifactsDir + "DocSaveOptions.UpdateCreatedTimeProperty.docx");

Assert.AreNotEqual(isUpdateCreatedTimeProperty, new DateTime(2019, 12, 20) == doc.BuiltInDocumentProperties.CreatedTime);
```

Показывает, как обновить свойство «Последняя печать» документа при сохранении.

```csharp
Document doc = new Document();
doc.BuiltInDocumentProperties.LastPrinted = new DateTime(2019, 12, 20);

// Этот флаг определяет, обновляется ли последняя напечатанная дата, которая является встроенным свойством.
// Если да, то дата последней операции сохранения документа
// с этим объектом SaveOptions, переданным в качестве параметра, используется в качестве даты печати.
DocSaveOptions saveOptions = new DocSaveOptions();
saveOptions.UpdateLastPrintedProperty = isUpdateLastPrintedProperty;

// В Microsoft Word 2003 это свойство можно найти через File -> gt; Свойства -> Статистика -> Распечатано.
// Его также можно отобразить в теле документа, используя поле PRINTDATE.
doc.Save(ArtifactsDir + "DocSaveOptions.UpdateLastPrintedProperty.doc", saveOptions);

// Открываем сохраненный документ, затем проверяем значение свойства.
doc = new Document(ArtifactsDir + "DocSaveOptions.UpdateLastPrintedProperty.doc");

Assert.AreNotEqual(isUpdateLastPrintedProperty, new DateTime(2019, 12, 20) == doc.BuiltInDocumentProperties.LastPrinted);
```

### Смотрите также

* class [SaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
