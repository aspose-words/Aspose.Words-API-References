---
title: DropDownItemCollection.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words для .NET
description: DropDownItemCollection Add метод. Добавляет строку в конец коллекции на С#.
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

Индекс, отсчитываемый от нуля, по которому вставляется новый элемент.

## Примеры

Показывает, как вставить поле со списком и отредактировать элементы в его коллекции элементов.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставляем поле со списком, а затем проверяем набор раскрывающихся элементов.
// В Microsoft Word пользователь щелкнет поле со списком,
// а затем выберите один из элементов текста в коллекции для отображения.
string[] items = { "One", "Two", "Three" };
FormField comboBoxField = builder.InsertComboBox("DropDown", items, 0);
DropDownItemCollection dropDownItems = comboBoxField.DropDownItems;

Assert.AreEqual(3, dropDownItems.Count);
Assert.AreEqual("One", dropDownItems[0]);
Assert.AreEqual(1, dropDownItems.IndexOf("Two"));
Assert.IsTrue(dropDownItems.Contains("Three"));

// Существует два способа добавления нового элемента в существующую коллекцию элементов раскрывающегося списка.
// 1 — добавить элемент в конец коллекции:
dropDownItems.Add("Four");

// 2 - Вставить элемент перед другим элементом по указанному индексу:
dropDownItems.Insert(3, "Three and a half");

Assert.AreEqual(5, dropDownItems.Count);

// Перебираем коллекцию и печатаем каждый элемент.
using (IEnumerator<string> dropDownCollectionEnumerator = dropDownItems.GetEnumerator())
    while (dropDownCollectionEnumerator.MoveNext())
        Console.WriteLine(dropDownCollectionEnumerator.Current);

// Есть два способа удаления элементов из коллекции раскрывающихся элементов.
// 1 - Удалить элемент, содержимое которого равно переданной строке:
dropDownItems.Remove("Four");

// 2 - Удалить элемент по индексу:
dropDownItems.RemoveAt(3);

Assert.AreEqual(3, dropDownItems.Count);
Assert.IsFalse(dropDownItems.Contains("Three and a half"));
Assert.IsFalse(dropDownItems.Contains("Four"));

doc.Save(ArtifactsDir + "FormFields.DropDownItemCollection.html");

// Очищаем всю коллекцию раскрывающихся элементов.
dropDownItems.Clear();
```

### Смотрите также

* class [DropDownItemCollection](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
