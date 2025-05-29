---
title: CustomDocumentProperties Class
linktitle: CustomDocumentProperties
articleTitle: CustomDocumentProperties
second_title: Aspose.Words для .NET
description: Откройте для себя Aspose.Words.Properties.CustomDocumentProperties для управления пользовательскими свойствами документа без усилий. Улучшите управление документами сегодня!
type: docs
weight: 5190
url: /ru/net/aspose.words.properties/customdocumentproperties/
---
## CustomDocumentProperties class

Коллекция пользовательских свойств документа.

Чтобы узнать больше, посетите[Работа со свойствами документа](https://docs.aspose.com/words/net/work-with-document-properties/) документальная статья.

```csharp
public class CustomDocumentProperties : DocumentPropertyCollection
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Count](../../aspose.words.properties/documentpropertycollection/count/) { get; } | Получает количество элементов в коллекции. |
| [Item](../../aspose.words.properties/documentpropertycollection/item/) { get; } | Возвращает[`DocumentProperty`](../documentproperty/) объект по индексу. |
| virtual [Item](../../aspose.words.properties/documentpropertycollection/item/) { get; } | Возвращает[`DocumentProperty`](../documentproperty/) объект по имени свойства. |

## Методы

| Имя | Описание |
| --- | --- |
| [Add](../../aspose.words.properties/customdocumentproperties/add/#add)(*string, bool*) | Создает новое пользовательское свойство документаBoolean тип данных. |
| [Add](../../aspose.words.properties/customdocumentproperties/add/#add_3)(*string, DateTime*) | Создает новое пользовательское свойство документаDateTime тип данных. |
| [Add](../../aspose.words.properties/customdocumentproperties/add/#add_1)(*string, double*) | Создает новое пользовательское свойство документаDouble тип данных. |
| [Add](../../aspose.words.properties/customdocumentproperties/add/#add_2)(*string, int*) | Создает новое пользовательское свойство документаNumber тип данных. |
| [Add](../../aspose.words.properties/customdocumentproperties/add/#add_4)(*string, string*) | Создает новое пользовательское свойство документаString тип данных. |
| [AddLinkToContent](../../aspose.words.properties/customdocumentproperties/addlinktocontent/)(*string, string*) | Создает новое связанное с содержимым пользовательское свойство документа. |
| [Clear](../../aspose.words.properties/documentpropertycollection/clear/)() | Удаляет все свойства из коллекции. |
| [Contains](../../aspose.words.properties/documentpropertycollection/contains/)(*string*) | Возврат`истинный` если свойство с указанным именем существует в коллекции. |
| [GetEnumerator](../../aspose.words.properties/documentpropertycollection/getenumerator/)() | Возвращает объект перечислителя, который можно использовать для перебора всех элементов в коллекции. |
| [IndexOf](../../aspose.words.properties/documentpropertycollection/indexof/)(*string*) | Получает индекс свойства по имени. |
| [Remove](../../aspose.words.properties/documentpropertycollection/remove/)(*string*) | Удаляет свойство с указанным именем из коллекции. |
| [RemoveAt](../../aspose.words.properties/documentpropertycollection/removeat/)(*int*) | Удаляет свойство по указанному индексу. |

## Примечания

Каждый[`DocumentProperty`](../documentproperty/) объект представляет собой пользовательское свойство документа-контейнера.

Имена свойств нечувствительны к регистру.

Объекты недвижимости в коллекции отсортированы в алфавитном порядке по названию.

## Примеры

Показывает, как работать с пользовательскими свойствами документа.

```csharp
Document doc = new Document(MyDir + "Properties.docx");

// Каждый документ содержит набор пользовательских свойств, которые, как и встроенные свойства, представляют собой пары ключ-значение.
 // Документ имеет фиксированный список встроенных свойств. Пользователь создает все пользовательские свойства.
Assert.AreEqual("Value of custom document property", doc.CustomDocumentProperties["CustomProperty"].ToString());

doc.CustomDocumentProperties.Add("CustomProperty2", "Value of custom document property #2");

Console.WriteLine("Custom Properties:");
foreach (var customDocumentProperty in doc.CustomDocumentProperties)
{
    Console.WriteLine(customDocumentProperty.Name);
    Console.WriteLine($"\tType:\t{customDocumentProperty.Type}");
    Console.WriteLine($"\tValue:\t\"{customDocumentProperty.Value}\"");
}
```

### Смотрите также

* class [Document](../../aspose.words/document/)
* property [BuiltInDocumentProperties](../../aspose.words/document/builtindocumentproperties/)
* property [CustomDocumentProperties](../../aspose.words/document/customdocumentproperties/)
* class [DocumentPropertyCollection](../documentpropertycollection/)
* пространство имен [Aspose.Words.Properties](../../aspose.words.properties/)
* сборка [Aspose.Words](../../)
