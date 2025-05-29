---
title: SignatureLine.Email
linktitle: Email
articleTitle: Email
second_title: .NET için Aspose.Words
description: Önerilen imzalayanların e-posta adreslerini SignatureLine E-posta özelliğiyle zahmetsizce yönetin. Özelleştirilebilir, kullanıcı dostu özelliklerle iş akışınızı geliştirin.
type: docs
weight: 30
url: /tr/net/aspose.words.drawing/signatureline/email/
---
## SignatureLine.Email property

Önerilen imzalayanın e-posta adresini alır veya ayarlar. Bu özellik için varsayılan değer**boş dize** (Empty ).

```csharp
public string Email { get; set; }
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

* class [SignatureLine](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
