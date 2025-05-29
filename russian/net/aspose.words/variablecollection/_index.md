---
title: VariableCollection Class
linktitle: VariableCollection
articleTitle: VariableCollection
second_title: Aspose.Words для .NET
description: Откройте для себя Aspose.Words.VariableCollection, эффективно управляйте и настраивайте переменные документа для повышения автоматизации и гибкости работы с документами.
type: docs
weight: 7380
url: /ru/net/aspose.words/variablecollection/
---
## VariableCollection class

Коллекция переменных документа.

Чтобы узнать больше, посетите[Работа со свойствами документа](https://docs.aspose.com/words/net/work-with-document-properties/) документальная статья.

```csharp
public class VariableCollection : IEnumerable<KeyValuePair<string, string>>
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Count](../../aspose.words/variablecollection/count/) { get; } | Получает количество элементов, содержащихся в коллекции. |
| [Item](../../aspose.words/variablecollection/item/) { get; set; } | Возвращает или задает переменную документа по имени без учета регистра. `нулевой`Значения не допускаются в правой части присваивания и будут заменены пустой строкой. (2 indexers) |

## Методы

| Имя | Описание |
| --- | --- |
| [Add](../../aspose.words/variablecollection/add/)(*string, string*) | Добавляет переменную документа в коллекцию. |
| [Clear](../../aspose.words/variablecollection/clear/)() | Удаляет все элементы из коллекции. |
| [Contains](../../aspose.words/variablecollection/contains/)(*string*) | Определяет, содержит ли коллекция переменную документа с указанным именем. |
| [GetEnumerator](../../aspose.words/variablecollection/getenumerator/)() | Возвращает объект перечислителя, который можно использовать для перебора всех переменных в коллекции. |
| [IndexOfKey](../../aspose.words/variablecollection/indexofkey/)(*string*) | Возвращает отсчитываемый от нуля индекс указанной переменной документа в коллекции. |
| [Remove](../../aspose.words/variablecollection/remove/)(*string*) | Удаляет переменную документа с указанным именем из коллекции. |
| [RemoveAt](../../aspose.words/variablecollection/removeat/)(*int*) | Удаляет переменную документа по указанному индексу. |

## Примечания

Имена и значения переменных являются строками.

Имена переменных нечувствительны к регистру.

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

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
