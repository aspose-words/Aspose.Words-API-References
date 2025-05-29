---
title: EndnoteOptions.Position
linktitle: Position
articleTitle: Position
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die Eigenschaft „EndnoteOptions Position“ das Layout Ihres Dokuments verbessert, indem sie die ideale Platzierung für Endnoten angibt. Optimieren Sie Ihr Schreiben noch heute!
type: docs
weight: 20
url: /de/net/aspose.words.notes/endnoteoptions/position/
---
## EndnoteOptions.Position property

Gibt die Position der Endnoten an.

```csharp
public EndnotePosition Position { get; set; }
```

## Beispiele

Zeigt, wie Sie einen anderen Ort auswählen, an dem das Dokument seine Endnoten sammelt und anzeigt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Eine Endnote ist eine Möglichkeit, einen Verweis oder einen Randkommentar an den Text anzuhängen
    // das den Textfluss des Hauptteils nicht beeinträchtigt.
// Das Einfügen einer Endnote fügt ein kleines hochgestelltes Referenzsymbol hinzu
// im Haupttext, wo wir die Endnote einfügen.
// Jede Endnote erzeugt auch einen Eintrag am Ende des Dokuments, bestehend aus einem Symbol
// das mit dem Referenzsymbol im Haupttext übereinstimmt.
// Der Referenztext, den wir an die Methode „InsertEndnote“ des Dokumentgenerators übergeben.
builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote contents.");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("This is the second section.");

// Wir können die Eigenschaft „Position“ verwenden, um zu bestimmen, wo das Dokument alle seine Endnoten platziert.
// Wenn wir den Wert der Eigenschaft „Position“ auf „EndnotePosition.EndOfDocument“ setzen,
// Jede Fußnote wird in einer Sammlung am Ende des Dokuments angezeigt. Dies ist der Standardwert.
// Wenn wir den Wert der Eigenschaft „Position“ auf „EndnotePosition.EndOfSection“ setzen,
// Jede Fußnote wird in einer Sammlung am Ende des Abschnitts angezeigt, dessen Text das Referenzzeichen der Endnote enthält.
doc.EndnoteOptions.Position = endnotePosition;

doc.Save(ArtifactsDir + "InlineStory.PositionEndnote.docx");
```

### Siehe auch

* enum [EndnotePosition](../../endnoteposition/)
* class [EndnoteOptions](../)
* namensraum [Aspose.Words.Notes](../../../aspose.words.notes/)
* Montage [Aspose.Words](../../../)
