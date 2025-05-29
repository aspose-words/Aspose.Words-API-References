---
title: DocumentProperty.ToString
linktitle: ToString
articleTitle: ToString
second_title: Aspose.Words для .NET
description: Откройте для себя метод DocumentProperty ToString, который форматирует значения свойств в виде строк на основе локали, улучшая представление данных и взаимодействие с пользователем.
type: docs
weight: 110
url: /ru/net/aspose.words.properties/documentproperty/tostring/
---
## DocumentProperty.ToString method

Возвращает значение свойства в виде строки, отформатированной в соответствии с текущей локалью.

```csharp
public override string ToString()
```

## Примечания

Преобразует логическое свойство в «Y» или «N». Преобразует свойство даты в короткую строку даты. Для всех остальных типов преобразует свойство с помощью Object.ToString().

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

* class [DocumentProperty](../)
* пространство имен [Aspose.Words.Properties](../../../aspose.words.properties/)
* сборка [Aspose.Words](../../../)
