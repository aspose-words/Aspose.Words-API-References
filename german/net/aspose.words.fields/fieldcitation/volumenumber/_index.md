---
title: FieldCitation.VolumeNumber
linktitle: VolumeNumber
articleTitle: VolumeNumber
second_title: Aspose.Words für .NET
description: Verwalten Sie Ihre Zitate mühelos mit der Eigenschaft „FieldCitation VolumeNumber“, mit der Sie zugehörige Bandnummern einfach festlegen oder abrufen können.
type: docs
weight: 110
url: /de/net/aspose.words.fields/fieldcitation/volumenumber/
---
## FieldCitation.VolumeNumber property

Ruft eine mit dem Zitat verknüpfte Bandnummer ab oder legt sie fest.

```csharp
public string VolumeNumber { get; set; }
```

## Beispiele

Zeigt, wie mit den Feldern CITATION und BIBLIOGRAPHY gearbeitet wird.

```csharp
// Öffnen Sie ein Dokument mit bibliographischen Quellen, die wir finden können in
// Microsoft Word über Verweise -> Zitate & Bibliografie -> Quellen verwalten.
Document doc = new Document(MyDir + "Bibliography.docx");
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Text to be cited with one source.");

// Erstellen Sie ein Zitat nur mit der Seitenzahl und dem Autor des referenzierten Buches.
FieldCitation fieldCitation = (FieldCitation)builder.InsertField(FieldType.FieldCitation, true);

// Wir verweisen auf Quellen anhand ihrer Tag-Namen.
fieldCitation.SourceTag = "Book1";
fieldCitation.PageNumber = "85";
fieldCitation.SuppressAuthor = false;
fieldCitation.SuppressTitle = true;
fieldCitation.SuppressYear = true;

Assert.AreEqual(" CITATION  Book1 \\p 85 \\t \\y", fieldCitation.GetFieldCode());

// Erstellen Sie ein ausführlicheres Zitat, das zwei Quellen zitiert.
builder.InsertParagraph();
builder.Write("Text to be cited with two sources.");
fieldCitation = (FieldCitation)builder.InsertField(FieldType.FieldCitation, true);
fieldCitation.SourceTag = "Book1";
fieldCitation.AnotherSourceTag = "Book2";
fieldCitation.FormatLanguageId = "en-US";
fieldCitation.PageNumber = "19";
fieldCitation.Prefix = "Prefix ";
fieldCitation.Suffix = " Suffix";
fieldCitation.SuppressAuthor = false;
fieldCitation.SuppressTitle = false;
fieldCitation.SuppressYear = false;
fieldCitation.VolumeNumber = "VII";

Assert.AreEqual(" CITATION  Book1 \\m Book2 \\l en-US \\p 19 \\f \"Prefix \" \\s \" Suffix\" \\v VII", fieldCitation.GetFieldCode());

// Wir können ein BIBLIOGRAPHY-Feld verwenden, um alle Quellen im Dokument anzuzeigen.
builder.InsertBreak(BreakType.PageBreak);
FieldBibliography fieldBibliography = (FieldBibliography)builder.InsertField(FieldType.FieldBibliography, true);
fieldBibliography.FormatLanguageId = "5129";
fieldBibliography.FilterLanguageId = "5129";
fieldBibliography.SourceTag = "Book2";

Assert.AreEqual(" BIBLIOGRAPHY  \\l 5129 \\f 5129 \\m Book2", fieldBibliography.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.CITATION.docx");
```

### Siehe auch

* class [FieldCitation](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
