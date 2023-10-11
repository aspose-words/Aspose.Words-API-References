---
title: Class VariableCollection
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.VariableCollection сорт. Коллекция переменных документа.
type: docs
weight: 6530
url: /ru/net/aspose.words/variablecollection/
---
## VariableCollection class

Коллекция переменных документа.

Чтобы узнать больше, посетите[Работа со свойствами документа](https://docs.aspose.com/words/net/work-with-document-properties/) статья документации.

```csharp
public class VariableCollection : IEnumerable<KeyValuePair<string, string>>
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Count](../../aspose.words/variablecollection/count/) { get; } | Получает количество элементов, содержащихся в коллекции. |
| [Item](../../aspose.words/variablecollection/item/) { get; set; } | Получает или задает переменную документа по имени без учета регистра. `нулевой` значения не допускаются в качестве правой части присваивания и будут заменены пустой строкой. (2 indexers) |

## Методы

| Имя | Описание |
| --- | --- |
| [Add](../../aspose.words/variablecollection/add/)(string, string) | Добавляет переменную документа в коллекцию. |
| [Clear](../../aspose.words/variablecollection/clear/)() | Удаляет все элементы из коллекции. |
| [Contains](../../aspose.words/variablecollection/contains/)(string) | Определяет, содержит ли коллекция переменную документа с заданным именем. |
| [GetEnumerator](../../aspose.words/variablecollection/getenumerator/)() | Возвращает объект перечислителя, который можно использовать для перебора всех переменных в коллекции. |
| [IndexOfKey](../../aspose.words/variablecollection/indexofkey/)(string) | Возвращает отсчитываемый от нуля индекс указанной переменной документа в коллекции. |
| [Remove](../../aspose.words/variablecollection/remove/)(string) | Удаляет переменную документа с указанным именем из коллекции. |
| [RemoveAt](../../aspose.words/variablecollection/removeat/)(int) | Удаляет переменную документа по указанному индексу. |

### Примечания

Имена и значения переменных являются строками.

Имена переменных не чувствительны к регистру.

### Примеры

Показывает, как работать с коллекцией переменных документа.

```csharp
Document doc = new Document();
VariableCollection variables = doc.Variables;

// В каждом документе есть набор переменных пары ключ/значение, в которые мы можем добавлять элементы.
variables.Add("Home address", "123 Main St.");
variables.Add("City", "London");
variables.Add("Bedrooms", "3");

Assert.AreEqual(3, variables.Count);

// Мы можем отображать значения переменных в теле документа, используя поля DOCVARIABLE.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocVariable field = (FieldDocVariable)builder.InsertField(FieldType.FieldDocVariable, true);
field.VariableName = "Home address";
field.Update();

Assert.AreEqual("123 Main St.", field.Result);

// Присвоение значений существующим ключам обновит их.
variables.Add("Home address", "456 Queen St.");

// Затем нам придется обновить поля DOCVARIABLE, чтобы они отображали актуальное значение.
Assert.AreEqual("123 Main St.", field.Result);

field.Update();

Assert.AreEqual("456 Queen St.", field.Result);

// Проверяем, что переменные документа с определенным именем или значением существуют.
Assert.True(variables.Contains("City"));
Assert.True(variables.Any(v => v.Value == "London"));

// Коллекция переменных автоматически сортирует переменные в алфавитном порядке по имени.
Assert.AreEqual(0, variables.IndexOfKey("Bedrooms"));
Assert.AreEqual(1, variables.IndexOfKey("City"));
Assert.AreEqual(2, variables.IndexOfKey("Home address"));

// Перебираем коллекцию переменных.
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

Assert.That(variables, Is.Empty);
```

### Смотрите также

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)


