---
title: Shape.SignatureLine
second_title: Aspose.Words for .NET API Referansı
description: Shape mülk. AlırSignatureLine şekil bir imza satırı ise nesne. İadeler hükümsüz aksi halde.
type: docs
weight: 160
url: /tr/net/aspose.words.drawing/shape/signatureline/
---
## Shape.SignatureLine property

Alır`SignatureLine` şekil bir imza satırı ise nesne. İadeler **hükümsüz** aksi halde.

```csharp
public SignatureLine SignatureLine { get; }
```

### Notlar

kullanarak belgeye yeni SignatureLines ekleyebilirsiniz.[`InsertSignatureLine`](../../../aspose.words/documentbuilder/insertsignatureline/) and

### Örnekler

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

// Görünüşünü değiştireceğimiz bir imza satırı içerecek bir şekil ekleyin
// yukarıda oluşturduğumuz "SignatureLineOptions" nesnesini kullanarak özelleştirelim.
// Koordinatları sayfanın sağ alt köşesinden başlayan bir şekil eklersek,
// şekli görüntüye getirmek için negatif x ve y koordinatlarını sağlamamız gerekecek.
Shape shape = builder.InsertSignatureLine(options, RelativeHorizontalPosition.RightMargin, -170.0, 
        RelativeVerticalPosition.BottomMargin, -60.0, WrapType.None);

Assert.True(shape.IsSignatureLine);

// İmza satırımızın özelliklerini Shape nesnesi aracılığıyla doğrulayın.
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

* class [SignatureLine](../../signatureline/)
* class [Shape](../)
* ad alanı [Aspose.Words.Drawing](../../shape/)
* toplantı [Aspose.Words](../../../)


