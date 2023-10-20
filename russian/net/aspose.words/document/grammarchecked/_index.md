---
title: Document.GrammarChecked
linktitle: GrammarChecked
articleTitle: GrammarChecked
second_title: Aspose.Words для .NET
description: Document GrammarChecked свойство. Возвращаетистинный если документ проверен на грамматику на С#.
type: docs
weight: 180
url: /ru/net/aspose.words/document/grammarchecked/
---
## Document.GrammarChecked property

Возвращает`истинный` если документ проверен на грамматику.

```csharp
public bool GrammarChecked { get; set; }
```

## Примечания

Чтобы перепроверить грамматику в документе, установите для этого свойства значение`ЛОЖЬ` .

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
