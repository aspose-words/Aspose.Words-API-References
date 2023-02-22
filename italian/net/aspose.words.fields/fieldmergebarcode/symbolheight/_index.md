---
title: FieldMergeBarcode.SymbolHeight
second_title: Aspose.Words per .NET API Reference
description: FieldMergeBarcode proprietà. Ottiene o imposta laltezza del simbolo. Le unità sono in TWIPS 1/1440 di pollice.
type: docs
weight: 130
url: /it/net/aspose.words.fields/fieldmergebarcode/symbolheight/
---
## FieldMergeBarcode.SymbolHeight property

Ottiene o imposta l'altezza del simbolo. Le unità sono in TWIPS (1/1440 di pollice).

```csharp
public string SymbolHeight { get; set; }
```

### Esempi

Mostra come eseguire una stampa unione sui codici a barre QR.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisce un campo MERGEBARCCODE, che accetterà i valori da un'origine dati durante una stampa unione.
// Questo campo converte tutti i valori nella colonna "MyQRCode" di un'origine dati di unione in codici QR.
FieldMergeBarcode field = (FieldMergeBarcode)builder.InsertField(FieldType.FieldMergeBarcode, true);
field.BarcodeType = "QR";
field.BarcodeValue = "MyQRCode";

// Applica colori e ridimensionamenti personalizzati.
field.BackgroundColor = "0xF8BD69";
field.ForegroundColor = "0xB5413B";
field.ErrorCorrectionLevel = "3";
field.ScalingFactor = "250";
field.SymbolHeight = "1000";
field.SymbolRotation = "0";

Assert.AreEqual(FieldType.FieldMergeBarcode, field.Type);
Assert.AreEqual(" MERGEBARCODE  MyQRCode QR \\b 0xF8BD69 \\f 0xB5413B \\q 3 \\s 250 \\h 1000 \\r 0",
    field.GetFieldCode());
builder.Writeln();

// Crea una DataTable con una colonna con lo stesso nome del nostro campo MERGEBARCODE BarcodeValue.
// La stampa unione creerà una nuova pagina per ogni riga. Ogni pagina conterrà un campo DISPLAYBARCCODE,
// che visualizzerà un codice QR con il valore della riga unita.
DataTable table = new DataTable("Barcodes");
table.Columns.Add("MyQRCode");
table.Rows.Add(new[] { "ABC123" });
table.Rows.Add(new[] { "DEF456" });

doc.MailMerge.Execute(table);

Assert.AreEqual(FieldType.FieldDisplayBarcode, doc.Range.Fields[0].Type);
Assert.AreEqual("DISPLAYBARCODE \"ABC123\" QR \\q 3 \\s 250 \\h 1000 \\r 0 \\b 0xF8BD69 \\f 0xB5413B", 
    doc.Range.Fields[0].GetFieldCode());
Assert.AreEqual(FieldType.FieldDisplayBarcode, doc.Range.Fields[1].Type);
Assert.AreEqual("DISPLAYBARCODE \"DEF456\" QR \\q 3 \\s 250 \\h 1000 \\r 0 \\b 0xF8BD69 \\f 0xB5413B",
    doc.Range.Fields[1].GetFieldCode());

doc.Save(ArtifactsDir + "Field.MERGEBARCODE.QR.docx");
```

### Guarda anche

* class [FieldMergeBarcode](../)
* spazio dei nomi [Aspose.Words.Fields](../../fieldmergebarcode/)
* assemblea [Aspose.Words](../../../)


