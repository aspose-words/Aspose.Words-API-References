---
title: FieldMergeBarcode.PosCodeStyle
linktitle: PosCodeStyle
articleTitle: PosCodeStyle
second_title: Aspose.Words per .NET
description: Scopri la proprietà FieldMergeBarcode PosCodeStyle per codici a barre POS personalizzabili. Supporto per UPCA, EAN13 e altro ancora con opzioni di stile flessibili!
type: docs
weight: 110
url: /it/net/aspose.words.fields/fieldmergebarcode/poscodestyle/
---
## FieldMergeBarcode.PosCodeStyle property

Ottiene o imposta lo stile di un codice a barre del punto vendita (tipi di codice a barre UPCA&#x7C;UPCE&#x7C;EAN13&#x7C;EAN8). I valori validi (senza distinzione tra maiuscole e minuscole) sono [STD&#x7C;SUP2&#x7C;SUP5&#x7C;CASE].

```csharp
public string PosCodeStyle { get; set; }
```

## Esempi

Mostra come eseguire una stampa unione su codici a barre EAN13.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserire un campo MERGEBARCODE, che accetterà valori da un'origine dati durante una stampa unione.
// Questo campo convertirà tutti i valori nella colonna "MyEAN13Barcode" di una sorgente dati di unione in codici a barre EAN13.
FieldMergeBarcode field = (FieldMergeBarcode)builder.InsertField(FieldType.FieldMergeBarcode, true);
field.BarcodeType = "EAN13";
field.BarcodeValue = "MyEAN13Barcode";

// Visualizza il valore numerico del codice a barre sotto le barre.
field.DisplayText = true;
field.PosCodeStyle = "CASE";
field.FixCheckDigit = true;

Assert.AreEqual(FieldType.FieldMergeBarcode, field.Type);
Assert.AreEqual(" MERGEBARCODE  MyEAN13Barcode EAN13 \\t \\p CASE \\x", field.GetFieldCode());
builder.Writeln();

// Crea un DataTable con una colonna con lo stesso nome del BarcodeValue del nostro campo MERGEBARCODE.
// La stampa unione creerà una nuova pagina per ogni riga. Ogni pagina conterrà un campo DISPLAYBARCODE,
// che visualizzerà un codice a barre EAN13 con il valore della riga unita.
DataTable table = new DataTable("Barcodes");
table.Columns.Add("MyEAN13Barcode");
table.Rows.Add(new[] { "501234567890" });
table.Rows.Add(new[] { "123456789012" });

doc.MailMerge.Execute(table);

Assert.AreEqual(FieldType.FieldDisplayBarcode, doc.Range.Fields[0].Type);
Assert.AreEqual("DISPLAYBARCODE \"501234567890\" EAN13 \\t \\p CASE \\x",
    doc.Range.Fields[0].GetFieldCode());
Assert.AreEqual(FieldType.FieldDisplayBarcode, doc.Range.Fields[1].Type);
Assert.AreEqual("DISPLAYBARCODE \"123456789012\" EAN13 \\t \\p CASE \\x",
    doc.Range.Fields[1].GetFieldCode());

doc.Save(ArtifactsDir + "Field.MERGEBARCODE.EAN13.docx");
```

### Guarda anche

* class [FieldMergeBarcode](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
