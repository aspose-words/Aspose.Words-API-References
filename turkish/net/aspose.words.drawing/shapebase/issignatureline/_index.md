---
title: ShapeBase.IsSignatureLine
linktitle: IsSignatureLine
articleTitle: IsSignatureLine
second_title: .NET için Aspose.Words
description: Şekilleri SignatureLines olarak tanımlayan ve belge bütünlüğünü ve profesyonel sunumu artıran ShapeBase'in IsSignatureLine özelliğini keşfedin.
type: docs
weight: 360
url: /tr/net/aspose.words.drawing/shapebase/issignatureline/
---
## ShapeBase.IsSignatureLine property

Şeklin bir[`SignatureLine`](../../signatureline/) .

```csharp
public bool IsSignatureLine { get; }
```

## Örnekler

İmza için bir satırın nasıl oluşturulacağını ve belgeye nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

SignatureLineOptions options = new SignatureLineOptions
{
    AllowComments = true,
    DefaultInstructions = true,
    Email = "john.doe@management.com",
    Instructions = "Please sign here",
    ShowDate = true,
    Signer = "John Doe",
    SignerTitle = "Senior Manager"
};

// Görünümünü belirleyeceğimiz bir imza satırı içerecek bir şekil ekleyin.
// Yukarıda oluşturduğumuz "SignatureLineOptions" nesnesini kullanarak özelleştiriyoruz.
// Sayfanın sağ alt köşesinden koordinatları çıkan bir şekil eklersek,
// Şekli görünür hale getirmek için negatif x ve y koordinatlarını sağlamamız gerekecek.
Shape shape = builder.InsertSignatureLine(options, RelativeHorizontalPosition.RightMargin, -170.0,
        RelativeVerticalPosition.BottomMargin, -60.0, WrapType.None);

Assert.True(shape.IsSignatureLine);

// İmza satırımızın özelliklerini Shape nesnesi aracılığıyla doğrulayalım.
SignatureLine signatureLine = shape.SignatureLine;

Assert.AreEqual("john.doe@management.com", signatureLine.Email);
Assert.AreEqual("John Doe", signatureLine.Signer);
Assert.AreEqual("Senior Manager", signatureLine.SignerTitle);
Assert.AreEqual("Please sign here", signatureLine.Instructions);
Assert.True(signatureLine.ShowDate);
Assert.True(signatureLine.AllowComments);
Assert.True(signatureLine.DefaultInstructions);

doc.Save(ArtifactsDir + "Shape.SignatureLine.docx");
```

### Ayrıca bakınız

* class [ShapeBase](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
