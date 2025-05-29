---
title: BarcodeParameters.PosCodeStyle
linktitle: PosCodeStyle
articleTitle: PosCodeStyle
second_title: Aspose.Words per .NET
description: Scopri la proprietà PosCodeStyle di BarcodeParameters per i codici a barre dei punti vendita. Supporta UPCA, EAN13 e altri. Migliora il tuo sistema POS oggi stesso!
type: docs
weight: 140
url: /it/net/aspose.words.fields/barcodeparameters/poscodestyle/
---
## BarcodeParameters.PosCodeStyle property

Stile di un codice a barre per punto vendita (tipi di codice a barre UPCA&#x7C;UPCE&#x7C;EAN13&#x7C;EAN8). I valori validi (senza distinzione tra maiuscole e minuscole) sono [STD&#x7C;SUP2&#x7C;SUP5&#x7C;CASE].

```csharp
public string PosCodeStyle { get; set; }
```

## Esempi

Mostra come utilizzare un generatore di codici a barre.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Possiamo utilizzare un'implementazione personalizzata di IBarcodeGenerator per generare codici a barre,
// e poi inserirli nel documento come immagini.
doc.FieldOptions.BarcodeGenerator = new CustomBarcodeGenerator();

// Di seguito sono riportati quattro esempi di diversi tipi di codici a barre che possiamo creare utilizzando il nostro generatore.
// Per ogni codice a barre, specifichiamo un nuovo set di parametri del codice a barre e poi generiamo l'immagine.
// Successivamente possiamo inserire l'immagine nel documento oppure salvarla nel file system locale.
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
#if NET461_OR_GREATER || JAVA
img.Save(ArtifactsDir + "FieldOptions.BarcodeGenerator.QR.jpg");
#elif NET5_0_OR_GREATER
using (SKFileWStream fs = new SKFileWStream(ArtifactsDir + "FieldOptions.BarcodeGenerator.QR.jpg"))
{
    img.Encode(fs, SKEncodedImageFormat.Jpeg, 100);
}
#endif
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
#if NET461_OR_GREATER || JAVA
img.Save(ArtifactsDir + "FieldOptions.BarcodeGenerator.EAN13.jpg");
#elif NET5_0_OR_GREATER
using (SKFileWStream fs = new SKFileWStream(ArtifactsDir + "FieldOptions.BarcodeGenerator.EAN13.jpg"))
{
    img.Encode(fs, SKEncodedImageFormat.Jpeg, 100);
}
#endif
builder.InsertImage(img);

// 3 - Codice a barre CODE39:
barcodeParameters = new BarcodeParameters
{
    BarcodeType = "CODE39",
    BarcodeValue = "12345ABCDE",
    AddStartStopChar = true
};

img = doc.FieldOptions.BarcodeGenerator.GetBarcodeImage(barcodeParameters);
#if NET461_OR_GREATER || JAVA
img.Save(ArtifactsDir + "FieldOptions.BarcodeGenerator.CODE39.jpg");
#elif NET5_0_OR_GREATER
using (SKFileWStream fs = new SKFileWStream(ArtifactsDir + "FieldOptions.BarcodeGenerator.CODE39.jpg"))
{
    img.Encode(fs, SKEncodedImageFormat.Jpeg, 100);
}
#endif
builder.InsertImage(img);

// 4 - Codice a barre ITF14:
barcodeParameters = new BarcodeParameters
{
    BarcodeType = "ITF14",
    BarcodeValue = "09312345678907",
    CaseCodeStyle = "STD"
};

img = doc.FieldOptions.BarcodeGenerator.GetBarcodeImage(barcodeParameters);
#if NET461_OR_GREATER || JAVA
img.Save(ArtifactsDir + "FieldOptions.BarcodeGenerator.ITF14.jpg");
#elif NET5_0_OR_GREATER
using (SKFileWStream fs = new SKFileWStream(ArtifactsDir + "FieldOptions.BarcodeGenerator.ITF14.jpg"))
{
    img.Encode(fs, SKEncodedImageFormat.Jpeg, 100);
}
#endif
builder.InsertImage(img);

doc.Save(ArtifactsDir + "FieldOptions.BarcodeGenerator.docx");
```

### Guarda anche

* class [BarcodeParameters](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
