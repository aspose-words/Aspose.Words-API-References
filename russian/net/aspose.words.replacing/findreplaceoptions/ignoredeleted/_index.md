---
title: FindReplaceOptions.IgnoreDeleted
linktitle: IgnoreDeleted
articleTitle: IgnoreDeleted
second_title: Aspose.Words для .NET
description: FindReplaceOptions IgnoreDeleted свойство. Получает или задает логическое значение указывающее следует ли игнорировать текст внутри удаляемых ревизий. Значение по умолчаниюЛОЖЬ  на С#.
type: docs
weight: 60
url: /ru/net/aspose.words.replacing/findreplaceoptions/ignoredeleted/
---
## FindReplaceOptions.IgnoreDeleted property

Получает или задает логическое значение, указывающее, следует ли игнорировать текст внутри удаляемых ревизий. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool IgnoreDeleted { get; set; }
```

## Примеры

Показывает, как включать или игнорировать текст внутри редакций удаления во время операции поиска и замены.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

// Начинаем отслеживать ревизии и удаляем второй абзац, что создаёт удаляемую ревизию.
// Этот абзац будет сохраняться в документе до тех пор, пока мы не примем удаление версии.
doc.StartTrackRevisions("John Doe", DateTime.Now);
doc.FirstSection.Body.Paragraphs[1].Remove();
doc.StopTrackRevisions();

Assert.True(doc.FirstSection.Body.Paragraphs[1].IsDeleteRevision);

// Мы можем использовать объект «FindReplaceOptions» для изменения процесса поиска и замены.
FindReplaceOptions options = new FindReplaceOptions();

// Установите флаг «IgnoreDeleted» в значение «true», чтобы получить возможность поиска и замены
// операция игнорирования абзацев, которые являются удаленными редакциями.
// Установите флаг «IgnoreDeleted» в значение «false», чтобы получить возможность поиска и замены
// операция для поиска текста внутри редакций удаления.
options.IgnoreDeleted = ignoreTextInsideDeleteRevisions;

doc.Range.Replace("Hello", "Greetings", options);

Assert.AreEqual(
    ignoreTextInsideDeleteRevisions
        ? "Greetings world!\rHello again!"
        : "Greetings world!\rGreetings again!", doc.GetText().Trim());
```

### Смотрите также

* class [FindReplaceOptions](../)
* пространство имен [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* сборка [Aspose.Words](../../../)
