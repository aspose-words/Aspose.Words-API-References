---
title: BarcodeParameters
second_title: Aspose.Words per .NET API Reference
description: Classe contenitore per parametri codici a barre da trasmettere a BarcodeGenerator.
type: docs
weight: 1320
url: /it/net/aspose.words.fields/barcodeparameters/
---
## BarcodeParameters class

Classe contenitore per parametri codici a barre da trasmettere a BarcodeGenerator.

```csharp
public class BarcodeParameters
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [BarcodeParameters](barcodeparameters/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [AddStartStopChar](../../aspose.words.fields/barcodeparameters/addstartstopchar/) { get; set; } | Se aggiungere i caratteri Start/Stop per i tipi di codici a barre NW7 e CODE39. |
| [BackgroundColor](../../aspose.words.fields/barcodeparameters/backgroundcolor/) { get; set; } | Colore sfondo codice a barre (0x000000 - 0xFFFFFF) |
| [BarcodeType](../../aspose.words.fields/barcodeparameters/barcodetype/) { get; set; } | Tipo di codice a barre. |
| [BarcodeValue](../../aspose.words.fields/barcodeparameters/barcodevalue/) { get; set; } | Dati da codificare. |
| [CaseCodeStyle](../../aspose.words.fields/barcodeparameters/casecodestyle/) { get; set; } | Stile di un codice caso per codice a barre tipo ITF14. I valori validi sono [STD&#x7C;EXT&#x7C;ADD] |
| [DisplayText](../../aspose.words.fields/barcodeparameters/displaytext/) { get; set; } | Indica se visualizzare i dati del codice a barre (testo) insieme all'immagine. |
| [ErrorCorrectionLevel](../../aspose.words.fields/barcodeparameters/errorcorrectionlevel/) { get; set; } | Livello di correzione degli errori del codice QR. I valori validi sono [0, 3]. |
| [FacingIdentificationMark](../../aspose.words.fields/barcodeparameters/facingidentificationmark/) { get; set; } | Tipo di contrassegno di identificazione di fronte (FIM). |
| [FixCheckDigit](../../aspose.words.fields/barcodeparameters/fixcheckdigit/) { get; set; } | Se correggere la cifra di controllo se non è valida. |
| [ForegroundColor](../../aspose.words.fields/barcodeparameters/foregroundcolor/) { get; set; } | Colore di primo piano del codice a barre (0x000000 - 0xFFFFFF) |
| [IsBookmark](../../aspose.words.fields/barcodeparameters/isbookmark/) { get; set; } | Se[`PostalAddress`](./postaladdress/) è il nome di un segnalibro. |
| [IsUSPostalAddress](../../aspose.words.fields/barcodeparameters/isuspostaladdress/) { get; set; } | Se[`PostalAddress`](./postaladdress/) è un indirizzo postale statunitense. |
| [PosCodeStyle](../../aspose.words.fields/barcodeparameters/poscodestyle/) { get; set; } | Stile di un codice a barre del punto vendita (tipi di codici a barre UPCA&#x7C;UPCE&#x7C;EAN13&#x7C;EAN8). I valori validi (senza distinzione tra maiuscole e minuscole) sono [STD&#x7C;SUP2&#x7C;SUP5&#x7C;CASE]. |
| [PostalAddress](../../aspose.words.fields/barcodeparameters/postaladdress/) { get; set; } | Indirizzo postale codice a barre. |
| [ScalingFactor](../../aspose.words.fields/barcodeparameters/scalingfactor/) { get; set; } | Fattore di scala per il simbolo. Il valore è espresso in punti percentuali interi e i valori validi sono [10, 1000]. |
| [SymbolHeight](../../aspose.words.fields/barcodeparameters/symbolheight/) { get; set; } | Altezza immagine codice a barre (in twip - 1/1440 pollici) |
| [SymbolRotation](../../aspose.words.fields/barcodeparameters/symbolrotation/) { get; set; } | Rotazione del simbolo del codice a barre. I valori validi sono [0, 3]. |

### Osservazioni

Il set di parametri è conforme alle opzioni del campo DISPLAYBARCCODE. Vedere l'elenco esatto in[https://msdn.microsoft.com/en-us/library/hh745901(v=office.12).aspx](https://msdn.microsoft.com/en-us/library/hh745901(v=office.12).aspx)

### Esempi

Mostra come utilizzare un generatore di codici a barre.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Possiamo utilizzare un'implementazione IBarcodeGenerator personalizzata per generare codici a barre,
// e quindi inserirli nel documento come immagini.
doc.FieldOptions.BarcodeGenerator = new CustomBarcodeGenerator();

// Di seguito sono riportati quattro esempi di diversi tipi di codici a barre che possiamo creare utilizzando il nostro generatore.
// Per ogni codice a barre, specifichiamo un nuovo set di parametri del codice a barre, quindi generiamo l'immagine.
// Successivamente, possiamo inserire l'immagine nel documento o salvarla nel file system locale.
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

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
