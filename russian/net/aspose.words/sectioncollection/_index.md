---
title: Class SectionCollection
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.SectionCollection сорт. Коллекция Раздел объекты в документе.
type: docs
weight: 5450
url: /ru/net/aspose.words/sectioncollection/
---
## SectionCollection class

Коллекция **Раздел** объекты в документе.

```csharp
public class SectionCollection : NodeCollection
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | Получает количество узлов в коллекции. |
| [Item](../../aspose.words/sectioncollection/item/) { get; } | Извлекает раздел по заданному индексу. (2 indexers) |

## Методы

| Имя | Описание |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(Node) | Добавляет узел в конец коллекции. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Удаляет все узлы из этой коллекции и из документа. |
| [Contains](../../aspose.words/nodecollection/contains/)(Node) | Определяет, находится ли узел в коллекции. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | Обеспечивает простую итерацию в стиле foreach по набору узлов. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(Node) | Возвращает отсчитываемый от нуля индекс указанного узла. |
| [Insert](../../aspose.words/nodecollection/insert/)(int, Node) | Вставляет узел в коллекцию по указанному индексу. |
| [Remove](../../aspose.words/nodecollection/remove/)(Node) | Удаляет узел из коллекции и из документа. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(int) | Удаляет узел с указанным индексом из коллекции и из документа. |
| [ToArray](../../aspose.words/sectioncollection/toarray/#toarray_1)() | Копирует все разделы из коллекции в новый массив разделов. (2 methods) |

### Примечания

Документ Microsoft Word может содержать несколько разделов. Чтобы создать раздел в Microsoft Word, выберите команду «Вставить/Разрыв» и выберите тип разрыва. Разрыв указывает, начинается ли раздел на новой странице или на той же странице.

Программная вставка и удаление разделов может использоваться для настройки документов, созданных во время слияния. Если документ должен иметь различное содержимое или части содержимого в зависимости от некоторых критериев, вы можете создать «главный» документ, содержащий несколько разделов , и удалить некоторые из разделов до или после слияния почты.

### Примеры

Показывает, как добавлять и удалять разделы в документе.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 2");

Assert.AreEqual("Section 1\x000cSection 2", doc.GetText().Trim());

// Удаляем первый раздел из документа.
doc.Sections.RemoveAt(0);

Assert.AreEqual("Section 2", doc.GetText().Trim());

// Добавляем копию того, что сейчас является первым разделом, в конец документа.
int lastSectionIdx = doc.Sections.Count - 1;
Section newSection = doc.Sections[lastSectionIdx].Clone();
doc.Sections.Add(newSection);

Assert.AreEqual("Section 2\x000cSection 2", doc.GetText().Trim());
```

### Смотрите также

* class [NodeCollection](../nodecollection/)
* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)


