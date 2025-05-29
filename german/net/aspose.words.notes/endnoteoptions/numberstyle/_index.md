---
title: EndnoteOptions.NumberStyle
linktitle: NumberStyle
articleTitle: NumberStyle
second_title: Aspose.Words für .NET
description: Entdecken Sie die NumberStyle-Eigenschaft von EndnoteOptions, um das Zahlenformat Ihrer Endnoten mühelos anzupassen. Verleihen Sie Ihrem Dokument noch heute mehr Professionalität!
type: docs
weight: 10
url: /de/net/aspose.words.notes/endnoteoptions/numberstyle/
---
## EndnoteOptions.NumberStyle property

Gibt das Zahlenformat für automatisch nummerierte Endnoten an.

```csharp
public NumberStyle NumberStyle { get; set; }
```

## Bemerkungen

Nicht alle Nummerierungsformate sind für diese Eigenschaft anwendbar. Eine Liste der anwendbaren Nummerierungsformate finden Sie im Dialogfeld „Fußnote oder Endnote einfügen“ in Microsoft Word. Wenn Sie ein nicht anwendbares Nummerierungsformat auswählen, greift Microsoft Word auf den Standardwert zurück.

## Beispiele

Zeigt, wie der Nummerierungsstil von Fußnoten-/Endnotenverweiszeichen geändert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fußnoten und Endnoten sind eine Möglichkeit, einen Verweis oder einen Randkommentar an den Text anzuhängen
    // das den Textfluss des Hauptteils nicht beeinträchtigt.
// Das Einfügen einer Fußnote/Endnote fügt ein kleines hochgestelltes Referenzsymbol hinzu
// im Haupttext, wo wir die Fußnote/Endnote einfügen.
// Jede Fußnote/Endnote erzeugt ebenfalls einen Eintrag, der aus einem Symbol besteht, das mit der Referenz übereinstimmt
// Symbol im Haupttext. Der Referenztext, den wir an die Methode „InsertEndnote“ des Dokumentgenerators übergeben.
// Fußnoteneinträge erscheinen standardmäßig am Ende jeder Seite, die Folgendes enthält:
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

// Standardmäßig ist das Referenzsymbol für jede Fußnote und Endnote der Index
// unter allen Fußnoten/Endnoten des Dokuments. Jedes Dokument verwaltet separate Zählungen
// für Fußnoten und Endnoten. Standardmäßig werden Fußnoten mit arabischen Ziffern nummeriert,
// und Endnoten zeigen ihre Nummern in römischen Kleinbuchstaben an.
Assert.AreEqual(NumberStyle.Arabic, doc.FootnoteOptions.NumberStyle);
Assert.AreEqual(NumberStyle.LowercaseRoman, doc.EndnoteOptions.NumberStyle);

// Wir können die Eigenschaft „NumberStyle“ verwenden, um benutzerdefinierte Nummerierungsstile auf Fußnoten und Endnoten anzuwenden.
// Fußnoten/Endnoten mit benutzerdefinierten Referenzzeichen sind hiervon nicht betroffen.
doc.FootnoteOptions.NumberStyle = NumberStyle.UppercaseRoman;
doc.EndnoteOptions.NumberStyle = NumberStyle.UppercaseLetter;

doc.Save(ArtifactsDir + "InlineStory.RefMarkNumberStyle.docx");
```

### Siehe auch

* enum [NumberStyle](../../../aspose.words/numberstyle/)
* class [EndnoteOptions](../)
* namensraum [Aspose.Words.Notes](../../../aspose.words.notes/)
* Montage [Aspose.Words](../../../)
