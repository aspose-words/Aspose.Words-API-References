---
title: FieldCitation.SuppressAuthor
second_title: Aspose.Words für .NET-API-Referenz
description: FieldCitation eigendom. Ruft ab oder legt fest ob die Autoreninformationen aus dem Zitat unterdrückt werden.
type: docs
weight: 80
url: /de/net/aspose.words.fields/fieldcitation/suppressauthor/
---
## FieldCitation.SuppressAuthor property

Ruft ab oder legt fest, ob die Autoreninformationen aus dem Zitat unterdrückt werden.

```csharp
public bool SuppressAuthor { get; set; }
```

### Beispiele

Zeigt, wie mit den Feldern CITATION und BIBLIOGRAPHY gearbeitet wird.

```csharp
// Öffnen Sie ein Dokument mit bibliografischen Quellen, die wir finden können
// Microsoft Word über Referenzen -> Zitate & Bibliographie -> Quellen verwalten.
Document doc = new Document(MyDir + "Bibliography.docx");
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Text to be cited with one source.");

// Erstellen Sie ein Zitat nur mit der Seitenzahl und dem Autor des Buches, auf das verwiesen wird.
FieldCitation fieldCitation = (FieldCitation)builder.InsertField(FieldType.FieldCitation, true);

// Wir verweisen auf Quellen mit ihren Tag-Namen.
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

// Wir können ein BIBLIOGRAPHY-Feld verwenden, um alle Quellen innerhalb des Dokuments anzuzeigen.
builder.InsertBreak(BreakType.PageBreak);
FieldBibliography fieldBibliography = (FieldBibliography)builder.InsertField(FieldType.FieldBibliography, true);
fieldBibliography.FormatLanguageId = "1124";

Assert.AreEqual(" BIBLIOGRAPHY  \\l 1124", fieldBibliography.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.CITATION.docx");
```

### Siehe auch

* class [FieldCitation](../)
* namensraum [Aspose.Words.Fields](../../fieldcitation/)
* Montage [Aspose.Words](../../../)


