---
title: Document.SpellingChecked
linktitle: SpellingChecked
articleTitle: SpellingChecked
second_title: Aspose.Words für .NET
description: Stellen Sie mit der Eigenschaft „SpellingChecked“ sicher, dass Ihr Dokument fehlerfrei ist. Finden Sie heraus, ob Ihr Inhalt gründlich auf Rechtschreibung geprüft wurde, um professionelle Ergebnisse zu erzielen.
type: docs
weight: 430
url: /de/net/aspose.words/document/spellingchecked/
---
## Document.SpellingChecked property

Rückgaben`WAHR` wenn das Dokument auf Rechtschreibung geprüft wurde.

```csharp
public bool SpellingChecked { get; set; }
```

## Bemerkungen

Um die Rechtschreibung im Dokument erneut zu überprüfen, setzen Sie diese Eigenschaft auf`FALSCH` .

## Beispiele

Zeigt, wie die Rechtschreib- oder Grammatikprüfung eingestellt wird.

```csharp
Document doc = new Document();

// Die Zeichenfolge mit Rechtschreibfehlern.
doc.FirstSection.Body.FirstParagraph.Runs.Add(new Run(doc, "The speeling in this documentz is all broked."));

// Die Rechtschreib-/Grammatikprüfung beginnt, wenn wir die Eigenschaften auf „false“ setzen.
// Wir können alle Fehler in Microsoft Word über Überprüfen -> Rechtschreibung und Grammatik sehen.
// Beachten Sie, dass Microsoft Word die Grammatik-/Rechtschreibprüfung für die Dokumentformate DOC und RTF nicht automatisch startet.
doc.SpellingChecked = checkSpellingGrammar;
doc.GrammarChecked = checkSpellingGrammar;

doc.Save(ArtifactsDir + "Document.SpellingOrGrammar.docx");
```

### Siehe auch

* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
