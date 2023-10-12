---
title: FootnoteOptions.Position
second_title: Aspose.Words für .NET-API-Referenz
description: FootnoteOptions eigendom. Gibt die Position der Fußnoten an.
type: docs
weight: 30
url: /de/net/aspose.words.notes/footnoteoptions/position/
---
## FootnoteOptions.Position property

Gibt die Position der Fußnoten an.

```csharp
public FootnotePosition Position { get; set; }
```

### Beispiele

Zeigt, wie Sie einen anderen Ort auswählen, an dem das Dokument seine Fußnoten sammelt und anzeigt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Eine Fußnote ist eine Möglichkeit, dem Text eine Referenz oder einen Randkommentar hinzuzufügen
 // das den Fluss des Haupttextes nicht beeinträchtigt.
// Beim Einfügen einer Fußnote wird ein kleines hochgestelltes Referenzsymbol hinzugefügt
// am Haupttext, wo wir die Fußnote einfügen.
// Jede Fußnote erzeugt auch einen Eintrag am Ende der Seite, bestehend aus einem Symbol
// das mit dem Referenzsymbol im Haupttext übereinstimmt.
// Der Referenztext, den wir an die Methode „InsertFootnote“ des Document Builders übergeben.
builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote contents.");

// Wir können die Eigenschaft „Position“ verwenden, um zu bestimmen, wo das Dokument alle seine Fußnoten platzieren soll.
// Wenn wir den Wert der Eigenschaft „Position“ auf „FootnotePosition.BottomOfPage“ setzen,
// Jede Fußnote wird am Ende der Seite angezeigt, die ihre Referenzmarke enthält. Dies ist der Standardwert.
// Wenn wir den Wert der Eigenschaft „Position“ auf „FootnotePosition.BeneathText“ setzen,
// Jede Fußnote wird am Ende des Seitentextes angezeigt, der ihre Referenzmarke enthält.
doc.FootnoteOptions.Position = footnotePosition;

doc.Save(ArtifactsDir + "InlineStory.PositionFootnote.docx");
```

### Siehe auch

* enum [FootnotePosition](../../footnoteposition/)
* class [FootnoteOptions](../)
* namensraum [Aspose.Words.Notes](../../footnoteoptions/)
* Montage [Aspose.Words](../../../)


