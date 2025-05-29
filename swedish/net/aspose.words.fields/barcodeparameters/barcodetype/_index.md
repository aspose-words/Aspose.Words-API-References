---
title: BarcodeParameters.BarcodeType
linktitle: BarcodeType
articleTitle: BarcodeType
second_title: Aspose.Words för .NET
description: Utforska egenskapen BarcodeParameters BarcodeType för förbättrad streckkodshantering. Upptäck dess unika funktioner och fördelar för dina projekt!
type: docs
weight: 40
url: /sv/net/aspose.words.fields/barcodeparameters/barcodetype/
---
## BarcodeParameters.BarcodeType property

Streckkodstyp.

```csharp
public string BarcodeType { get; set; }
```

## Exempel

Visar hur man använder en streckkodsgenerator.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Vi kan använda en anpassad IBarcodeGenerator-implementering för att generera streckkoder,
// och sedan infoga dem i dokumentet som bilder.
doc.FieldOptions.BarcodeGenerator = new CustomBarcodeGenerator();

// Nedan följer fyra exempel på olika streckkodstyper som vi kan skapa med vår generator.
// För varje streckkod anger vi en ny uppsättning streckkodsparametrar och genererar sedan bilden.
// Efteråt kan vi infoga bilden i dokumentet, eller spara den i det lokala filsystemet.
// 1 - QR-kod:
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

// 2 - EAN13-streckkod:
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

// 3 - CODE39 streckkod:
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

// 4 - ITF14-streckkod:
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

### Se även

* class [BarcodeParameters](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
