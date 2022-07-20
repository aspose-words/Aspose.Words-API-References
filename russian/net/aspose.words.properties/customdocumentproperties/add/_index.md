---
title: Add
second_title: Справочник по API Aspose.Words для .NET
description: Создает новое пользовательское свойство документа Тип свойства.String тип данных.
type: docs
weight: 10
url: /ru/net/aspose.words.properties/customdocumentproperties/add/
---
## Add(string, string) {#add_4}

Создает новое пользовательское свойство документа **Тип свойства.String** тип данных.

```csharp
public DocumentProperty Add(string name, string value)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| name | String | Имя свойства. |
| value | String | Стоимость имущества. |

### Возвращаемое значение

Недавно созданный объект свойства.

### Примеры

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

// Распечатать каждое пользовательское свойство в документе.
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

// Мы можем найти эти пользовательские свойства в Microsoft Word через «Файл» -> "Свойства" > "Дополнительные свойства" > "Обычай".
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

* class [DocumentProperty](../../documentproperty)
* class [CustomDocumentProperties](../../customdocumentproperties)
* пространство имен [Aspose.Words.Properties](../../customdocumentproperties)
* сборка [Aspose.Words](../../../)

---

## Add(string, int) {#add_2}

Создает новое пользовательское свойство документа **PropertyType.Number** тип данных.

```csharp
public DocumentProperty Add(string name, int value)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| name | String | Имя свойства. |
| value | Int32 | Стоимость имущества. |

### Возвращаемое значение

Недавно созданный объект свойства.

### Примеры

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

// Распечатать каждое пользовательское свойство в документе.
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

// Мы можем найти эти пользовательские свойства в Microsoft Word через «Файл» -> "Свойства" > "Дополнительные свойства" > "Обычай".
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

* class [DocumentProperty](../../documentproperty)
* class [CustomDocumentProperties](../../customdocumentproperties)
* пространство имен [Aspose.Words.Properties](../../customdocumentproperties)
* сборка [Aspose.Words](../../../)

---

## Add(string, DateTime) {#add_3}

Создает новое пользовательское свойство документа **PropertyType.DateTime** тип данных.

```csharp
public DocumentProperty Add(string name, DateTime value)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| name | String | Имя свойства. |
| value | DateTime | Стоимость имущества. |

### Возвращаемое значение

Недавно созданный объект свойства.

### Примеры

Показывает, как создать пользовательское свойство документа, содержащее дату и время.

```csharp
Document doc = new Document();

doc.CustomDocumentProperties.Add("AuthorizationDate", DateTime.Now);

Console.WriteLine($"Document authorized on {doc.CustomDocumentProperties["AuthorizationDate"].ToDateTime()}");
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

// Распечатать каждое пользовательское свойство в документе.
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

// Мы можем найти эти пользовательские свойства в Microsoft Word через «Файл» -> "Свойства" > "Дополнительные свойства" > "Обычай".
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

* class [DocumentProperty](../../documentproperty)
* class [CustomDocumentProperties](../../customdocumentproperties)
* пространство имен [Aspose.Words.Properties](../../customdocumentproperties)
* сборка [Aspose.Words](../../../)

---

## Add(string, bool) {#add}

Создает новое пользовательское свойство документа **PropertyType.Boolean** тип данных.

```csharp
public DocumentProperty Add(string name, bool value)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| name | String | Имя свойства. |
| value | Boolean | Стоимость имущества. |

### Возвращаемое значение

Недавно созданный объект свойства.

### Примеры

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

// Распечатать каждое пользовательское свойство в документе.
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

// Мы можем найти эти пользовательские свойства в Microsoft Word через «Файл» -> "Свойства" > "Дополнительные свойства" > "Обычай".
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

* class [DocumentProperty](../../documentproperty)
* class [CustomDocumentProperties](../../customdocumentproperties)
* пространство имен [Aspose.Words.Properties](../../customdocumentproperties)
* сборка [Aspose.Words](../../../)

---

## Add(string, double) {#add_1}

Создает новое пользовательское свойство документа **PropertyType.Float** тип данных.

```csharp
public DocumentProperty Add(string name, double value)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| name | String | Имя свойства. |
| value | Double | Стоимость имущества. |

### Возвращаемое значение

Недавно созданный объект свойства.

### Примеры

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

// Распечатать каждое пользовательское свойство в документе.
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

// Мы можем найти эти пользовательские свойства в Microsoft Word через «Файл» -> "Свойства" > "Дополнительные свойства" > "Обычай".
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

* class [DocumentProperty](../../documentproperty)
* class [CustomDocumentProperties](../../customdocumentproperties)
* пространство имен [Aspose.Words.Properties](../../customdocumentproperties)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
