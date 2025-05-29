---
title: SaveOptions.UpdateCreatedTimeProperty
linktitle: UpdateCreatedTimeProperty
articleTitle: UpdateCreatedTimeProperty
second_title: Aspose.Words для .NET
description: Оптимизируйте SaveOptions с помощью UpdateCreatedTimeProperty. Контролируйте обновления CreatedTime перед сохранением, повышая точность данных. По умолчанию — false.
type: docs
weight: 160
url: /ru/net/aspose.words.saving/saveoptions/updatecreatedtimeproperty/
---
## SaveOptions.UpdateCreatedTimeProperty property

Возвращает или задает значение, определяющее, является ли[`CreatedTime`](../../../aspose.words.properties/builtindocumentproperties/createdtime/) свойство обновляется перед сохранением. Значение по умолчанию:`ЛОЖЬ` ;

```csharp
public bool UpdateCreatedTimeProperty { get; set; }
```

## Примеры

Показывает, как обновить свойство «CreatedTime» документа при сохранении.

```csharp
Document doc = new Document();

DateTime createdTime = new DateTime(2019, 12, 20);
doc.BuiltInDocumentProperties.CreatedTime = createdTime;

// Этот флаг определяет, обновляется ли созданное время, которое является встроенным свойством.
// Если да, то дата последней операции сохранения документа
// с этим объектом SaveOptions, переданным в качестве параметра, используется как созданное время.
DocSaveOptions saveOptions = new DocSaveOptions();
saveOptions.UpdateCreatedTimeProperty = isUpdateCreatedTimeProperty;

doc.Save(ArtifactsDir + "DocSaveOptions.UpdateCreatedTimeProperty.docx", saveOptions);

// Откройте сохраненный документ, затем проверьте значение свойства.
doc = new Document(ArtifactsDir + "DocSaveOptions.UpdateCreatedTimeProperty.docx");

if (isUpdateCreatedTimeProperty)
    Assert.AreNotEqual(createdTime, doc.BuiltInDocumentProperties.CreatedTime);
else
    Assert.AreEqual(createdTime, doc.BuiltInDocumentProperties.CreatedTime);
```

### Смотрите также

* class [SaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
