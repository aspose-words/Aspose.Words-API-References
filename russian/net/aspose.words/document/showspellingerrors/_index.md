---
title: Document.ShowSpellingErrors
second_title: Справочник по API Aspose.Words для .NET
description: Document свойство. Указывает отображать ли орфографические ошибки в этом документе.
type: docs
weight: 380
url: /ru/net/aspose.words/document/showspellingerrors/
---
## Document.ShowSpellingErrors property

Указывает, отображать ли орфографические ошибки в этом документе.

```csharp
public bool ShowSpellingErrors { get; set; }
```

### Примеры

Показывает, как показать/скрыть ошибки в документе.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставляем два предложения с ошибками, которые будут убраны
// средствами проверки орфографии и грамматики в Microsoft Word.
builder.Writeln("There is a speling error in this sentence.");
builder.Writeln("Their is a grammatical error in this sentence.");

// Если эти опции включены, то орфографические ошибки будут подчеркнуты
// в выходном документе неровной красной линией, а двойная синяя линия выделяет грамматические ошибки.
doc.ShowGrammaticalErrors = showErrors;
doc.ShowSpellingErrors = showErrors;

doc.Save(ArtifactsDir + "Document.SpellingAndGrammarErrors.docx");
```

### Смотрите также

* class [Document](../)
* пространство имен [Aspose.Words](../../document/)
* сборка [Aspose.Words](../../../)


