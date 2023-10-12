---
title: FieldBibliography.FormatLanguageId
second_title: Aspose.Words für .NET-API-Referenz
description: FieldBibliography eigendom. Ruft die SprachID ab die zum Formatieren der bibliografischen Quellen im Dokument verwendet wird oder legt diese fest.
type: docs
weight: 30
url: /de/net/aspose.words.fields/fieldbibliography/formatlanguageid/
---
## FieldBibliography.FormatLanguageId property

Ruft die Sprach-ID ab, die zum Formatieren der bibliografischen Quellen im Dokument verwendet wird, oder legt diese fest.

```csharp
public string FormatLanguageId { get; set; }
```

### Beispiele

Zeigt, wie mit den Feldern CITATION und BIBLIOGRAPHY gearbeitet wird.

```csharp
// Öffnen Sie ein Dokument mit bibliografischen Quellen, in denen wir finden können
// Microsoft Word über Referenzen -> Zitate & Bibliographie -> Quellen verwalten.
Document doc = new Document(MyDir + "Bibliography.docx");
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Text to be cited with one source.");

// Erstellen Sie ein Zitat nur mit der Seitenzahl und dem Autor des referenzierten Buches.
FieldCitation fieldCitation = (FieldCitation)builder.InsertField(FieldType.FieldCitation, true);

// Wir verweisen auf Quellen mit ihren Tag-Namen.
fieldCitation.SourceTag = "Book1";
fieldCitation.PageNumber = "85";
fieldCitation.SuppressAuthor = false;
fieldCitation.SuppressTitle = true;
fieldCitation.SuppressYear = true;

Assert.AreEqual(" CITATION  Book1 \\p 85 \\t \\y", fieldCitation.GetFieldCode());

// Erstellen Sie ein detaillierteres Zitat, das zwei Quellen zitiert.
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

Assert.AreEqual(" BIBLIOGRAPHY  \\l 5129", fieldBibliography.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.CITATION.docx");
```

### Siehe auch

* class [FieldBibliography](../)
* namensraum [Aspose.Words.Fields](../../fieldbibliography/)
* Montage [Aspose.Words](../../../)


