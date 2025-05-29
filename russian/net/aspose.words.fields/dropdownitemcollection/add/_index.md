---
title: DropDownItemCollection.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words для .NET
description: Легко улучшите DropDownItemCollection с помощью метода Add. Мгновенно добавляйте строки, чтобы расширить свою коллекцию и улучшить пользовательский опыт.
type: docs
weight: 30
url: /ru/net/aspose.words.fields/dropdownitemcollection/add/
---
## DropDownItemCollection.Add method

Добавляет строку в конец коллекции.

```csharp
public int Add(string value)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | String | Строка, добавляемая в конец коллекции. |

### Возвращаемое значение

Индекс (начиная с нуля), по которому вставляется новый элемент.

## Примеры

Показывает, как вставить поле со списком и редактировать элементы в его коллекции.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте поле со списком, а затем проверьте набор раскрывающихся элементов.
// В Microsoft Word пользователь щелкнет по полю со списком,
// а затем выберите один из элементов текста в коллекции для отображения.
string[] items = { "One", "Two", "Three" };
FormField comboBoxField = builder.InsertComboBox("DropDown", items, 0);
DropDownItemCollection dropDownItems = comboBoxField.DropDownItems;

Assert.AreEqual(3, dropDownItems.Count);
Assert.AreEqual("One", dropDownItems[0]);
Assert.AreEqual(1, dropDownItems.IndexOf("Two"));
Assert.IsTrue(dropDownItems.Contains("Three"));

// Существует два способа добавления нового элемента в существующую коллекцию элементов раскрывающегося списка.
// 1 — Добавить элемент в конец коллекции:
dropDownItems.Add("Four");

// 2 - Вставить элемент перед другим элементом по указанному индексу:
dropDownItems.Insert(3, "Three and a half");

Assert.AreEqual(5, dropDownItems.Count);

// Проходим по коллекции и выводим каждый элемент.
using (IEnumerator<string> dropDownCollectionEnumerator = dropDownItems.GetEnumerator())
    while (dropDownCollectionEnumerator.MoveNext())
        Console.WriteLine(dropDownCollectionEnumerator.Current);

// Существует два способа удаления элементов из коллекции раскрывающихся списков.
// 1 - Удалить элемент с содержимым, равным переданной строке:
dropDownItems.Remove("Four");

// 2 - Удалить элемент по индексу:
dropDownItems.RemoveAt(3);

Assert.AreEqual(3, dropDownItems.Count);
Assert.IsFalse(dropDownItems.Contains("Three and a half"));
Assert.IsFalse(dropDownItems.Contains("Four"));

doc.Save(ArtifactsDir + "FormFields.DropDownItemCollection.html");

// Очистить всю коллекцию раскрывающихся элементов.
dropDownItems.Clear();
```

### Смотрите также

* class [DropDownItemCollection](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
