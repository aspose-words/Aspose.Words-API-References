---
title: FieldCitation.FormatLanguageId
linktitle: FormatLanguageId
articleTitle: FormatLanguageId
second_title: Aspose.Words per .NET
description: FieldCitation FormatLanguageId proprietà. Ottiene o imposta lID della lingua utilizzato insieme allo stile bibliografico specificato per formattare la citazione nel documento in C#.
type: docs
weight: 30
url: /it/net/aspose.words.fields/fieldcitation/formatlanguageid/
---
## FieldCitation.FormatLanguageId property

Ottiene o imposta l'ID della lingua utilizzato insieme allo stile bibliografico specificato per formattare la citazione nel documento.

```csharp
public string FormatLanguageId { get; set; }
```

## Esempi

Mostra come lavorare con i campi CITAZIONE e BIBLIOGRAFIA.

```csharp
// Apre un documento contenente fonti bibliografiche che possiamo trovare in
// Microsoft Word tramite riferimenti -> Citazioni e citazioni Bibliografia -> Gestisci fonti.
Document doc = new Document(MyDir + "Bibliography.docx");
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Text to be cited with one source.");

// Crea una citazione con solo il numero di pagina e l'autore del libro di riferimento.
FieldCitation fieldCitation = (FieldCitation)builder.InsertField(FieldType.FieldCitation, true);

// Facciamo riferimento alle fonti utilizzando i nomi dei tag.
fieldCitation.SourceTag = "Book1";
fieldCitation.PageNumber = "85";
fieldCitation.SuppressAuthor = false;
fieldCitation.SuppressTitle = true;
fieldCitation.SuppressYear = true;

Assert.AreEqual(" CITATION  Book1 \\p 85 \\t \\y", fieldCitation.GetFieldCode());

// Crea una citazione più dettagliata che citi due fonti.
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

// Possiamo utilizzare un campo BIBLIOGRAFIA per visualizzare tutte le fonti all'interno del documento.
builder.InsertBreak(BreakType.PageBreak);
FieldBibliography fieldBibliography = (FieldBibliography)builder.InsertField(FieldType.FieldBibliography, true);
fieldBibliography.FormatLanguageId = "5129";

Assert.AreEqual(" BIBLIOGRAPHY  \\l 5129", fieldBibliography.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.CITATION.docx");
```

### Guarda anche

* class [FieldCitation](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
