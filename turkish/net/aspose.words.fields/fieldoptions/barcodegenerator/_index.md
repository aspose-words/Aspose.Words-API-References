---
title: FieldOptions.BarcodeGenerator
linktitle: BarcodeGenerator
articleTitle: BarcodeGenerator
second_title: .NET için Aspose.Words
description: FieldOptions BarcodeGenerator ile zahmetsizce özel barkodlar oluşturun. Envanter yönetiminizi geliştirin ve operasyonlarınızı bugün kolaylaştırın!
type: docs
weight: 10
url: /tr/net/aspose.words.fields/fieldoptions/barcodegenerator/
---
## FieldOptions.BarcodeGenerator property

Özel barkod oluşturucuyu alır veya ayarlar.

```csharp
public IBarcodeGenerator BarcodeGenerator { get; set; }
```

## Notlar

Özel barkod oluşturucu genel arayüzü uygulamalıdır[`IBarcodeGenerator`](../../ibarcodegenerator/) .

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

* interface [IBarcodeGenerator](../../ibarcodegenerator/)
* class [FieldOptions](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
