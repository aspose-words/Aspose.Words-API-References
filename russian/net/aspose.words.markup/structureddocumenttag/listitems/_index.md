---
title: StructuredDocumentTag.ListItems
second_title: Справочник по API Aspose.Words для .NET
description: StructuredDocumentTag свойство. получаетSdtListItemCollection связанные с этим СДТ .
type: docs
weight: 180
url: /ru/net/aspose.words.markup/structureddocumenttag/listitems/
---
## StructuredDocumentTag.ListItems property

получает[`SdtListItemCollection`](../../sdtlistitemcollection/) связанные с этим **СДТ** .

```csharp
public SdtListItemCollection ListItems { get; }
```

### Примечания

Доступ к этому свойству будет работать только дляComboBox или жеDropDownList Типы SDT.

Для всех других типов SDT будет иметь место исключение.

### Примеры

Показывает, как работать с тегами структурированного документа с раскрывающимся списком.

```csharp
Document doc = new Document();
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.DropDownList, MarkupLevel.Block);
doc.FirstSection.Body.AppendChild(tag);

// Структурированный тег документа с раскрывающимся списком — это форма, которая позволяет пользователю
// выберите вариант из списка, щелкнув левой кнопкой мыши и открыв форму в Microsoft Word.
// Свойство "ListItems" содержит все элементы списка, и каждый элемент списка является "SdtListItem".
SdtListItemCollection listItems = tag.ListItems;
listItems.Add(new SdtListItem("Value 1"));

Assert.AreEqual(listItems[0].DisplayText, listItems[0].Value);

// Добавляем еще 3 элемента списка. Инициализируйте эти элементы, используя другой конструктор для первого элемента.
// для отображения строк, которые отличаются от их значений.
listItems.Add(new SdtListItem("Item 2", "Value 2"));
listItems.Add(new SdtListItem("Item 3", "Value 3"));
listItems.Add(new SdtListItem("Item 4", "Value 4"));

Assert.AreEqual(4, listItems.Count);

// В раскрывающемся списке отображается первый элемент. Назначьте другой элемент списка «SelectedValue», чтобы отобразить его.
listItems.SelectedValue = listItems[3];

Assert.AreEqual("Value 4", listItems.SelectedValue.Value);

// Перечисляем коллекцию и печатаем каждый элемент.
using (IEnumerator<SdtListItem> enumerator = listItems.GetEnumerator())
{
    while (enumerator.MoveNext())
        if (enumerator.Current != null)
            Console.WriteLine($"List item: {enumerator.Current.DisplayText}, value: {enumerator.Current.Value}");
}

 // Удалить последний элемент списка.
listItems.RemoveAt(3);

Assert.AreEqual(3, listItems.Count);

// Так как наш раскрывающийся список настроен на отображение удаленного элемента по умолчанию, укажите существующий элемент для отображения.
listItems.SelectedValue = listItems[1];

doc.Save(ArtifactsDir + "StructuredDocumentTag.ListItemCollection.docx");

// Используйте метод «Очистить», чтобы сразу очистить всю коллекцию раскрывающихся элементов.
listItems.Clear();

Assert.AreEqual(0, listItems.Count);
```

### Смотрите также

* class [SdtListItemCollection](../../sdtlistitemcollection/)
* class [StructuredDocumentTag](../)
* пространство имен [Aspose.Words.Markup](../../structureddocumenttag/)
* сборка [Aspose.Words](../../../)


