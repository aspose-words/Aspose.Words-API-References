---
title: Enum EndnotePosition
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Notes.EndnotePosition opsomming. Definiert die Position der Endnote.
type: docs
weight: 4010
url: /de/net/aspose.words.notes/endnoteposition/
---
## EndnotePosition enumeration

Definiert die Position der Endnote.

```csharp
public enum EndnotePosition
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| EndOfSection | `0` | Endnoten werden am Ende des Abschnitts ausgegeben. |
| EndOfDocument | `3` | Endnoten werden am Ende des Dokuments ausgegeben. |

### Beispiele

Zeigt, wie Sie einen anderen Ort auswählen, an dem das Dokument seine Endnoten sammelt und anzeigt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Eine Endnote ist eine Möglichkeit, eine Referenz oder einen Nebenkommentar an Text anzuhängen
// das den Fluss des Haupttextes nicht stört. 
// Das Einfügen einer Endnote fügt ein kleines hochgestelltes Referenzsymbol hinzu
// am Haupttext, wo wir die Endnote einfügen.
// Jede Endnote erzeugt auch einen Eintrag am Ende des Dokuments, bestehend aus einem Symbol
// das mit dem Referenzsymbol im Haupttext übereinstimmt.
// Der Referenztext, den wir an die "InsertEndnote"-Methode des Dokumenterstellers übergeben.
builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote contents.");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("This is the second section.");

// Wir können die Eigenschaft "Position" verwenden, um zu bestimmen, wo das Dokument alle seine Endnoten platzieren wird.
// Wenn wir den Wert der Eigenschaft "Position" auf "EndnotePosition.EndOfDocument" setzen,
// Jede Fußnote wird in einer Sammlung am Ende des Dokuments angezeigt. Dies ist der Standardwert.
// Wenn wir den Wert der Eigenschaft "Position" auf "EndnotePosition.EndOfSection" setzen,
// Jede Fußnote wird in einer Sammlung am Ende des Abschnitts angezeigt, dessen Text das Referenzzeichen der Endnote enthält.
doc.EndnoteOptions.Position = endnotePosition;

doc.Save(ArtifactsDir + "InlineStory.PositionEndnote.docx");
```

### Siehe auch

* class [EndnoteOptions](../endnoteoptions/)
* namensraum [Aspose.Words.Notes](../../aspose.words.notes/)
* Montage [Aspose.Words](../../)


