---
title: DocumentPropertyCollection.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: Aspose.Words для .NET
description: Откройте для себя метод DocumentPropertyCollection GetEnumerator. Легко перебирайте все элементы коллекции с помощью этого эффективного перечислителя для бесперебойного доступа к данным.
type: docs
weight: 50
url: /ru/net/aspose.words.properties/documentpropertycollection/getenumerator/
---
## DocumentPropertyCollection.GetEnumerator method

Возвращает объект перечислителя, который можно использовать для перебора всех элементов в коллекции.

```csharp
public IEnumerator<DocumentProperty> GetEnumerator()
```

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

* class [DocumentProperty](../../documentproperty/)
* class [DocumentPropertyCollection](../)
* пространство имен [Aspose.Words.Properties](../../../aspose.words.properties/)
* сборка [Aspose.Words](../../../)
