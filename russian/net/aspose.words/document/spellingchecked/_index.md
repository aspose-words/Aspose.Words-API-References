---
title: Document.SpellingChecked
linktitle: SpellingChecked
articleTitle: SpellingChecked
second_title: Aspose.Words для .NET
description: Document SpellingChecked свойство. Возвращаетистинный если документ проверен на орфографию на С#.
type: docs
weight: 410
url: /ru/net/aspose.words/document/spellingchecked/
---
## Document.SpellingChecked property

Возвращает`истинный` если документ проверен на орфографию.

```csharp
public bool SpellingChecked { get; set; }
```

## Примечания

Чтобы перепроверить орфографию в документе, установите для этого свойства значение`ЛОЖЬ` .

## Примеры

Показывает, как настроить проверку орфографии или грамматики.

```csharp
Document doc = new Document();

// Строка с орфографическими ошибками.
doc.FirstSection.Body.FirstParagraph.Runs.Add(new Run(doc, "The speeling in this documentz is all broked."));

 // Проверка орфографии/грамматики начинается, если мы установили для свойств значение false.
// Мы можем увидеть все ошибки в Microsoft Word через Обзор -> -> Правописание и усиление; Грамматика.
// Обратите внимание, что Microsoft Word не запускает автоматически проверку грамматики/орфографии для форматов документов DOC и RTF.
doc.SpellingChecked = checkSpellingGrammar;
doc.GrammarChecked = checkSpellingGrammar;

doc.Save(ArtifactsDir + "Document.SpellingOrGrammar.docx");
```

### Смотрите также

* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
