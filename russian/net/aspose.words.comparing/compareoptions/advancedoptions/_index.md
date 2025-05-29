---
title: CompareOptions.AdvancedOptions
linktitle: AdvancedOptions
articleTitle: AdvancedOptions
second_title: Aspose.Words для .NET
description: Откройте CompareOptions AdvancedOptions для улучшения сравнений. Достигайте точных результатов с помощью индивидуальных настроек для оптимального вывода.
type: docs
weight: 20
url: /ru/net/aspose.words.comparing/compareoptions/advancedoptions/
---
## CompareOptions.AdvancedOptions property

Указывает расширенные параметры сравнения, которые могут помочь получить более точные результаты сравнения.

```csharp
public AdvancedCompareOptions AdvancedOptions { get; }
```

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

* class [AdvancedCompareOptions](../../advancedcompareoptions/)
* class [CompareOptions](../)
* пространство имен [Aspose.Words.Comparing](../../../aspose.words.comparing/)
* сборка [Aspose.Words](../../../)
