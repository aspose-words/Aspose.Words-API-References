---
title: DocumentProperty.ToInt
second_title: Справочник по API Aspose.Words для .NET
description: DocumentProperty метод. Возвращает значение свойства в виде целого числа.
type: docs
weight: 100
url: /ru/net/aspose.words.properties/documentproperty/toint/
---
## DocumentProperty.ToInt method

Возвращает значение свойства в виде целого числа.

```csharp
public int ToInt()
```

### Примечания

Выдает исключение, если тип свойства неNumber .

### Примеры

Показывает различные методы преобразования типов пользовательских свойств документа.

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

DateTime authDate = DateTime.Today;
properties.Add("Authorized", true);
properties.Add("Authorized By", "John Doe");
properties.Add("Authorized Date", authDate);
properties.Add("Authorized Revision", doc.BuiltInDocumentProperties.RevisionNumber);
properties.Add("Authorized Amount", 123.45);

Assert.AreEqual(true, properties["Authorized"].ToBool());
Assert.AreEqual("John Doe", properties["Authorized By"].ToString());
Assert.AreEqual(authDate, properties["Authorized Date"].ToDateTime());
Assert.AreEqual(1, properties["Authorized Revision"].ToInt());
Assert.AreEqual(123.45d, properties["Authorized Amount"].ToDouble());
```

### Смотрите также

* class [DocumentProperty](../)
* пространство имен [Aspose.Words.Properties](../../documentproperty/)
* сборка [Aspose.Words](../../../)


