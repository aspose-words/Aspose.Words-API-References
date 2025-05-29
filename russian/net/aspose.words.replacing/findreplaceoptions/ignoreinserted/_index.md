---
title: FindReplaceOptions.IgnoreInserted
linktitle: IgnoreInserted
articleTitle: IgnoreInserted
second_title: Aspose.Words для .NET
description: Откройте для себя свойство FindReplaceOptions IgnoreInserted, управляйте обработкой текста в ревизиях вставки с помощью этой простой логической настройки. Значение по умолчанию — false.
type: docs
weight: 100
url: /ru/net/aspose.words.replacing/findreplaceoptions/ignoreinserted/
---
## FindReplaceOptions.IgnoreInserted property

Возвращает или задает логическое значение, указывающее, следует ли игнорировать текст внутри вставленных ревизий. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool IgnoreInserted { get; set; }
```

## Примеры

Показывает, как включать или игнорировать текст внутри вставленных правок во время операции поиска и замены.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

// Начать отслеживать правки и вставить абзац. Этот абзац будет вставленной правкой.
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("Hello again!");
doc.StopTrackRevisions();

Assert.True(doc.FirstSection.Body.Paragraphs[1].IsInsertRevision);

// Мы можем использовать объект «FindReplaceOptions» для изменения процесса поиска и замены.
FindReplaceOptions options = new FindReplaceOptions();

// Установите флаг "IgnoreInserted" на "true", чтобы получить функцию поиска и замены
// операция по игнорированию абзацев, являющихся вставленными правками.
// Установите флаг "IgnoreInserted" на "false", чтобы получить функцию поиска и замены
// операция также для поиска текста внутри вставок ревизий.
options.IgnoreInserted = ignoreTextInsideInsertRevisions;

doc.Range.Replace("Hello", "Greetings", options);

Assert.AreEqual(
    ignoreTextInsideInsertRevisions
        ? "Greetings world!\rHello again!"
        : "Greetings world!\rGreetings again!", doc.GetText().Trim());
```

### Смотрите также

* class [FindReplaceOptions](../)
* пространство имен [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* сборка [Aspose.Words](../../../)
