---
title: DropDownItemCollection Class
linktitle: DropDownItemCollection
articleTitle: DropDownItemCollection
second_title: Aspose.Words для .NET
description: Изучите класс Aspose.Words.Fields.DropDownItemCollection — ваше идеальное решение для легкого управления раскрывающимися элементами в полях форм!
type: docs
weight: 1910
url: /ru/net/aspose.words.fields/dropdownitemcollection/
---
## DropDownItemCollection class

Коллекция строк, представляющих все элементы в раскрывающемся поле формы.

Чтобы узнать больше, посетите[Работа с полями](https://docs.aspose.com/words/net/working-with-fields/) документальная статья.

```csharp
public class DropDownItemCollection : IEnumerable<string>
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Count](../../aspose.words.fields/dropdownitemcollection/count/) { get; } | Получает количество элементов, содержащихся в коллекции. |
| [Item](../../aspose.words.fields/dropdownitemcollection/item/) { get; set; } | Получает или задает элемент по указанному индексу. |

## Методы

| Имя | Описание |
| --- | --- |
| [Add](../../aspose.words.fields/dropdownitemcollection/add/)(*string*) | Добавляет строку в конец коллекции. |
| [Clear](../../aspose.words.fields/dropdownitemcollection/clear/)() | Удаляет все элементы из коллекции. |
| [Contains](../../aspose.words.fields/dropdownitemcollection/contains/)(*string*) | Определяет, содержит ли коллекция указанное значение. |
| [GetEnumerator](../../aspose.words.fields/dropdownitemcollection/getenumerator/)() | Возвращает объект перечислителя, который можно использовать для перебора всех элементов в коллекции. |
| [IndexOf](../../aspose.words.fields/dropdownitemcollection/indexof/)(*string*) | Возвращает отсчитываемый от нуля индекс указанного значения в коллекции. |
| [Insert](../../aspose.words.fields/dropdownitemcollection/insert/)(*int, string*) | Вставляет строку в коллекцию по указанному индексу. |
| [Remove](../../aspose.words.fields/dropdownitemcollection/remove/)(*string*) | Удаляет указанное значение из коллекции. |
| [RemoveAt](../../aspose.words.fields/dropdownitemcollection/removeat/)(*int*) | Удаляет значение по указанному индексу. |

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

* class [FormField](../formfield/)
* property [DropDownItems](../formfield/dropdownitems/)
* пространство имен [Aspose.Words.Fields](../../aspose.words.fields/)
* сборка [Aspose.Words](../../)
