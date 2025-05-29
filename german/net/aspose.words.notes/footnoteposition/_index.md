---
title: FootnotePosition Enum
linktitle: FootnotePosition
articleTitle: FootnotePosition
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aufzählung Aspose.Words.Notes.FootnotePosition für eine anpassbare Platzierung von Fußnoten, die die Formatierung und Lesbarkeit von Dokumenten verbessert.
type: docs
weight: 4980
url: /de/net/aspose.words.notes/footnoteposition/
---
## FootnotePosition enumeration

Definiert die Fußnotenposition.

```csharp
public enum FootnotePosition
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| BottomOfPage | `1` | Fußnoten werden am Ende jeder Seite ausgegeben. |
| BeneathText | `2` | Fußnoten werden auf jeder Seite unter dem Text ausgegeben. |

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

* class [FootnoteOptions](../footnoteoptions/)
* namensraum [Aspose.Words.Notes](../../aspose.words.notes/)
* Montage [Aspose.Words](../../)
