---
title: Document.SpellingChecked
second_title: Aspose.Words für .NET-API-Referenz
description: Document eigendom. gibt zurück Stimmt wenn das Dokument auf Rechtschreibung geprüft wurde.
type: docs
weight: 390
url: /de/net/aspose.words/document/spellingchecked/
---
## Document.SpellingChecked property

gibt zurück **Stimmt** wenn das Dokument auf Rechtschreibung geprüft wurde.

```csharp
public bool SpellingChecked { get; set; }
```

### Bemerkungen

Um die Rechtschreibung im Dokument erneut zu prüfen, setzen Sie diese Eigenschaft auf **FALSCH** .

### Beispiele

Zeigt, wie die Rechtschreib- oder Grammatikprüfung eingestellt wird.

```csharp
Document doc = new Document();

// Der String mit Rechtschreibfehlern.
doc.FirstSection.Body.FirstParagraph.Runs.Add(new Run(doc, "The speeling in this documentz is all broked."));

 // Rechtschreib-/Grammatikprüfung starten, wenn wir Eigenschaften auf „false“ setzen.
// Wir können alle Fehler in Microsoft Word über Review sehen -> Rechtschreibung & Grammatik.
// Beachten Sie, dass Microsoft Word die Grammatik-/Rechtschreibprüfung für DOC- und RTF-Dokumentformate nicht automatisch startet.
doc.SpellingChecked = checkSpellingGrammar;
doc.GrammarChecked = checkSpellingGrammar;

doc.Save(ArtifactsDir + "Document.SpellingOrGrammar.docx");
```

### Siehe auch

* class [Document](../)
* namensraum [Aspose.Words](../../document/)
* Montage [Aspose.Words](../../../)


