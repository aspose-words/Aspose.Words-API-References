---
title: BuiltInDocumentProperties.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words для .NET
description: Доступ к объектам DocumentProperty без усилий с помощью свойства BuiltInDocumentProperties Item. Оптимизируйте управление документами уже сегодня!
type: docs
weight: 140
url: /ru/net/aspose.words.properties/builtindocumentproperties/item/
---
## BuiltInDocumentProperties indexer

Возвращает[`DocumentProperty`](../../documentproperty/) объект по имени свойства.

```csharp
public override DocumentProperty this[string name] { get; }
```

| Параметр | Описание |
| --- | --- |
| name | Нечувствительное к регистру имя извлекаемого свойства. |

## Примечания

Строковые имена свойств соответствуют именам свойств typed , доступных из[`BuiltInDocumentProperties`](../).

Если вы запрашиваете свойство, которого нет в документе, но name свойства распознается как допустимое встроенное имя, будет создано новое[`DocumentProperty`](../../documentproperty/) создается, добавляется в коллекцию и возвращается. Вновь созданному свойству присваивается значение по умолчанию (пустая строка, ноль,`ЛОЖЬ` или DateTime.MinValue в зависимости от type встроенного свойства).

Если вы запрашиваете свойство, которого нет в документе, и name не распознается как встроенное имя,`нулевой` возвращается.

## Примеры

Показывает, как работать с пользовательскими свойствами документа.

```csharp
Document doc = new Document(MyDir + "Properties.docx");

// Каждый документ содержит набор пользовательских свойств, которые, как и встроенные свойства, представляют собой пары ключ-значение.
 // Документ имеет фиксированный список встроенных свойств. Пользователь создает все пользовательские свойства.
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
* class [BuiltInDocumentProperties](../)
* пространство имен [Aspose.Words.Properties](../../../aspose.words.properties/)
* сборка [Aspose.Words](../../../)
