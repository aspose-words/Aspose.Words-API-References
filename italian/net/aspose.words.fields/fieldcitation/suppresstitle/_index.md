---
title: FieldCitation.SuppressTitle
linktitle: SuppressTitle
articleTitle: SuppressTitle
second_title: Aspose.Words per .NET
description: Controlla la visibilità del titolo nelle citazioni con la proprietà FieldCitation SuppressTitle. Gestisci facilmente la visualizzazione delle informazioni per una chiarezza ottimale.
type: docs
weight: 90
url: /it/net/aspose.words.fields/fieldcitation/suppresstitle/
---
## FieldCitation.SuppressTitle property

Ottiene o imposta se le informazioni sul titolo vengono soppresse dalla citazione.

```csharp
public bool SuppressTitle { get; set; }
```

## Esempi

Mostra come lavorare con i campi CITAZIONE e BIBLIOGRAFIA.

```csharp
// Apri un documento contenente fonti bibliografiche che possiamo trovare in
// Microsoft Word tramite Riferimenti -> Citazioni e bibliografia -> Gestisci fonti.
Document doc = new Document(MyDir + "Bibliography.docx");
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Text to be cited with one source.");

// Crea una citazione solo con il numero di pagina e l'autore del libro a cui si fa riferimento.
FieldCitation fieldCitation = (FieldCitation)builder.InsertField(FieldType.FieldCitation, true);

// Facciamo riferimento alle fonti utilizzando i nomi dei loro tag.
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

// Possiamo utilizzare un campo BIBLIOGRAFIA per visualizzare tutte le fonti presenti nel documento.
builder.InsertBreak(BreakType.PageBreak);
FieldBibliography fieldBibliography = (FieldBibliography)builder.InsertField(FieldType.FieldBibliography, true);
fieldBibliography.FormatLanguageId = "5129";
fieldBibliography.FilterLanguageId = "5129";
fieldBibliography.SourceTag = "Book2";

Assert.AreEqual(" BIBLIOGRAPHY  \\l 5129 \\f 5129 \\m Book2", fieldBibliography.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.CITATION.docx");
```

### Guarda anche

* class [FieldCitation](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
