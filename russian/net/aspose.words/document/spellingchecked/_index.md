---
title: Document.SpellingChecked
linktitle: SpellingChecked
articleTitle: SpellingChecked
second_title: Aspose.Words для .NET
description: Убедитесь, что ваш документ не содержит ошибок, используя свойство SpellingChecked. Узнайте, был ли ваш контент тщательно проверен на профессиональность.
type: docs
weight: 430
url: /ru/net/aspose.words/document/spellingchecked/
---
## Document.SpellingChecked property

Возврат`истинный` если документ был проверен на орфографию.

```csharp
public bool SpellingChecked { get; set; }
```

## Примечания

Чтобы перепроверить орфографию в документе, установите для этого свойства значение`ЛОЖЬ` .

## Примеры

Показывает, как настроить проверку орфографии и грамматики.

```csharp
Document doc = new Document();

// Строка с орфографическими ошибками.
doc.FirstSection.Body.FirstParagraph.Runs.Add(new Run(doc, "The speeling in this documentz is all broked."));

// Проверка орфографии/грамматики начнется, если мы установим свойства на false.
// Мы можем увидеть все ошибки в Microsoft Word через Обзор -> Правописание и грамматика.
// Обратите внимание, что Microsoft Word не запускает автоматическую проверку грамматики/орфографии для документов формата DOC и RTF.
doc.SpellingChecked = checkSpellingGrammar;
doc.GrammarChecked = checkSpellingGrammar;

doc.Save(ArtifactsDir + "Document.SpellingOrGrammar.docx");
```

### Смотрите также

* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
