---
title: BarcodeParameters Class
linktitle: BarcodeParameters
articleTitle: BarcodeParameters
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Fields.BarcodeParameters – Ihr unverzichtbares Tool für die nahtlose Barcode-Generierung und -Anpassung bei der Dokumentenverarbeitung.
type: docs
weight: 1880
url: /de/net/aspose.words.fields/barcodeparameters/
---
## BarcodeParameters class

Containerklasse für Barcode-Parameter zur Weiterleitung an BarcodeGenerator.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Feldern](https://docs.aspose.com/words/net/working-with-fields/) Dokumentationsartikel.

```csharp
public class BarcodeParameters
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [BarcodeParameters](barcodeparameters/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [AddStartStopChar](../../aspose.words.fields/barcodeparameters/addstartstopchar/) { get; set; } | Ob Start-/Stoppzeichen für die Barcodetypen NW7 und CODE39 hinzugefügt werden sollen. |
| [BackgroundColor](../../aspose.words.fields/barcodeparameters/backgroundcolor/) { get; set; } | Barcode-Hintergrundfarbe (0x000000 - 0xFFFFFF) |
| [BarcodeType](../../aspose.words.fields/barcodeparameters/barcodetype/) { get; set; } | Barcodetyp. |
| [BarcodeValue](../../aspose.words.fields/barcodeparameters/barcodevalue/) { get; set; } | Zu kodierende Daten. |
| [CaseCodeStyle](../../aspose.words.fields/barcodeparameters/casecodestyle/) { get; set; } | Stil eines Case Codes für Barcode-Typ ITF14. Gültige Werte sind [STD&#x7C;EXT&#x7C;ADD] |
| [DisplayText](../../aspose.words.fields/barcodeparameters/displaytext/) { get; set; } | Ob Barcode-Daten (Text) zusammen mit dem Bild angezeigt werden sollen. |
| [ErrorCorrectionLevel](../../aspose.words.fields/barcodeparameters/errorcorrectionlevel/) { get; set; } | Fehlerkorrekturstufe des QR-Codes. Gültige Werte sind [0, 3]. |
| [FacingIdentificationMark](../../aspose.words.fields/barcodeparameters/facingidentificationmark/) { get; set; } | Art einer gegenüberliegenden Identifikationsmarke (FIM). |
| [FixCheckDigit](../../aspose.words.fields/barcodeparameters/fixcheckdigit/) { get; set; } | Ob die Prüfziffer korrigiert werden soll, wenn sie ungültig ist. |
| [ForegroundColor](../../aspose.words.fields/barcodeparameters/foregroundcolor/) { get; set; } | Vordergrundfarbe des Barcodes (0x000000 - 0xFFFFFF) |
| [IsBookmark](../../aspose.words.fields/barcodeparameters/isbookmark/) { get; set; } | Ob[`PostalAddress`](./postaladdress/) ist der Name eines Lesezeichens. |
| [IsUSPostalAddress](../../aspose.words.fields/barcodeparameters/isuspostaladdress/) { get; set; } | Ob[`PostalAddress`](./postaladdress/) ist eine US-Postanschrift. |
| [PosCodeStyle](../../aspose.words.fields/barcodeparameters/poscodestyle/) { get; set; } | Stil eines Point-of-Sale-Barcodes (Barcode-Typen UPCA&#x7C;UPCE&#x7C;EAN13&#x7C;EAN8). Gültige Werte (ohne Berücksichtigung der Groß-/Kleinschreibung) sind [STD&#x7C;SUP2&#x7C;SUP5&#x7C;CASE]. |
| [PostalAddress](../../aspose.words.fields/barcodeparameters/postaladdress/) { get; set; } | Barcode-Postanschrift. |
| [ScalingFactor](../../aspose.words.fields/barcodeparameters/scalingfactor/) { get; set; } | Skalierungsfaktor für das Symbol. Der Wert wird in ganzen Prozentpunkten angegeben. Die gültigen Werte sind [10, 1000]. |
| [SymbolHeight](../../aspose.words.fields/barcodeparameters/symbolheight/) { get; set; } | Höhe des Barcode-Bildes (in Twips – 1/1440 Zoll) |
| [SymbolRotation](../../aspose.words.fields/barcodeparameters/symbolrotation/) { get; set; } | Rotation des Barcode-Symbols. Gültige Werte sind [0, 3]. |

## Bemerkungen

Der Parametersatz entspricht den DISPLAYBARCODE-Feldoptionen. Die genaue Liste finden Sie unter[https://msdn.microsoft.com/en-us/library/hh745901(v=office.12).aspx](https://msdn.microsoft.com/en-us/library/hh745901(v=office.12).aspx)

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
