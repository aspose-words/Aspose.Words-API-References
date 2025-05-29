---
title: AdvancedCompareOptions Class
linktitle: AdvancedCompareOptions
articleTitle: AdvancedCompareOptions
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.AdvancedCompareOptions для эффективного сравнения документов. Настройте параметры для точных результатов и повышения производительности.
type: docs
weight: 460
url: /ru/net/aspose.words.comparing/advancedcompareoptions/
---
## AdvancedCompareOptions class

Позволяет задать расширенные параметры сравнения.

```csharp
public class AdvancedCompareOptions
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [AdvancedCompareOptions](advancedcompareoptions/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [IgnoreDmlUniqueId](../../aspose.words.comparing/advancedcompareoptions/ignoredmluniqueid/) { get; set; } | Указывает, следует ли игнорировать разницу в уникальном идентификаторе DrawingML. |
| [IgnoreStoreItemId](../../aspose.words.comparing/advancedcompareoptions/ignorestoreitemid/) { get; set; } | Указывает, следует ли игнорировать разницу в элементе хранилища StructuredDocumentTag Id. |

## Примечания

Эти параметры не имеют эквивалента в Microsoft Word и могут помочь получить более точный результат сравнения.

## Примеры

Показывает, как сравнивать SDT с одинаковым содержимым, но разными идентификаторами товаров в магазине.

```csharp
Document docA = new Document(MyDir + "Document with SDT 1.docx");
Document docB = new Document(MyDir + "Document with SDT 2.docx");

// Настройте параметры для сравнения SDT с одинаковым содержимым, но разными идентификаторами элементов магазина.
CompareOptions compareOptions = new CompareOptions();
compareOptions.AdvancedOptions.IgnoreStoreItemId = false;

docA.Compare(docB, "user", DateTime.Now, compareOptions);
Assert.AreEqual(8, docA.Revisions.Count);

compareOptions.AdvancedOptions.IgnoreStoreItemId = true;

docA.Revisions.RejectAll();
docA.Compare(docB, "user", DateTime.Now, compareOptions);
Assert.AreEqual(0, docA.Revisions.Count);
```

### Смотрите также

* пространство имен [Aspose.Words.Comparing](../../aspose.words.comparing/)
* сборка [Aspose.Words](../../)
