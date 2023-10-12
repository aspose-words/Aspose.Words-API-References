---
title: FieldMergeBarcode.AddStartStopChar
second_title: Aspose.Words per .NET API Reference
description: FieldMergeBarcode proprietà. Ottiene o imposta se aggiungere caratteri di inizio/fine per i tipi di codici a barre NW7 e CODE39.
type: docs
weight: 20
url: /it/net/aspose.words.fields/fieldmergebarcode/addstartstopchar/
---
## FieldMergeBarcode.AddStartStopChar property

Ottiene o imposta se aggiungere caratteri di inizio/fine per i tipi di codici a barre NW7 e CODE39.

```csharp
public bool AddStartStopChar { get; set; }
```

### Esempi

Mostra come eseguire una stampa unione sui codici a barre CODE39.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci un campo MERGEBARCODE, che accetterà valori da un'origine dati durante una stampa unione.
// Questo campo convertirà tutti i valori nella colonna "MyCODE39Barcode" di un'origine dati di unione in codici a barre CODE39.
FieldMergeBarcode field = (FieldMergeBarcode)builder.InsertField(FieldType.FieldMergeBarcode, true);
field.BarcodeType = "CODE39";
field.BarcodeValue = "MyCODE39Barcode";

// Modifica il suo aspetto per visualizzare i caratteri di inizio/fine.
field.AddStartStopChar = true;

Assert.AreEqual(FieldType.FieldMergeBarcode, field.Type);
Assert.AreEqual(" MERGEBARCODE  MyCODE39Barcode CODE39 \\d", field.GetFieldCode());
builder.Writeln();

// Crea una DataTable con una colonna con lo stesso nome del BarcodeValue del nostro campo MERGEBARCODE.
// La stampa unione creerà una nuova pagina per ogni riga. Ogni pagina conterrà un campo DISPLAYBARCODE,
// che visualizzerà un codice a barre CODE39 con il valore della riga unita.
DataTable table = new DataTable("Barcodes");
table.Columns.Add("MyCODE39Barcode");
table.Rows.Add(new[] { "12345ABCDE" });
table.Rows.Add(new[] { "67890FGHIJ" });

doc.MailMerge.Execute(table);

Assert.AreEqual(FieldType.FieldDisplayBarcode, doc.Range.Fields[0].Type);
Assert.AreEqual("DISPLAYBARCODE \"12345ABCDE\" CODE39 \\d",
    doc.Range.Fields[0].GetFieldCode());
Assert.AreEqual(FieldType.FieldDisplayBarcode, doc.Range.Fields[1].Type);
Assert.AreEqual("DISPLAYBARCODE \"67890FGHIJ\" CODE39 \\d",
    doc.Range.Fields[1].GetFieldCode());

doc.Save(ArtifactsDir + "Field.MERGEBARCODE.CODE39.docx");
```

### Guarda anche

* class [FieldMergeBarcode](../)
* spazio dei nomi [Aspose.Words.Fields](../../fieldmergebarcode/)
* assemblea [Aspose.Words](../../../)


