---
title: Document.ShowSpellingErrors
linktitle: ShowSpellingErrors
articleTitle: ShowSpellingErrors
second_title: Aspose.Words для .NET
description: Контролируйте видимость орфографических ошибок в документе с помощью свойства ShowSpellingErrors. Улучшите процесс редактирования и повысьте качество документа.
type: docs
weight: 420
url: /ru/net/aspose.words/document/showspellingerrors/
---
## Document.ShowSpellingErrors property

Указывает, отображать ли орфографические ошибки в этом документе.

```csharp
public bool ShowSpellingErrors { get; set; }
```

## Примеры

Показывает, как показать/скрыть ошибки в документе.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте два предложения с ошибками, которые будут учтены
// средствами проверки орфографии и грамматики в Microsoft Word.
builder.Writeln("There is a speling error in this sentence.");
builder.Writeln("Their is a grammatical error in this sentence.");

// Если эти параметры включены, то орфографические ошибки будут подчеркнуты
// в выходном документе неровной красной линией, а двойная синяя линия будет выделять грамматические ошибки.
doc.ShowGrammaticalErrors = showErrors;
doc.ShowSpellingErrors = showErrors;

doc.Save(ArtifactsDir + "Document.SpellingAndGrammarErrors.docx");
```

### Смотрите также

* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
