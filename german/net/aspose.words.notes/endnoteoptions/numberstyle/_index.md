---
title: EndnoteOptions.NumberStyle
second_title: Aspose.Words für .NET-API-Referenz
description: EndnoteOptions eigendom. Gibt das Zahlenformat für automatisch nummerierte Endnoten an.
type: docs
weight: 10
url: /de/net/aspose.words.notes/endnoteoptions/numberstyle/
---
## EndnoteOptions.NumberStyle property

Gibt das Zahlenformat für automatisch nummerierte Endnoten an.

```csharp
public NumberStyle NumberStyle { get; set; }
```

### Bemerkungen

Für diese Eigenschaft sind nicht alle Zahlenstile anwendbar. Die Liste der anwendbaren -Zahlenstile finden Sie im Dialogfeld „Fußnote oder Endnote einfügen“ in Microsoft Word. Wenn Sie einen nicht anwendbaren Zahlenstil auswählen , wird Microsoft Word auf einen Standardwert zurückgesetzt.

### Beispiele

Zeigt, wie der Nummernstil von Fußnoten-/Endnoten-Referenzzeichen geändert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fußnoten und Endnoten sind eine Möglichkeit, dem Text eine Referenz oder einen Randkommentar hinzuzufügen
 // das den Fluss des Haupttextes nicht beeinträchtigt.
// Beim Einfügen einer Fußnote/Endnote wird ein kleines hochgestelltes Referenzsymbol hinzugefügt
// am Haupttext, wo wir die Fußnote/Endnote einfügen.
// Jede Fußnote/Endnote erstellt auch einen Eintrag, der aus einem Symbol besteht, das mit der Referenz übereinstimmt
// Symbol im Haupttext. Der Referenztext, den wir an die Methode „InsertEndnote“ des Document Builders übergeben.
// Fußnoteneinträge werden standardmäßig unten auf jeder Seite angezeigt, die Folgendes enthält
// Ihre Referenzsymbole und Endnoten werden am Ende des Dokuments angezeigt.
builder.Write("Text 1. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 1.");
builder.Write("Text 2. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 2.");
builder.Write("Text 3. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 3.", "Custom footnote reference mark");

builder.InsertParagraph();

builder.Write("Text 1. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 1.");
builder.Write("Text 2. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 2.");
builder.Write("Text 3. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 3.", "Custom endnote reference mark");

// Standardmäßig ist das Referenzsymbol für jede Fußnote und Endnote ihr Index
// unter allen Fußnoten/Endnoten des Dokuments. Jedes Dokument verwaltet separate Zählungen
// für Fußnoten und für Endnoten. Standardmäßig werden in Fußnoten ihre Nummern mit arabischen Ziffern angezeigt.
// und Endnoten zeigen ihre Nummern in kleinen römischen Ziffern an.
Assert.AreEqual(NumberStyle.Arabic, doc.FootnoteOptions.NumberStyle);
Assert.AreEqual(NumberStyle.LowercaseRoman, doc.EndnoteOptions.NumberStyle);

// Wir können die Eigenschaft „NumberStyle“ verwenden, um benutzerdefinierte Nummerierungsstile auf Fußnoten und Endnoten anzuwenden.
// Dies hat keine Auswirkungen auf Fußnoten/Endnoten mit benutzerdefinierten Referenzmarken.
doc.FootnoteOptions.NumberStyle = NumberStyle.UppercaseRoman;
doc.EndnoteOptions.NumberStyle = NumberStyle.UppercaseLetter;

doc.Save(ArtifactsDir + "InlineStory.RefMarkNumberStyle.docx");
```

### Siehe auch

* enum [NumberStyle](../../../aspose.words/numberstyle/)
* class [EndnoteOptions](../)
* namensraum [Aspose.Words.Notes](../../endnoteoptions/)
* Montage [Aspose.Words](../../../)


