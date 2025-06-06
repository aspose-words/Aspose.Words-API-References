---
title: PropertyType Enum
linktitle: PropertyType
articleTitle: PropertyType
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.PropertyType, чтобы легко определять типы данных свойств документа для улучшенного управления документами и их настройки.
type: docs
weight: 5230
url: /ru/net/aspose.words.properties/propertytype/
---
## PropertyType enumeration

Указывает тип данных свойства документа.

```csharp
public enum PropertyType
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Boolean | `0` | Свойство представляет собой логическое значение. |
| DateTime | `1` | Свойство представляет собой значение даты и времени. |
| Double | `2` | Свойство представляет собой плавающее число. |
| Number | `3` | Свойство представляет собой целое число. |
| String | `4` | Свойство представляет собой строковое значение. |
| StringArray | `5` | Свойство представляет собой массив строк. |
| ObjectArray | `6` | Свойство представляет собой массив объектов. |
| ByteArray | `7` | Свойство представляет собой массив байтов. |
| Other | `8` | Свойство имеет другой тип. |

## Примеры

Показывает, как работать с пользовательскими свойствами документа.

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

Assert.AreEqual(0, properties.Count);

// Пользовательские свойства документа — это пары ключ-значение, которые мы можем добавить в документ.
properties.Add("Authorized", true);
properties.Add("Authorized By", "John Doe");
properties.Add("Authorized Date", DateTime.Today);
properties.Add("Authorized Revision", doc.BuiltInDocumentProperties.RevisionNumber);
properties.Add("Authorized Amount", 123.45);

// Коллекция сортирует пользовательские свойства в алфавитном порядке.
Assert.AreEqual(1, properties.IndexOf("Authorized Amount"));
Assert.AreEqual(5, properties.Count);

// Распечатать все пользовательские свойства в документе.
using (IEnumerator<DocumentProperty> enumerator = properties.GetEnumerator())
{
    while (enumerator.MoveNext())
        Console.WriteLine($"Name: \"{enumerator.Current.Name}\"\n\tType: \"{enumerator.Current.Type}\"\n\tValue: \"{enumerator.Current.Value}\"");
}

// Отображение значения пользовательского свойства с использованием поля DOCPROPERTY.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocProperty field = (FieldDocProperty)builder.InsertField(" DOCPROPERTY \"Authorized By\"");
field.Update();

Assert.AreEqual("John Doe", field.Result);

// Эти пользовательские свойства можно найти в Microsoft Word через «Файл» -> «Свойства» -> «Дополнительные свойства» -> «Пользовательские».
doc.Save(ArtifactsDir + "DocumentProperties.DocumentPropertyCollection.docx");

// Ниже приведены три способа удаления пользовательских свойств из документа.
// 1 - Удалить по индексу:
properties.RemoveAt(1);

Assert.False(properties.Contains("Authorized Amount"));
Assert.AreEqual(4, properties.Count);

// 2 - Удалить по имени:
properties.Remove("Authorized Revision");

Assert.False(properties.Contains("Authorized Revision"));
Assert.AreEqual(3, properties.Count);

// 3 - Очистить всю коллекцию сразу:
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### Смотрите также

* class [DocumentProperty](../documentproperty/)
* property [Type](../documentproperty/type/)
* пространство имен [Aspose.Words.Properties](../../aspose.words.properties/)
* сборка [Aspose.Words](../../)
