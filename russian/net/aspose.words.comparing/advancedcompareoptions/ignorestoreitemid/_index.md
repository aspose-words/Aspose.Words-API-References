---
title: AdvancedCompareOptions.IgnoreStoreItemId
linktitle: IgnoreStoreItemId
articleTitle: IgnoreStoreItemId
second_title: Aspose.Words для .NET
description: Узнайте, как свойство AdvancedCompareOptions IgnoreStoreItemId улучшает сравнение документов, игнорируя различия в идентификаторах StructuredDocumentTag для повышения точности.
type: docs
weight: 30
url: /ru/net/aspose.words.comparing/advancedcompareoptions/ignorestoreitemid/
---
## AdvancedCompareOptions.IgnoreStoreItemId property

Указывает, следует ли игнорировать разницу в элементе хранилища StructuredDocumentTag Id.

```csharp
public bool IgnoreStoreItemId { get; set; }
```

## Примечания

Значение по умолчанию:`ЛОЖЬ` .

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

* class [AdvancedCompareOptions](../)
* пространство имен [Aspose.Words.Comparing](../../../aspose.words.comparing/)
* сборка [Aspose.Words](../../../)
