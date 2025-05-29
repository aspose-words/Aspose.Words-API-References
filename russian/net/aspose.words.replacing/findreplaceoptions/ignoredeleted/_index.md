---
title: FindReplaceOptions.IgnoreDeleted
linktitle: IgnoreDeleted
articleTitle: IgnoreDeleted
second_title: Aspose.Words для .NET
description: Откройте для себя свойство FindReplaceOptions IgnoreDeleted, управляйте видимостью текста в удаленных ревизиях с помощью простого булевого переключения. Улучшите свой опыт редактирования!
type: docs
weight: 60
url: /ru/net/aspose.words.replacing/findreplaceoptions/ignoredeleted/
---
## FindReplaceOptions.IgnoreDeleted property

Возвращает или задает логическое значение, указывающее, следует ли игнорировать текст внутри удаленных ревизий. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool IgnoreDeleted { get; set; }
```

## Примеры

Показывает, как включать или игнорировать текст внутри удаленных ревизий во время операции поиска и замены.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

// Начать отслеживать изменения и удалить второй абзац, что приведет к удалению изменения.
// Этот абзац будет сохраняться в документе до тех пор, пока мы не примем удаление редакции.
doc.StartTrackRevisions("John Doe", DateTime.Now);
doc.FirstSection.Body.Paragraphs[1].Remove();
doc.StopTrackRevisions();

Assert.True(doc.FirstSection.Body.Paragraphs[1].IsDeleteRevision);

// Мы можем использовать объект «FindReplaceOptions» для изменения процесса поиска и замены.
FindReplaceOptions options = new FindReplaceOptions();

// Установите флаг "IgnoreDeleted" на "true", чтобы получить функцию поиска и замены
// операция по игнорированию абзацев, являющихся удаленными редакциями.
// Установите флаг "IgnoreDeleted" на "false", чтобы получить функцию поиска и замены
// операция также для поиска текста внутри удаленных ревизий.
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
