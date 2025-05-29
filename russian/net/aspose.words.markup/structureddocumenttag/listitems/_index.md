---
title: StructuredDocumentTag.ListItems
linktitle: ListItems
articleTitle: ListItems
second_title: Aspose.Words для .NET
description: Откройте для себя свойство StructuredDocumentTag ListItems, обеспечивающее простой доступ к SdtListItemCollection для улучшенного управления и организации документов.
type: docs
weight: 180
url: /ru/net/aspose.words.markup/structureddocumenttag/listitems/
---
## StructuredDocumentTag.ListItems property

Получает[`SdtListItemCollection`](../../sdtlistitemcollection/) связанный с этим**СДТ** .

```csharp
public SdtListItemCollection ListItems { get; }
```

## Примечания

Доступ к этому свойству будет возможен только дляComboBox илиDropDownList Типы СДТ.

Для всех остальных типов SDT возникнет исключение.

## Примеры

Показывает, как работать с тегами документа, структурированными в виде раскрывающегося списка.

```csharp
Document doc = new Document();
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.DropDownList, MarkupLevel.Block);
doc.FirstSection.Body.AppendChild(tag);

// Тег документа со структурой раскрывающегося списка — это форма, которая позволяет пользователю
// выберите вариант из списка, щелкнув левой кнопкой мыши и открыв форму в Microsoft Word.
// Свойство "ListItems" содержит все элементы списка, а каждый элемент списка является "SdtListItem".
SdtListItemCollection listItems = tag.ListItems;
listItems.Add(new SdtListItem("Value 1"));

Assert.AreEqual(listItems[0].DisplayText, listItems[0].Value);

// Добавить еще 3 элемента списка. Инициализируем эти элементы, используя другой конструктор для первого элемента
// для отображения строк, которые отличаются от своих значений.
listItems.Add(new SdtListItem("Item 2", "Value 2"));
listItems.Add(new SdtListItem("Item 3", "Value 3"));
listItems.Add(new SdtListItem("Item 4", "Value 4"));

Assert.AreEqual(4, listItems.Count);

// Раскрывающийся список отображает первый элемент. Назначьте другой элемент списка "SelectedValue", чтобы отобразить его.
listItems.SelectedValue = listItems[3];

Assert.AreEqual("Value 4", listItems.SelectedValue.Value);

// Перечислить коллекцию и вывести каждый элемент.
using (IEnumerator<SdtListItem> enumerator = listItems.GetEnumerator())
{
    while (enumerator.MoveNext())
        if (enumerator.Current != null)
            Console.WriteLine($"List item: {enumerator.Current.DisplayText}, value: {enumerator.Current.Value}");
}

 // Удалить последний элемент списка.
listItems.RemoveAt(3);

Assert.AreEqual(3, listItems.Count);

// Поскольку наш раскрывающийся список по умолчанию настроен на отображение удаленного элемента, укажите для него существующий элемент для отображения.
listItems.SelectedValue = listItems[1];

doc.Save(ArtifactsDir + "StructuredDocumentTag.ListItemCollection.docx");

// Используйте метод «Очистить», чтобы очистить всю коллекцию раскрывающихся элементов одновременно.
listItems.Clear();

Assert.AreEqual(0, listItems.Count);
```

### Смотрите также

* class [SdtListItemCollection](../../sdtlistitemcollection/)
* class [StructuredDocumentTag](../)
* пространство имен [Aspose.Words.Markup](../../../aspose.words.markup/)
* сборка [Aspose.Words](../../../)
