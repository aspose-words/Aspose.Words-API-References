---
title: DocumentPropertyCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words для .NET
description: DocumentPropertyCollection Item свойство. ВозвращаетDocumentProperty объект по имени свойства на С#.
type: docs
weight: 20
url: /ru/net/aspose.words.properties/documentpropertycollection/item/
---
## DocumentPropertyCollection indexer (1 of 2)

Возвращает[`DocumentProperty`](../../documentproperty/) объект по имени свойства.

```csharp
public virtual DocumentProperty this[string name] { get; }
```

| Параметр | Описание |
| --- | --- |
| name | Имя извлекаемого свойства без учета регистра. |

## Примечания

Возврат`нулевой` если свойство с указанным именем не найдено.

## Примеры

Показывает, как создать настраиваемое свойство документа, содержащее дату и время.

```csharp
Document doc = new Document();

doc.CustomDocumentProperties.Add("AuthorizationDate", DateTime.Now);

Console.WriteLine($"Document authorized on {doc.CustomDocumentProperties["AuthorizationDate"].ToDateTime()}");
```

### Смотрите также

* class [DocumentProperty](../../documentproperty/)
* class [DocumentPropertyCollection](../)
* пространство имен [Aspose.Words.Properties](../../../aspose.words.properties/)
* сборка [Aspose.Words](../../../)

---

## DocumentPropertyCollection indexer (2 of 2)

Возвращает[`DocumentProperty`](../../documentproperty/) объект по индексу.

```csharp
public DocumentProperty this[int index] { get; }
```

| Параметр | Описание |
| --- | --- |
| index | Нулевой индекс[`DocumentProperty`](../../documentproperty/) чтобы получить. |

## Примеры

Показывает, как работать с настраиваемыми свойствами документа.

```csharp
Document doc = new Document(MyDir + "Properties.docx");

// Каждый документ содержит коллекцию пользовательских свойств, которые, как и встроенные свойства, представляют собой пары ключ-значение.
 // Документ имеет фиксированный список встроенных свойств. Пользователь создает все настраиваемые свойства.
Assert.AreEqual("Value of custom document property", doc.CustomDocumentProperties["CustomProperty"].ToString());

doc.CustomDocumentProperties.Add("CustomProperty2", "Value of custom document property #2");

Console.WriteLine("Custom Properties:");
foreach (var customDocumentProperty in doc.CustomDocumentProperties)
{
    Console.WriteLine(customDocumentProperty.Name);
    Console.WriteLine($"\tType:\t{customDocumentProperty.Type}");
    Console.WriteLine($"\tValue:\t\"{customDocumentProperty.Value}\"");
}
```

### Смотрите также

* class [DocumentProperty](../../documentproperty/)
* class [DocumentPropertyCollection](../)
* пространство имен [Aspose.Words.Properties](../../../aspose.words.properties/)
* сборка [Aspose.Words](../../../)
