---
title: EndnoteOptions.StartNumber
linktitle: StartNumber
articleTitle: StartNumber
second_title: Aspose.Words für .NET
description: EndnoteOptions StartNumber eigendom. Gibt die Startnummer oder das Anfangszeichen für die ersten automatisch nummerierten Endnoten an in C#.
type: docs
weight: 40
url: /de/net/aspose.words.notes/endnoteoptions/startnumber/
---
## EndnoteOptions.StartNumber property

Gibt die Startnummer oder das Anfangszeichen für die ersten automatisch nummerierten Endnoten an.

```csharp
public int StartNumber { get; set; }
```

## Bemerkungen

Diese Eigenschaft ist nur wirksam, wenn[`RestartRule`](../restartrule/) ist auf gesetztContinuous.

## Beispiele

Zeigt, wie man eine Zahl festlegt, bei der das Dokument mit der Fußnoten-/Endnotenzählung beginnt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fußnoten und Endnoten sind eine Möglichkeit, dem Text eine Referenz oder einen Randkommentar hinzuzufügen
 // das den Fluss des Haupttextes nicht beeinträchtigt.
// Beim Einfügen einer Fußnote/Endnote wird ein kleines hochgestelltes Referenzsymbol hinzugefügt
// am Haupttext, wo wir die Fußnote/Endnote einfügen.
// Jede Fußnote/Endnote erzeugt auch einen Eintrag, der aus einem Symbol besteht
// das mit dem Referenzsymbol im Haupttext übereinstimmt.
// Der Referenztext, den wir an die „InsertEndnote“-Methode des Document Builders übergeben.
// Fußnoteneinträge werden standardmäßig unten auf jeder Seite angezeigt, die Folgendes enthält
// Ihre Referenzsymbole und Endnoten werden am Ende des Dokuments angezeigt.
builder.Write("Text 1. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 1.");
builder.Write("Text 2. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 2.");
builder.Write("Text 3. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 3.");

builder.InsertParagraph();

builder.Write("Text 1. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 1.");
builder.Write("Text 2. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 2.");
builder.Write("Text 3. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 3.");

// Standardmäßig ist das Referenzsymbol für jede Fußnote und Endnote ihr Index
// unter allen Fußnoten/Endnoten des Dokuments. Jedes Dokument verwaltet separate Zählungen
// für Fußnoten und für Endnoten, die beide bei 1 beginnen.
Assert.AreEqual(1, doc.FootnoteOptions.StartNumber);
Assert.AreEqual(1, doc.EndnoteOptions.StartNumber);

// Wir können die Eigenschaft „StartNumber“ verwenden, um das Dokument abzurufen
// Beginnen Sie eine Fußnoten- oder Endnotenzählung mit einer anderen Zahl.
doc.EndnoteOptions.NumberStyle = NumberStyle.Arabic;
doc.EndnoteOptions.StartNumber = 50;

doc.Save(ArtifactsDir + "InlineStory.StartNumber.docx");
```

### Siehe auch

* class [EndnoteOptions](../)
* namensraum [Aspose.Words.Notes](../../../aspose.words.notes/)
* Montage [Aspose.Words](../../../)
