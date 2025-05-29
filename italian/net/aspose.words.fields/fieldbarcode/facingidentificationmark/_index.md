---
title: FieldBarcode.FacingIdentificationMark
linktitle: FacingIdentificationMark
articleTitle: FacingIdentificationMark
second_title: Aspose.Words per .NET
description: Scopri la proprietà FieldBarcode FacingIdentificationMark per gestire e personalizzare facilmente i Facing Identification Marks (FIM) per una maggiore efficienza di scansione.
type: docs
weight: 20
url: /it/net/aspose.words.fields/fieldbarcode/facingidentificationmark/
---
## FieldBarcode.FacingIdentificationMark property

Ottiene o imposta il tipo di un Facing Identification Mark (FIM) da inserire.

```csharp
public string FacingIdentificationMark { get; set; }
```

## Esempi

Mostra come utilizzare il campo CODICE A BARRE per visualizzare i codici postali degli Stati Uniti sotto forma di codice a barre.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln();

// Di seguito sono riportati due modi per utilizzare i campi BARCODE per visualizzare valori personalizzati come codici a barre.
// 1 - Memorizza il valore che il codice a barre visualizzerà nella proprietà PostalAddress:
FieldBarcode field = (FieldBarcode)builder.InsertField(FieldType.FieldBarcode, true);

// Questo valore deve essere un codice postale valido.
field.PostalAddress = "96801";
field.IsUSPostalAddress = true;
field.FacingIdentificationMark = "C";

Assert.AreEqual(" BARCODE  96801 \\u \\f C", field.GetFieldCode());

builder.InsertBreak(BreakType.LineBreak);

// 2 - Riferimento a un segnalibro che memorizza il valore che verrà visualizzato da questo codice a barre:
field = (FieldBarcode)builder.InsertField(FieldType.FieldBarcode, true);
field.PostalAddress = "BarcodeBookmark";
field.IsBookmark = true;

Assert.AreEqual(" BARCODE  BarcodeBookmark \\b", field.GetFieldCode());

// Il segnalibro a cui fa riferimento il campo BARCODE nella sua proprietà PostalAddress
// non deve contenere altro oltre al codice postale valido.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("BarcodeBookmark");
builder.Writeln("968877");
builder.EndBookmark("BarcodeBookmark");

doc.Save(ArtifactsDir + "Field.BARCODE.docx");
```

### Guarda anche

* class [FieldBarcode](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
