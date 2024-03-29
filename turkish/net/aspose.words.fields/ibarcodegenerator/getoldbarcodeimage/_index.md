---
title: IBarcodeGenerator.GetOldBarcodeImage
linktitle: GetOldBarcodeImage
articleTitle: GetOldBarcodeImage
second_title: Aspose.Words for .NET
description: IBarcodeGenerator GetOldBarcodeImage yöntem. Parametre kümesini kullanarak barkod görüntüsü oluşturun eski moda Barkod alanı için C#'da.
type: docs
weight: 20
url: /tr/net/aspose.words.fields/ibarcodegenerator/getoldbarcodeimage/
---
## IBarcodeGenerator.GetOldBarcodeImage method

Parametre kümesini kullanarak barkod görüntüsü oluşturun (eski moda Barkod alanı için).

```csharp
public Image GetOldBarcodeImage(BarcodeParameters parameters)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| parameters | BarcodeParameters | Parametre seti |

### Geri dönüş değeri

Oluşturulan barkodu temsil eden resim.

## Örnekler

Barkod oluşturucunun nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Barkod oluşturmak için özel bir IBarcodeGenerator uygulamasını kullanabiliriz,
// ve ardından bunları belgeye resim olarak ekleyin.
doc.FieldOptions.BarcodeGenerator = new CustomBarcodeGenerator();

// Aşağıda oluşturucumuzu kullanarak oluşturabileceğimiz farklı barkod türlerine ait dört örnek bulunmaktadır.
// Her barkod için yeni bir barkod parametreleri seti belirliyoruz ve ardından görüntüyü oluşturuyoruz.
// Daha sonra görüntüyü belgeye ekleyebilir veya yerel dosya sistemine kaydedebiliriz.
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
img.Save(ArtifactsDir + "FieldOptions.BarcodeGenerator.QR.jpg");

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
img.Save(ArtifactsDir + "FieldOptions.BarcodeGenerator.EAN13.jpg");
builder.InsertImage(img);

// 3 - CODE39 barkodu:
barcodeParameters = new BarcodeParameters
{
    BarcodeType = "CODE39",
    BarcodeValue = "12345ABCDE",
    AddStartStopChar = true
};

img = doc.FieldOptions.BarcodeGenerator.GetBarcodeImage(barcodeParameters);
img.Save(ArtifactsDir + "FieldOptions.BarcodeGenerator.CODE39.jpg");
builder.InsertImage(img);

// 4 - ITF14 barkodu:
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

### Ayrıca bakınız

* class [BarcodeParameters](../../barcodeparameters/)
* interface [IBarcodeGenerator](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
