---
title: IBarcodeGenerator Interface
linktitle: IBarcodeGenerator
articleTitle: IBarcodeGenerator
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aspose.Words.Fields.IBarcodeGenerator-Schnittstelle zur benutzerdefinierten Barcode-Generierung. Optimieren Sie Ihre Projekte mit benutzerdefinierten Implementierungen und erweitern Sie die Funktionalität!
type: docs
weight: 3070
url: /de/net/aspose.words.fields/ibarcodegenerator/
---
## IBarcodeGenerator interface

Öffentliche Schnittstelle für benutzerdefinierten Barcode-Generator. Die Implementierung muss vom Benutzer bereitgestellt werden.

```csharp
public interface IBarcodeGenerator
```

## Methoden

| Name | Beschreibung |
| --- | --- |
| [GetBarcodeImage](../../aspose.words.fields/ibarcodegenerator/getbarcodeimage/)(*[BarcodeParameters](../barcodeparameters/)*) | Barcodebild mit dem Parametersatz generieren (für das Feld „DisplayBarcode“). |
| [GetOldBarcodeImage](../../aspose.words.fields/ibarcodegenerator/getoldbarcodeimage/)(*[BarcodeParameters](../barcodeparameters/)*) | Barcode-Bild mit dem Parametersatz generieren (für altmodisches Barcode-Feld). |

## Bemerkungen

Generatorinstanz sollte durch die[`BarcodeGenerator`](../fieldoptions/barcodegenerator/) Eigenschaft.

## Beispiele

Zeigt, wie ein Barcode-Generator verwendet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Wir können eine benutzerdefinierte IBarcodeGenerator-Implementierung verwenden, um Barcodes zu generieren,
// und fügen Sie sie dann als Bilder in das Dokument ein.
doc.FieldOptions.BarcodeGenerator = new CustomBarcodeGenerator();

// Unten sind vier Beispiele für verschiedene Barcodetypen, die wir mit unserem Generator erstellen können.
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
#if NET461_OR_GREATER || JAVA
img.Save(ArtifactsDir + "FieldOptions.BarcodeGenerator.QR.jpg");
#elif NET5_0_OR_GREATER
using (SKFileWStream fs = new SKFileWStream(ArtifactsDir + "FieldOptions.BarcodeGenerator.QR.jpg"))
{
    img.Encode(fs, SKEncodedImageFormat.Jpeg, 100);
}
#endif
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
#if NET461_OR_GREATER || JAVA
img.Save(ArtifactsDir + "FieldOptions.BarcodeGenerator.EAN13.jpg");
#elif NET5_0_OR_GREATER
using (SKFileWStream fs = new SKFileWStream(ArtifactsDir + "FieldOptions.BarcodeGenerator.EAN13.jpg"))
{
    img.Encode(fs, SKEncodedImageFormat.Jpeg, 100);
}
#endif
builder.InsertImage(img);

// 3 - CODE39-Barcode:
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

// 4 - ITF14-Barcode:
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

### Siehe auch

* namensraum [Aspose.Words.Fields](../../aspose.words.fields/)
* Montage [Aspose.Words](../../)
