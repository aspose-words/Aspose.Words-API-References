---
title: Document.GrammarChecked
linktitle: GrammarChecked
articleTitle: GrammarChecked
second_title: Aspose.Words für .NET
description: Sichern Sie die Qualität Ihres Dokuments mit der Funktion „GrammarChecked“. Finden Sie heraus, ob Ihr Text grammatikalisch geprüft ist, um ein professionelles Ergebnis zu erzielen.
type: docs
weight: 190
url: /de/net/aspose.words/document/grammarchecked/
---
## Document.GrammarChecked property

Rückgaben`WAHR` ob das Dokument auf Grammatik geprüft wurde.

```csharp
public bool GrammarChecked { get; set; }
```

## Bemerkungen

Um die Grammatik im Dokument erneut zu überprüfen, setzen Sie diese Eigenschaft auf`FALSCH` .

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
