---
title: SignatureLine.DefaultInstructions
linktitle: DefaultInstructions
articleTitle: DefaultInstructions
second_title: .NET için Aspose.Words
description: SignatureLine DefaultInstructions özelliğinin, kusursuz bir kullanıcı deneyimi için İmza iletişim kutunuzu özelleştirilebilir varsayılan talimatlarla nasıl geliştirdiğini keşfedin.
type: docs
weight: 20
url: /tr/net/aspose.words.drawing/signatureline/defaultinstructions/
---
## SignatureLine.DefaultInstructions property

İşaret iletişim kutusunda varsayılan talimatların gösterildiğini belirten bir değer alır veya ayarlar. Bu özellik için varsayılan değer`doğru` .

```csharp
public bool DefaultInstructions { get; set; }
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
