---
title: DocumentPropertyCollection.Item
second_title: Справочник по API Aspose.Words для .NET
description: DocumentPropertyCollection свойство. ВозвращаетDocumentProperty объект по имени свойства.
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
| name | Нечувствительное к регистру имя извлекаемого свойства. |

### Примечания

Возвращает null, если свойство с указанным именем не найдено.

### Примеры

Показывает, как создать пользовательское свойство документа, содержащее дату и время.

```csharp
Document doc = new Document();

doc.CustomDocumentProperties.Add("AuthorizationDate", DateTime.Now);

Console.WriteLine($"Document authorized on {doc.CustomDocumentProperties["AuthorizationDate"].ToDateTime()}");
```

### Смотрите также

* class [DocumentProperty](../../documentproperty/)
* class [DocumentPropertyCollection](../)
* пространство имен [Aspose.Words.Properties](../../documentpropertycollection/)
* сборка [Aspose.Words](../../../)

---

## DocumentPropertyCollection indexer (2 of 2)

Возвращает[`DocumentProperty`](../../documentproperty/) объект по индексу.

```csharp
public DocumentProperty this[int index] { get; }
```

| Параметр | Описание |
| --- | --- |
| index | Отсчитываемый от нуля индекс[`DocumentProperty`](../../documentproperty/) получить. |

### Примеры

Показывает, как работать с пользовательскими свойствами документа.

```csharp
Document doc = new Document(MyDir + "Properties.docx");

// Каждый документ содержит набор настраиваемых свойств, которые, как и встроенные свойства, представляют собой пары ключ-значение.
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
* пространство имен [Aspose.Words.Properties](../../documentpropertycollection/)
* сборка [Aspose.Words](../../../)


