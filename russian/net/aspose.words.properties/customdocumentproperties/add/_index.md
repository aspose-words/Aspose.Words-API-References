---
title: CustomDocumentProperties.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words для .NET
description: Создавайте уникальные пользовательские свойства документа без усилий с помощью метода Add. Улучшайте свои документы с помощью специализированных типов данных String для оптимальной производительности.
type: docs
weight: 10
url: /ru/net/aspose.words.properties/customdocumentproperties/add/
---
## Add(*string, string*) {#add_4}

Создает новое пользовательское свойство документаString тип данных.

```csharp
public DocumentProperty Add(string name, string value)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| name | String | Название объекта недвижимости. |
| value | String | Стоимость имущества. |

### Возвращаемое значение

Вновь созданный объект свойства.

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
* class [CustomDocumentProperties](../)
* пространство имен [Aspose.Words.Properties](../../../aspose.words.properties/)
* сборка [Aspose.Words](../../../)

---

## Add(*string, int*) {#add_2}

Создает новое пользовательское свойство документаNumber тип данных.

```csharp
public DocumentProperty Add(string name, int value)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| name | String | Название объекта недвижимости. |
| value | Int32 | Стоимость имущества. |

### Возвращаемое значение

Вновь созданный объект свойства.

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
* class [CustomDocumentProperties](../)
* пространство имен [Aspose.Words.Properties](../../../aspose.words.properties/)
* сборка [Aspose.Words](../../../)

---

## Add(*string, DateTime*) {#add_3}

Создает новое пользовательское свойство документаDateTime тип данных.

```csharp
public DocumentProperty Add(string name, DateTime value)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| name | String | Название объекта недвижимости. |
| value | DateTime | Стоимость имущества. |

### Возвращаемое значение

Вновь созданный объект свойства.

## Примеры

Показывает, как создать пользовательское свойство документа, содержащее дату и время.

```csharp
Document doc = new Document();

doc.CustomDocumentProperties.Add("AuthorizationDate", DateTime.Now);
DateTime authorizationDate = doc.CustomDocumentProperties["AuthorizationDate"].ToDateTime();
Console.WriteLine($"Document authorized on {authorizationDate}");
```

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
* class [CustomDocumentProperties](../)
* пространство имен [Aspose.Words.Properties](../../../aspose.words.properties/)
* сборка [Aspose.Words](../../../)

---

## Add(*string, bool*) {#add}

Создает новое пользовательское свойство документаBoolean тип данных.

```csharp
public DocumentProperty Add(string name, bool value)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| name | String | Название объекта недвижимости. |
| value | Boolean | Стоимость имущества. |

### Возвращаемое значение

Вновь созданный объект свойства.

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
* class [CustomDocumentProperties](../)
* пространство имен [Aspose.Words.Properties](../../../aspose.words.properties/)
* сборка [Aspose.Words](../../../)

---

## Add(*string, double*) {#add_1}

Создает новое пользовательское свойство документаDouble тип данных.

```csharp
public DocumentProperty Add(string name, double value)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| name | String | Название объекта недвижимости. |
| value | Double | Стоимость имущества. |

### Возвращаемое значение

Вновь созданный объект свойства.

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
* class [CustomDocumentProperties](../)
* пространство имен [Aspose.Words.Properties](../../../aspose.words.properties/)
* сборка [Aspose.Words](../../../)
