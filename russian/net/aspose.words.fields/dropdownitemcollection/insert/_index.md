---
title: DropDownItemCollection.Insert
linktitle: Insert
articleTitle: Insert
second_title: Aspose.Words для .NET
description: Легко вставляйте строки в DropDownItemCollection в любом индексе с помощью нашего простого в использовании метода Insert. Улучшите управление данными сегодня!
type: docs
weight: 80
url: /ru/net/aspose.words.fields/dropdownitemcollection/insert/
---
## DropDownItemCollection.Insert method

Вставляет строку в коллекцию по указанному индексу.

```csharp
public void Insert(int index, string value)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| index | Int32 | Индекс, начинающийся с нуля, по которому вставляется значение. |
| value | String | Строка для вставки. |

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
