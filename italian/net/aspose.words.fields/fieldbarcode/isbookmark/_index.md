---
title: FieldBarcode.IsBookmark
second_title: Aspose.Words per .NET API Reference
description: FieldBarcode proprietà. Ottiene o imposta sePostalAddress è il nome di un segnalibro.
type: docs
weight: 30
url: /it/net/aspose.words.fields/fieldbarcode/isbookmark/
---
## FieldBarcode.IsBookmark property

Ottiene o imposta se[`PostalAddress`](../postaladdress/) è il nome di un segnalibro.

```csharp
public bool IsBookmark { get; set; }
```

### Esempi

Mostra come utilizzare il campo BARCODE per visualizzare i codici postali statunitensi sotto forma di codice a barre.

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

// 2 - Fa riferimento a un segnalibro che memorizza il valore che verrà visualizzato da questo codice a barre:
field = (FieldBarcode)builder.InsertField(FieldType.FieldBarcode, true);
field.PostalAddress = "BarcodeBookmark";
field.IsBookmark = true;

Assert.AreEqual(" BARCODE  BarcodeBookmark \\b", field.GetFieldCode());

// Il segnalibro a cui fa riferimento il campo BARCODE nella relativa proprietà PostalAddress
// non deve contenere nulla oltre al codice postale valido.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("BarcodeBookmark");
builder.Writeln("968877");
builder.EndBookmark("BarcodeBookmark");

doc.Save(ArtifactsDir + "Field.BARCODE.docx");
```

### Guarda anche

* class [FieldBarcode](../)
* spazio dei nomi [Aspose.Words.Fields](../../fieldbarcode/)
* assemblea [Aspose.Words](../../../)


