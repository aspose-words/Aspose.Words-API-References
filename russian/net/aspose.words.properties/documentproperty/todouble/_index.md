---
title: DocumentProperty.ToDouble
linktitle: ToDouble
articleTitle: ToDouble
second_title: Aspose.Words для .NET
description: Конвертируйте значения DocumentProperty в double без усилий с помощью метода ToDouble. Разблокируйте точную обработку данных для своих приложений сегодня!
type: docs
weight: 90
url: /ru/net/aspose.words.properties/documentproperty/todouble/
---
## DocumentProperty.ToDouble method

Возвращает значение свойства как double.

```csharp
public double ToDouble()
```

## Примечания

Выдает исключение, если тип свойства не являетсяNumber .

## Примеры

Демонстрирует различные методы преобразования типов пользовательских свойств документа.

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
* пространство имен [Aspose.Words.Properties](../../../aspose.words.properties/)
* сборка [Aspose.Words](../../../)
