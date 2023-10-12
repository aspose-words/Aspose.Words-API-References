---
title: SignatureLine.Instructions
second_title: Aspose.Words for .NET API Referansı
description: SignatureLine mülk. İmza satırını imzalarken görüntülenen imzalayana yönelik talimatları alır veya ayarlar. Aşağıdaki durumlarda bu özellik yoksayılırDefaultInstructionsayarlandı. Bu özelliğin varsayılan değeri boş dize Empty.
type: docs
weight: 50
url: /tr/net/aspose.words.drawing/signatureline/instructions/
---
## SignatureLine.Instructions property

İmza satırını imzalarken görüntülenen imzalayana yönelik talimatları alır veya ayarlar. Aşağıdaki durumlarda bu özellik yoksayılır:[`DefaultInstructions`](../defaultinstructions/)ayarlandı. Bu özelliğin varsayılan değeri: **boş dize** (Empty).

```csharp
public string Instructions { get; set; }
```

### Örnekler

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
* ad alanı [Aspose.Words.Drawing](../../signatureline/)
* toplantı [Aspose.Words](../../../)


