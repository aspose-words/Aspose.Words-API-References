---
title: DocumentProperty.ToBool
linktitle: ToBool
articleTitle: ToBool
second_title: Aspose.Words для .NET
description: DocumentProperty ToBool метод. Возвращает значение свойства как bool на С#.
type: docs
weight: 60
url: /ru/net/aspose.words.properties/documentproperty/tobool/
---
## DocumentProperty.ToBool method

Возвращает значение свойства как bool.

```csharp
public bool ToBool()
```

## Примечания

Выдает исключение, если тип свойства неBoolean.

## Примеры

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
* пространство имен [Aspose.Words.Properties](../../../aspose.words.properties/)
* сборка [Aspose.Words](../../../)
