---
title: BarcodeParameters.BackgroundColor
linktitle: BackgroundColor
articleTitle: BackgroundColor
second_title: .NET için Aspose.Words
description: Özel barkod tasarımları için BarcodeParameters BackgroundColor özelliğini keşfedin. En iyi görünürlük için arka plan renklerini 0x000000 ila 0xFFFFFF arasında kolayca ayarlayın!
type: docs
weight: 30
url: /tr/net/aspose.words.fields/barcodeparameters/backgroundcolor/
---
## BarcodeParameters.BackgroundColor property

Barkod arka plan rengi (0x000000 - 0xFFFFFF)

```csharp
public string BackgroundColor { get; set; }
```

## Örnekler

Barkod üretecinin nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Barkodları oluşturmak için özel bir IBarcodeGenerator uygulamasını kullanabiliriz.
// ve sonra bunları resim olarak belgeye ekleyin.
doc.FieldOptions.BarcodeGenerator = new CustomBarcodeGenerator();

// Aşağıda, üretecimizi kullanarak oluşturabileceğimiz farklı barkod tiplerine ait dört örnek bulunmaktadır.
// Her barkod için yeni bir barkod parametreleri kümesi belirliyoruz ve ardından görüntüyü oluşturuyoruz.
// Daha sonra resmi belgeye ekleyebiliriz veya yerel dosya sistemine kaydedebiliriz.
// 1 - QR kodu:
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

// 2 - EAN13 barkodu:
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

// 3 - CODE39 barkodu:
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

// 4 - ITF14 barkodu:
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

### Ayrıca bakınız

* class [BarcodeParameters](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
