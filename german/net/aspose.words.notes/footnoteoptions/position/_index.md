---
title: FootnoteOptions.Position
linktitle: Position
articleTitle: Position
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die Eigenschaft „FootnoteOptions Position“ Ihr Dokumentlayout verbessert, indem sie die Platzierung von Fußnoten präzise steuert und so die Lesbarkeit verbessert.
type: docs
weight: 30
url: /de/net/aspose.words.notes/footnoteoptions/position/
---
## FootnoteOptions.Position property

Gibt die Position der Fußnoten an.

```csharp
public FootnotePosition Position { get; set; }
```

## Beispiele

Zeigt, wie Sie einen anderen Ort auswählen, an dem das Dokument seine Fußnoten sammelt und anzeigt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Eine Fußnote ist eine Möglichkeit, einem Text einen Verweis oder einen Randkommentar hinzuzufügen.
    // das den Textfluss des Hauptteils nicht beeinträchtigt.
// Das Einfügen einer Fußnote fügt ein kleines hochgestelltes Referenzsymbol hinzu
// im Haupttext, wo wir die Fußnote einfügen.
// Jede Fußnote erzeugt auch einen Eintrag am Ende der Seite, bestehend aus einem Symbol
// das mit dem Referenzsymbol im Haupttext übereinstimmt.
// Der Referenztext, den wir an die Methode „InsertFootnote“ des Dokumentgenerators übergeben.
builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote contents.");

// Mit der Eigenschaft „Position“ können wir bestimmen, wo im Dokument alle Fußnoten platziert werden.
// Wenn wir den Wert der Eigenschaft „Position“ auf „FootnotePosition.BottomOfPage“ setzen,
// Jede Fußnote wird unten auf der Seite angezeigt, die das entsprechende Referenzzeichen enthält. Dies ist der Standardwert.
// Wenn wir den Wert der Eigenschaft „Position“ auf „FootnotePosition.BeneathText“ setzen,
// Jede Fußnote wird am Ende des Seitentextes angezeigt, der ihr Referenzzeichen enthält.
doc.FootnoteOptions.Position = footnotePosition;

doc.Save(ArtifactsDir + "InlineStory.PositionFootnote.docx");
```

### Siehe auch

* enum [FootnotePosition](../../footnoteposition/)
* class [FootnoteOptions](../)
* namensraum [Aspose.Words.Notes](../../../aspose.words.notes/)
* Montage [Aspose.Words](../../../)
