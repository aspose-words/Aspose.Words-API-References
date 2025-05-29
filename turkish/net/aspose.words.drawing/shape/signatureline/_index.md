---
title: Shape.SignatureLine
linktitle: SignatureLine
articleTitle: SignatureLine
second_title: .NET için Aspose.Words
description: Şekilleriniz için SignatureLine nesnesine nasıl erişeceğinizi keşfedin. İmza satırlarını kolayca tanımlayın ve belgenizin profesyonelliğini artırın!
type: docs
weight: 170
url: /tr/net/aspose.words.drawing/shape/signatureline/
---
## Shape.SignatureLine property

Alır[`SignatureLine`](../../signatureline/) şekil bir imza satırıysa nesne. Geri döner`hükümsüz` aksi takdirde.

```csharp
public SignatureLine SignatureLine { get; }
```

## Notlar

Yeni ekleyebilirsiniz[`SignatureLine`](../../signatureline/) kullanarak belgeye girin[`InsertSignatureLine`](../../../aspose.words/documentbuilder/insertsignatureline/) ve

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

* class [SignatureLine](../../signatureline/)
* class [Shape](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
