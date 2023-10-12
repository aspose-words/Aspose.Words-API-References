---
title: CompareOptions.IgnoreDmlUniqueId
second_title: Справочник по API Aspose.Words для .NET
description: CompareOptions свойство. Указывает следует ли игнорировать разницу в уникальном идентификаторе DrawingML. Значение по умолчаниюЛОЖЬ .
type: docs
weight: 60
url: /ru/net/aspose.words.comparing/compareoptions/ignoredmluniqueid/
---
## CompareOptions.IgnoreDmlUniqueId property

Указывает, следует ли игнорировать разницу в уникальном идентификаторе DrawingML. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool IgnoreDmlUniqueId { get; set; }
```

### Примеры

Показывает, как сравнивать документы, игнорируя уникальный идентификатор DML.

```csharp
Document docA = new Document(MyDir + "DML unique ID original.docx");
Document docB = new Document(MyDir + "DML unique ID compare.docx");

// По умолчанию Aspose.Words не игнорирует уникальный идентификатор DML, а количество ревизий равно 2.
// Если мы игнорируем уникальный идентификатор DML и количество ревизий равно 0.
Aspose.Words.Comparing.CompareOptions compareOptions = new Aspose.Words.Comparing.CompareOptions();
compareOptions.IgnoreDmlUniqueId = isIgnoreDmlUniqueId;

docA.Compare(docB, "Aspose.Words", DateTime.Now, compareOptions);

Assert.AreEqual(isIgnoreDmlUniqueId ? 0 : 2, docA.Revisions.Count);
```

### Смотрите также

* class [CompareOptions](../)
* пространство имен [Aspose.Words.Comparing](../../compareoptions/)
* сборка [Aspose.Words](../../../)


