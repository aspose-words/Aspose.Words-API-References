---
title: DocumentProperty.ToDateTime
linktitle: ToDateTime
articleTitle: ToDateTime
second_title: Aspose.Words для .NET
description: Конвертируйте DocumentProperty в UTC DateTime без усилий. Получите доступ к точным временным меткам и улучшите управление данными с помощью нашего надежного метода.
type: docs
weight: 80
url: /ru/net/aspose.words.properties/documentproperty/todatetime/
---
## DocumentProperty.ToDateTime method

Возвращает значение свойства как**ДатаВремя** в UTC.

```csharp
public DateTime ToDateTime()
```

## Примечания

Выдает исключение, если тип свойства не являетсяDateTime.

Microsoft Word сохраняет только часть даты (без времени) для пользовательских свойств даты.

## Примеры

Показывает, как создать пользовательское свойство документа, содержащее дату и время.

```csharp
Document doc = new Document();

doc.CustomDocumentProperties.Add("AuthorizationDate", DateTime.Now);
DateTime authorizationDate = doc.CustomDocumentProperties["AuthorizationDate"].ToDateTime();
Console.WriteLine($"Document authorized on {authorizationDate}");
```

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
