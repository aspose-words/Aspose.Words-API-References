---
title: Document.ShowGrammaticalErrors
linktitle: ShowGrammaticalErrors
articleTitle: ShowGrammaticalErrors
second_title: Aspose.Words für .NET
description: Kontrollieren Sie die Sichtbarkeit von Grammatikfehlern in Ihrem Dokument mit der Eigenschaft „ShowGrammaticalErrors“. Verbessern Sie mühelos Klarheit und Professionalität beim Schreiben.
type: docs
weight: 410
url: /de/net/aspose.words/document/showgrammaticalerrors/
---
## Document.ShowGrammaticalErrors property

Gibt an, ob Grammatikfehler in diesem Dokument angezeigt werden sollen.

```csharp
public bool ShowGrammaticalErrors { get; set; }
```

## Beispiele

Zeigt, wie Fehler im Dokument angezeigt/ausgeblendet werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie zwei Sätze mit Fehlern ein, die erkannt werden würden
// durch die Rechtschreib- und Grammatikprüfung in Microsoft Word.
builder.Writeln("There is a speling error in this sentence.");
builder.Writeln("Their is a grammatical error in this sentence.");

// Wenn diese Optionen aktiviert sind, werden Rechtschreibfehler unterstrichen
// im Ausgabedokument durch eine gezackte rote Linie und eine doppelte blaue Linie hebt Grammatikfehler hervor.
doc.ShowGrammaticalErrors = showErrors;
doc.ShowSpellingErrors = showErrors;

doc.Save(ArtifactsDir + "Document.SpellingAndGrammarErrors.docx");
```

### Siehe auch

* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
