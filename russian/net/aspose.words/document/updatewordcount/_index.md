---
title: Document.UpdateWordCount
linktitle: UpdateWordCount
articleTitle: UpdateWordCount
second_title: Aspose.Words для .NET
description: Повысьте эффективность вашего документа с помощью метода UpdateWordCount, обеспечивающего точные свойства подсчета слов для лучшего редактирования и просмотра.
type: docs
weight: 850
url: /ru/net/aspose.words/document/updatewordcount/
---
## UpdateWordCount() {#updatewordcount}

Обновляет свойства количества слов в документе.

```csharp
public void UpdateWordCount()
```

## Примечания

`UpdateWordCount` пересчитывает и обновляет свойства «Символы», «Слова» и «Параграфы » в[`BuiltInDocumentProperties`](../builtindocumentproperties/) коллекция[`Document`](../).

Обратите внимание, что`UpdateWordCount` не обновляет количество строк и свойства страниц. Используйте`UpdateWordCount` перегрузка и пропуск`истинный` значение в качестве параметра для этого.

При использовании ознакомительной версии водяной знак оценки также будет включен в количество слов.

## Примеры

Показывает, как обновить все метки списков в документе.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder.Write("Ut enim ad minim veniam, " +
                "quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Aspose.Words не отслеживает подобные показатели документов в режиме реального времени.
Assert.AreEqual(0, doc.BuiltInDocumentProperties.Characters);
Assert.AreEqual(0, doc.BuiltInDocumentProperties.Words);
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Paragraphs);
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Lines);

// Чтобы получить точные значения для трех из этих свойств, нам придется обновить их вручную.
doc.UpdateWordCount();

Assert.AreEqual(196, doc.BuiltInDocumentProperties.Characters);
Assert.AreEqual(36, doc.BuiltInDocumentProperties.Words);
Assert.AreEqual(2, doc.BuiltInDocumentProperties.Paragraphs);

// Для подсчета количества строк нам потребуется вызвать определенную перегрузку метода обновления.
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Lines);

doc.UpdateWordCount(true);

Assert.AreEqual(4, doc.BuiltInDocumentProperties.Lines);
```

### Смотрите также

* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## UpdateWordCount(*bool*) {#updatewordcount_1}

Обновляет свойства количества слов в документе, опционально обновляет[`Lines`](../../../aspose.words.properties/builtindocumentproperties/lines/) свойство.

```csharp
public void UpdateWordCount(bool updateLinesCount)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| updateLinesCount | Boolean | `истинный` если необходимо подсчитать количество строк в документе. |

## Примечания

Этот метод перестроит макет страницы документа.

## Примеры

Показывает, как обновить все метки списков в документе.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder.Write("Ut enim ad minim veniam, " +
                "quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Aspose.Words не отслеживает подобные показатели документов в режиме реального времени.
Assert.AreEqual(0, doc.BuiltInDocumentProperties.Characters);
Assert.AreEqual(0, doc.BuiltInDocumentProperties.Words);
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Paragraphs);
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Lines);

// Чтобы получить точные значения для трех из этих свойств, нам придется обновить их вручную.
doc.UpdateWordCount();

Assert.AreEqual(196, doc.BuiltInDocumentProperties.Characters);
Assert.AreEqual(36, doc.BuiltInDocumentProperties.Words);
Assert.AreEqual(2, doc.BuiltInDocumentProperties.Paragraphs);

// Для подсчета количества строк нам потребуется вызвать определенную перегрузку метода обновления.
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Lines);

doc.UpdateWordCount(true);

Assert.AreEqual(4, doc.BuiltInDocumentProperties.Lines);
```

### Смотрите также

* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
