---
title: Interface IBarcodeGenerator
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Fields.IBarcodeGenerator koppel. Öffentliche Schnittstelle für den benutzerdefinierten BarcodeGenerator. Die Implementierung sollte vom Benutzer bereitgestellt werden.
type: docs
weight: 2660
url: /de/net/aspose.words.fields/ibarcodegenerator/
---
## IBarcodeGenerator interface

Öffentliche Schnittstelle für den benutzerdefinierten Barcode-Generator. Die Implementierung sollte vom Benutzer bereitgestellt werden.

```csharp
public interface IBarcodeGenerator
```

## Methoden

| Name | Beschreibung |
| --- | --- |
| [GetBarcodeImage](../../aspose.words.fields/ibarcodegenerator/getbarcodeimage/)(BarcodeParameters) | Erzeugen Sie ein Barcode-Bild mithilfe des Parametersatzes (für das DisplayBarcode-Feld). |
| [GetOldBarcodeImage](../../aspose.words.fields/ibarcodegenerator/getoldbarcodeimage/)(BarcodeParameters) | Erzeugen Sie ein Barcode-Bild mithilfe des Parametersatzes (für das altmodische Barcode-Feld). |

### Bemerkungen

Generatorinstanz sollte durch die geleitet werden[`BarcodeGenerator`](../fieldoptions/barcodegenerator/) Eigenschaft.

### Beispiele

Zeigt, wie ein Barcode-Generator verwendet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Wir können eine benutzerdefinierte IBarcodeGenerator-Implementierung verwenden, um Barcodes zu generieren.
// und fügen Sie sie dann als Bilder in das Dokument ein.
doc.FieldOptions.BarcodeGenerator = new CustomBarcodeGenerator();

// Nachfolgend finden Sie vier Beispiele für verschiedene Barcode-Typen, die wir mit unserem Generator erstellen können.
// Für jeden Barcode geben wir einen neuen Satz Barcode-Parameter an und generieren dann das Bild.
// Anschließend können wir das Bild in das Dokument einfügen oder im lokalen Dateisystem speichern.
// 1 - QR-Code:
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

// 2 - EAN13-Barcode:
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

// 3 - CODE39-Barcode:
barcodeParameters = new BarcodeParameters
{
    BarcodeType = "CODE39",
    BarcodeValue = "12345ABCDE",
    AddStartStopChar = true
};

img = doc.FieldOptions.BarcodeGenerator.GetBarcodeImage(barcodeParameters);
img.Save(ArtifactsDir + "FieldOptions.BarcodeGenerator.CODE39.jpg");
builder.InsertImage(img);

// 4 - ITF14-Barcode:
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

### Siehe auch

* namensraum [Aspose.Words.Fields](../../aspose.words.fields/)
* Montage [Aspose.Words](../../)


