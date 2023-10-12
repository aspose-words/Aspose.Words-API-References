---
title: Interface IBarcodeGenerator
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Fields.IBarcodeGenerator interfaccia. Interfaccia pubblica per generatore personalizzato di codici a barre. Limplementazione dovrebbe essere fornita dallutente.
type: docs
weight: 2660
url: /it/net/aspose.words.fields/ibarcodegenerator/
---
## IBarcodeGenerator interface

Interfaccia pubblica per generatore personalizzato di codici a barre. L'implementazione dovrebbe essere fornita dall'utente.

```csharp
public interface IBarcodeGenerator
```

## Metodi

| Nome | Descrizione |
| --- | --- |
| [GetBarcodeImage](../../aspose.words.fields/ibarcodegenerator/getbarcodeimage/)(BarcodeParameters) | Genera l'immagine del codice a barre utilizzando il set di parametri (per il campo DisplayBarcode). |
| [GetOldBarcodeImage](../../aspose.words.fields/ibarcodegenerator/getoldbarcodeimage/)(BarcodeParameters) | Genera l'immagine del codice a barre utilizzando il set di parametri (per il campo Codice a barre vecchio stile). |

### Osservazioni

L'istanza del generatore deve essere passata attraverso il file[`BarcodeGenerator`](../fieldoptions/barcodegenerator/) proprietà.

### Esempi

Mostra come utilizzare un generatore di codici a barre.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Possiamo utilizzare un'implementazione IBarcodeGenerator personalizzata per generare codici a barre,
// e poi inserirli nel documento come immagini.
doc.FieldOptions.BarcodeGenerator = new CustomBarcodeGenerator();

// Di seguito sono riportati quattro esempi di diversi tipi di codici a barre che possiamo creare utilizzando il nostro generatore.
// Per ciascun codice a barre, specifichiamo un nuovo set di parametri del codice a barre, quindi generiamo l'immagine.
// Successivamente possiamo inserire l'immagine nel documento o salvarla nel file system locale.
// 1 - Codice QR:
BarcodeParameters barcodeParameters = new BarcodeParameters
{
    BarcodeType = "QR",
    BarcodeValue = "ABC123",
    BackgroundColor = "0xF8BD69",
    ForegroundColor = "0xB5413B",
    ErrorCorrectionLevel = "3",
    ScalingFactor = "250",
    SymbolHeight = "1000",
    SymbolRotation = "0"
};

Image img = doc.FieldOptions.BarcodeGenerator.GetBarcodeImage(barcodeParameters);
img.Save(ArtifactsDir + "FieldOptions.BarcodeGenerator.QR.jpg");

builder.InsertImage(img);

// 2 - Codice a barre EAN13:
barcodeParameters = new BarcodeParameters
{
    BarcodeType = "EAN13",
    BarcodeValue = "501234567890",
    DisplayText = true,
    PosCodeStyle = "CASE",
    FixCheckDigit = true
};

img = doc.FieldOptions.BarcodeGenerator.GetBarcodeImage(barcodeParameters);
img.Save(ArtifactsDir + "FieldOptions.BarcodeGenerator.EAN13.jpg");
builder.InsertImage(img);

// 3 - Codice a barre CODE39:
barcodeParameters = new BarcodeParameters
{
    BarcodeType = "CODE39",
    BarcodeValue = "12345ABCDE",
    AddStartStopChar = true
};

img = doc.FieldOptions.BarcodeGenerator.GetBarcodeImage(barcodeParameters);
img.Save(ArtifactsDir + "FieldOptions.BarcodeGenerator.CODE39.jpg");
builder.InsertImage(img);

// 4 - Codice a barre ITF14:
barcodeParameters = new BarcodeParameters
{
    BarcodeType = "ITF14",
    BarcodeValue = "09312345678907",
    CaseCodeStyle = "STD"
};

img = doc.FieldOptions.BarcodeGenerator.GetBarcodeImage(barcodeParameters);
img.Save(ArtifactsDir + "FieldOptions.BarcodeGenerator.ITF14.jpg");
builder.InsertImage(img);

doc.Save(ArtifactsDir + "FieldOptions.BarcodeGenerator.docx");
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Fields](../../aspose.words.fields/)
* assemblea [Aspose.Words](../../)


