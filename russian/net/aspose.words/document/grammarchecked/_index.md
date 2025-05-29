---
title: Document.GrammarChecked
linktitle: GrammarChecked
articleTitle: GrammarChecked
second_title: Aspose.Words для .NET
description: Обеспечьте качество вашего документа с помощью свойства GrammarChecked. Узнайте, проверен ли ваш текст на грамматику для получения отточенных профессиональных результатов.
type: docs
weight: 190
url: /ru/net/aspose.words/document/grammarchecked/
---
## Document.GrammarChecked property

Возврат`истинный` если документ был проверен на грамматику.

```csharp
public bool GrammarChecked { get; set; }
```

## Примечания

Чтобы перепроверить грамматику в документе, установите это свойство на`ЛОЖЬ` .

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
