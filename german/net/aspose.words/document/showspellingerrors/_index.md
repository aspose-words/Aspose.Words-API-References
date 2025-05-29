---
title: Document.ShowSpellingErrors
linktitle: ShowSpellingErrors
articleTitle: ShowSpellingErrors
second_title: Aspose.Words für .NET
description: Steuern Sie die Sichtbarkeit von Rechtschreibfehlern in Ihrem Dokument mit der Eigenschaft „ShowSpellingErrors“. Optimieren Sie Ihren Bearbeitungsprozess und verbessern Sie die Dokumentqualität.
type: docs
weight: 420
url: /de/net/aspose.words/document/showspellingerrors/
---
## Document.ShowSpellingErrors property

Gibt an, ob Rechtschreibfehler in diesem Dokument angezeigt werden sollen.

```csharp
public bool ShowSpellingErrors { get; set; }
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
