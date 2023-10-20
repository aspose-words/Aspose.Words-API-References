---
title: Document.SpellingChecked
linktitle: SpellingChecked
articleTitle: SpellingChecked
second_title: Aspose.Words für .NET
description: Document SpellingChecked eigendom. Gibt zurückWAHR wenn das Dokument auf Rechtschreibung geprüft wurde in C#.
type: docs
weight: 410
url: /de/net/aspose.words/document/spellingchecked/
---
## Document.SpellingChecked property

Gibt zurück`WAHR` wenn das Dokument auf Rechtschreibung geprüft wurde.

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

 // Rechtschreib-/Grammatikprüfung startet, wenn wir Eigenschaften auf „false“ setzen.
// Wir können alle Fehler in Microsoft Word über Überprüfen -> sehen. Rechtschreibung & Grammatik.
// Beachten Sie, dass Microsoft Word die Grammatik-/Rechtschreibprüfung für DOC- und RTF-Dokumentformate nicht automatisch startet.
doc.SpellingChecked = checkSpellingGrammar;
doc.GrammarChecked = checkSpellingGrammar;

doc.Save(ArtifactsDir + "Document.SpellingOrGrammar.docx");
```

### Siehe auch

* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
