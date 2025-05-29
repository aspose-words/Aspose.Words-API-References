---
title: EndnoteOptions.StartNumber
linktitle: StartNumber
articleTitle: StartNumber
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die StartNumber-Eigenschaft von EndnoteOptions Ihr Dokument verbessert, indem sie die ersten nummerierten Endnoten für mehr Klarheit und Organisation anpasst.
type: docs
weight: 40
url: /de/net/aspose.words.notes/endnoteoptions/startnumber/
---
## EndnoteOptions.StartNumber property

Gibt die Startnummer oder das Startzeichen für die ersten automatisch nummerierten Endnoten an.

```csharp
public int StartNumber { get; set; }
```

## Bemerkungen

Diese Eigenschaft ist nur wirksam, wenn[`RestartRule`](../restartrule/)ist auf eingestelltContinuous.

## Beispiele

Zeigt, wie eine Zahl festgelegt wird, bei der im Dokument mit der Zählung der Fußnoten/Endnoten begonnen wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fußnoten und Endnoten sind eine Möglichkeit, einen Verweis oder einen Randkommentar an den Text anzuhängen
    // das den Textfluss des Hauptteils nicht beeinträchtigt.
// Das Einfügen einer Fußnote/Endnote fügt ein kleines hochgestelltes Referenzsymbol hinzu
// im Haupttext, wo wir die Fußnote/Endnote einfügen.
// Jede Fußnote/Endnote erzeugt ebenfalls einen Eintrag, der aus einem Symbol besteht
// das mit dem Referenzsymbol im Haupttext übereinstimmt.
// Der Referenztext, den wir an die Methode „InsertEndnote“ des Dokumentgenerators übergeben.
// Fußnoteneinträge erscheinen standardmäßig am Ende jeder Seite, die Folgendes enthält:
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

// Standardmäßig ist das Referenzsymbol für jede Fußnote und Endnote der Index
// unter allen Fußnoten/Endnoten des Dokuments. Jedes Dokument verwaltet separate Zählungen
// für Fußnoten und für Endnoten, die beide bei 1 beginnen.
Assert.AreEqual(1, doc.FootnoteOptions.StartNumber);
Assert.AreEqual(1, doc.EndnoteOptions.StartNumber);

// Wir können die Eigenschaft "StartNumber" verwenden, um das Dokument zu erhalten
// Beginnen Sie mit der Zählung einer Fuß- oder Endnote bei einer anderen Zahl.
doc.EndnoteOptions.NumberStyle = NumberStyle.Arabic;
doc.EndnoteOptions.StartNumber = 50;

doc.Save(ArtifactsDir + "InlineStory.StartNumber.docx");
```

### Siehe auch

* class [EndnoteOptions](../)
* namensraum [Aspose.Words.Notes](../../../aspose.words.notes/)
* Montage [Aspose.Words](../../../)
