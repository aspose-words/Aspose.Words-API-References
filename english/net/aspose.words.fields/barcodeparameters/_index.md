---
title: BarcodeParameters Class
linktitle: BarcodeParameters
articleTitle: BarcodeParameters
second_title: Aspose.Words for .NET
description: Aspose.Words.Fields.BarcodeParameters class. Container class for barcode parameters to passthrough to BarcodeGenerator in C#.
type: docs
weight: 1850
url: /net/aspose.words.fields/barcodeparameters/
---
## BarcodeParameters class

Container class for barcode parameters to pass-through to BarcodeGenerator.

To learn more, visit the [Working with Fields](https://docs.aspose.com/words/net/working-with-fields/) documentation article.

```csharp
public class BarcodeParameters
```

## Constructors

| Name | Description |
| --- | --- |
| [BarcodeParameters](barcodeparameters/)() | The default constructor. |

## Properties

| Name | Description |
| --- | --- |
| [AddStartStopChar](../../aspose.words.fields/barcodeparameters/addstartstopchar/) { get; set; } | Whether to add Start/Stop characters for barcode types NW7 and CODE39. |
| [BackgroundColor](../../aspose.words.fields/barcodeparameters/backgroundcolor/) { get; set; } | Bar code background color (0x000000 - 0xFFFFFF) |
| [BarcodeType](../../aspose.words.fields/barcodeparameters/barcodetype/) { get; set; } | Bar code type. |
| [BarcodeValue](../../aspose.words.fields/barcodeparameters/barcodevalue/) { get; set; } | Data to be encoded. |
| [CaseCodeStyle](../../aspose.words.fields/barcodeparameters/casecodestyle/) { get; set; } | Style of a Case Code for barcode type ITF14. The valid values are [STD&#x7C;EXT&#x7C;ADD] |
| [DisplayText](../../aspose.words.fields/barcodeparameters/displaytext/) { get; set; } | Whether to display barcode data (text) along with image. |
| [ErrorCorrectionLevel](../../aspose.words.fields/barcodeparameters/errorcorrectionlevel/) { get; set; } | Error correction level of QR Code. Valid values are [0, 3]. |
| [FacingIdentificationMark](../../aspose.words.fields/barcodeparameters/facingidentificationmark/) { get; set; } | Type of a Facing Identification Mark (FIM). |
| [FixCheckDigit](../../aspose.words.fields/barcodeparameters/fixcheckdigit/) { get; set; } | Whether to fix the check digit if it’s invalid. |
| [ForegroundColor](../../aspose.words.fields/barcodeparameters/foregroundcolor/) { get; set; } | Bar code foreground color (0x000000 - 0xFFFFFF) |
| [IsBookmark](../../aspose.words.fields/barcodeparameters/isbookmark/) { get; set; } | Whether [`PostalAddress`](./postaladdress/) is the name of a bookmark. |
| [IsUSPostalAddress](../../aspose.words.fields/barcodeparameters/isuspostaladdress/) { get; set; } | Whether [`PostalAddress`](./postaladdress/) is a U.S. postal address. |
| [PosCodeStyle](../../aspose.words.fields/barcodeparameters/poscodestyle/) { get; set; } | Style of a Point of Sale barcode (barcode types UPCA&#x7C;UPCE&#x7C;EAN13&#x7C;EAN8). The valid values (case insensitive) are [STD&#x7C;SUP2&#x7C;SUP5&#x7C;CASE]. |
| [PostalAddress](../../aspose.words.fields/barcodeparameters/postaladdress/) { get; set; } | Barcode postal address. |
| [ScalingFactor](../../aspose.words.fields/barcodeparameters/scalingfactor/) { get; set; } | Scaling factor for the symbol. The value is in whole percentage points and the valid values are [10, 1000]. |
| [SymbolHeight](../../aspose.words.fields/barcodeparameters/symbolheight/) { get; set; } | Bar code image height (in twips - 1/1440 inches) |
| [SymbolRotation](../../aspose.words.fields/barcodeparameters/symbolrotation/) { get; set; } | Rotation of the barcode symbol. Valid values are [0, 3]. |

## Remarks

The set of parameters are according to DISPLAYBARCODE field options. See the exact list at [https://msdn.microsoft.com/en-us/library/hh745901(v=office.12).aspx](https://msdn.microsoft.com/en-us/library/hh745901(v=office.12).aspx)

## Examples

Shows how to use a barcode generator.

```csharp
Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);
            // We can use a custom IBarcodeGenerator implementation to generate barcodes,
            // and then insert them into the document as images.
            doc.FieldOptions.BarcodeGenerator = new CustomBarcodeGenerator();

            // Below are four examples of different barcode types that we can create using our generator.
            // For each barcode, we specify a new set of barcode parameters, and then generate the image.
            // Afterwards, we can insert the image into the document, or save it to the local file system.
            // 1 -  QR code:
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

            // 2 -  EAN13 barcode:
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

            // 3 -  CODE39 barcode:
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

            // 4 -  ITF14 barcode:
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

### See Also

* namespace [Aspose.Words.Fields](../../aspose.words.fields/)
* assembly [Aspose.Words](../../)
