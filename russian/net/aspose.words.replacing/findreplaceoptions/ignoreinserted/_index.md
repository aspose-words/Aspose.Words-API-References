---
title: FindReplaceOptions.IgnoreInserted
linktitle: IgnoreInserted
articleTitle: IgnoreInserted
second_title: Aspose.Words для .NET
description: FindReplaceOptions IgnoreInserted свойство. Получает или задает логическое значение указывающее следует ли игнорировать текст внутри редакций вставки. Значение по умолчаниюЛОЖЬ  на С#.
type: docs
weight: 100
url: /ru/net/aspose.words.replacing/findreplaceoptions/ignoreinserted/
---
## FindReplaceOptions.IgnoreInserted property

Получает или задает логическое значение, указывающее, следует ли игнорировать текст внутри редакций вставки. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool IgnoreInserted { get; set; }
```

## Примеры

Показывает, как включать или игнорировать текст внутри редакций вставки во время операции поиска и замены.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

// Начинаем отслеживать изменения и вставляем абзац. Этот абзац будет вставленной редакцией.
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("Hello again!");
doc.StopTrackRevisions();

Assert.True(doc.FirstSection.Body.Paragraphs[1].IsInsertRevision);

// Мы можем использовать объект «FindReplaceOptions» для изменения процесса поиска и замены.
FindReplaceOptions options = new FindReplaceOptions();

// Установите флаг «IgnoreInserted» в значение «true», чтобы получить возможность поиска и замены
// операция игнорирования абзацев, которые являются вставленными редакциями.
// Установите флаг «IgnoreInserted» в значение «false», чтобы получить возможность поиска и замены
// операция для поиска текста внутри редакций вставки.
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
