---
title: SignatureLine.SignerTitle
linktitle: SignerTitle
articleTitle: SignerTitle
second_title: Aspose.Words for .NET
description: SignatureLine SignerTitle mülk. Önerilen imzalayanın unvanını alır veya ayarlar örneğin Yönetici. Bu özellik için varsayılan değerboş dize Empty C#'da.
type: docs
weight: 110
url: /tr/net/aspose.words.drawing/signatureline/signertitle/
---
## SignatureLine.SignerTitle property

Önerilen imzalayanın unvanını alır veya ayarlar (örneğin, Yönetici). Bu özellik için varsayılan değer:**boş dize** (Empty).

```csharp
public string SignerTitle { get; set; }
```

## Örnekler

İmza için nasıl satır oluşturulacağını ve bunun belgeye nasıl ekleneceğini gösterir.

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

// Görünümünü belirleyeceğimiz, imza çizgisi içeren bir şekil ekleyin
// yukarıda oluşturduğumuz "SignatureLineOptions" nesnesini kullanarak özelleştirin.
// Koordinatları sayfanın sağ alt köşesinden başlayan bir şekil eklersek,
// şekli görünür hale getirmek için negatif x ve y koordinatlarını sağlamamız gerekecek.
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

* class [SignatureLine](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
