---
title: FieldMergeBarcode.CaseCodeStyle
second_title: Aspose.Words per .NET API Reference
description: FieldMergeBarcode proprietà. Ottiene o imposta lo stile di un codice caso per il tipo di codice a barre ITF14. I valori validi sono STDEXTADD
type: docs
weight: 60
url: /it/net/aspose.words.fields/fieldmergebarcode/casecodestyle/
---
## FieldMergeBarcode.CaseCodeStyle property

Ottiene o imposta lo stile di un codice caso per il tipo di codice a barre ITF14. I valori validi sono [STD&#x7C;EXT&#x7C;ADD]

```csharp
public string CaseCodeStyle { get; set; }
```

### Esempi

Mostra come eseguire una stampa unione su codici a barre ITF14.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisce un campo MERGEBARCCODE, che accetterà i valori da un'origine dati durante una stampa unione.
// Questo campo converte tutti i valori nella colonna "MyITF14Barcode" di un'origine dati di unione in codici a barre ITF14.
FieldMergeBarcode field = (FieldMergeBarcode)builder.InsertField(FieldType.FieldMergeBarcode, true);
field.BarcodeType = "ITF14";
field.BarcodeValue = "MyITF14Barcode";
field.CaseCodeStyle = "STD";

Assert.AreEqual(FieldType.FieldMergeBarcode, field.Type);
Assert.AreEqual(" MERGEBARCODE  MyITF14Barcode ITF14 \\c STD", field.GetFieldCode());

// Crea una DataTable con una colonna con lo stesso nome del nostro campo MERGEBARCODE BarcodeValue.
// La stampa unione creerà una nuova pagina per ogni riga. Ogni pagina conterrà un campo DISPLAYBARCCODE,
// che visualizzerà un codice a barre ITF14 con il valore della riga unita.
DataTable table = new DataTable("Barcodes");
table.Columns.Add("MyITF14Barcode");
table.Rows.Add(new[] { "09312345678907" });
table.Rows.Add(new[] { "1234567891234" });

doc.MailMerge.Execute(table);

Assert.AreEqual(FieldType.FieldDisplayBarcode, doc.Range.Fields[0].Type);
Assert.AreEqual("DISPLAYBARCODE \"09312345678907\" ITF14 \\c STD",
    doc.Range.Fields[0].GetFieldCode());
Assert.AreEqual(FieldType.FieldDisplayBarcode, doc.Range.Fields[1].Type);
Assert.AreEqual("DISPLAYBARCODE \"1234567891234\" ITF14 \\c STD",
    doc.Range.Fields[1].GetFieldCode());

doc.Save(ArtifactsDir + "Field.MERGEBARCODE.ITF14.docx");
```

### Guarda anche

* class [FieldMergeBarcode](../)
* spazio dei nomi [Aspose.Words.Fields](../../fieldmergebarcode/)
* assemblea [Aspose.Words](../../../)


