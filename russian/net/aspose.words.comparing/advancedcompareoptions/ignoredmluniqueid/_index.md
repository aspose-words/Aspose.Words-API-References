---
title: AdvancedCompareOptions.IgnoreDmlUniqueId
linktitle: IgnoreDmlUniqueId
articleTitle: IgnoreDmlUniqueId
second_title: Aspose.Words для .NET
description: Откройте для себя свойство AdvancedCompareOptions IgnoreDmlUniqueId, чтобы улучшить обработку DrawingML за счет эффективного управления уникальными идентификаторами. Оптимизируйте свой рабочий процесс!
type: docs
weight: 20
url: /ru/net/aspose.words.comparing/advancedcompareoptions/ignoredmluniqueid/
---
## AdvancedCompareOptions.IgnoreDmlUniqueId property

Указывает, следует ли игнорировать разницу в уникальном идентификаторе DrawingML.

```csharp
public bool IgnoreDmlUniqueId { get; set; }
```

## Примечания

Значение по умолчанию:`ЛОЖЬ` .

## Примеры

Показывает, как сравнивать документы, игнорируя уникальный идентификатор DML.

```csharp
Document docA = new Document(MyDir + "DML unique ID original.docx");
Document docB = new Document(MyDir + "DML unique ID compare.docx");

// По умолчанию Aspose.Words не игнорирует уникальный идентификатор DML, а количество ревизий равно 2.
// Если мы игнорируем уникальный идентификатор DML, а количество ревизий равно 0.
CompareOptions compareOptions = new CompareOptions();
compareOptions.AdvancedOptions.IgnoreDmlUniqueId = isIgnoreDmlUniqueId;

docA.Compare(docB, "Aspose.Words", DateTime.Now, compareOptions);

Assert.AreEqual(isIgnoreDmlUniqueId ? 0 : 2, docA.Revisions.Count);
```

### Смотрите также

* class [AdvancedCompareOptions](../)
* пространство имен [Aspose.Words.Comparing](../../../aspose.words.comparing/)
* сборка [Aspose.Words](../../../)
