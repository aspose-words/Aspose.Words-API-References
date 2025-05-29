---
title: Document.Variables
linktitle: Variables
articleTitle: Variables
second_title: Aspose.Words для .NET
description: Откройте для себя переменные документа. Получите доступ к мощной коллекции настраиваемых переменных для ваших документов и шаблонов, повышающих эффективность и гибкость.
type: docs
weight: 460
url: /ru/net/aspose.words/document/variables/
---
## Document.Variables property

Возвращает коллекцию переменных, добавленных в документ или шаблон.

```csharp
public VariableCollection Variables { get; }
```

## Примеры

Показывает, как работать с коллекцией переменных документа.

```csharp
Document doc = new Document();
VariableCollection variables = doc.Variables;

// Каждый документ имеет набор переменных пар ключ/значение, в которые мы можем добавлять элементы.
variables.Add("Home address", "123 Main St.");
variables.Add("City", "London");
variables.Add("Bedrooms", "3");

Assert.AreEqual(3, variables.Count);

// Мы можем отобразить значения переменных в теле документа, используя поля DOCVARIABLE.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocVariable field = (FieldDocVariable)builder.InsertField(FieldType.FieldDocVariable, true);
field.VariableName = "Home address";
field.Update();

Assert.AreEqual("123 Main St.", field.Result);

// Присвоение значений существующим ключам приведет к их обновлению.
variables.Add("Home address", "456 Queen St.");

// Затем нам придется обновить поля DOCVARIABLE, чтобы убедиться, что они отображают актуальное значение.
Assert.AreEqual("123 Main St.", field.Result);

field.Update();

Assert.AreEqual("456 Queen St.", field.Result);

// Проверяем, существуют ли переменные документа с определенным именем или значением.
Assert.True(variables.Contains("City"));
Assert.True(variables.Any(v => v.Value == "London"));

// Коллекция переменных автоматически сортирует переменные в алфавитном порядке по имени.
Assert.AreEqual(0, variables.IndexOfKey("Bedrooms"));
Assert.AreEqual(1, variables.IndexOfKey("City"));
Assert.AreEqual(2, variables.IndexOfKey("Home address"));

Assert.AreEqual("3", variables[0]);
Assert.AreEqual("London", variables["City"]);

// Перечислить коллекцию переменных.
using (IEnumerator<KeyValuePair<string, string>> enumerator = doc.Variables.GetEnumerator())
    while (enumerator.MoveNext())
        Console.WriteLine($"Name: {enumerator.Current.Key}, Value: {enumerator.Current.Value}");

// Ниже приведены три способа удаления переменных документа из коллекции.
// 1 - По имени:
variables.Remove("City");

Assert.False(variables.Contains("City"));

// 2 - По индексу:
variables.RemoveAt(1);

Assert.False(variables.Contains("Home address"));

// 3 - Очистить всю коллекцию сразу:
variables.Clear();

Assert.AreEqual(0, variables.Count);
```

### Смотрите также

* class [VariableCollection](../../variablecollection/)
* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
