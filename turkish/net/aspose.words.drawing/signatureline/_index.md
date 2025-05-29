---
title: SignatureLine Class
linktitle: SignatureLine
articleTitle: SignatureLine
second_title: .NET için Aspose.Words
description: Gelişmiş belge güvenliği için imza satırı özelliklerini kolayca yönetmek ve özelleştirmek amacıyla Aspose.Words.Drawing.SignatureLine sınıfını keşfedin.
type: docs
weight: 1700
url: /tr/net/aspose.words.drawing/signatureline/
---
## SignatureLine class

İmza satırı özelliklerine erişim sağlar.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Dijital İmzalarla Çalışın](https://docs.aspose.com/words/net/working-with-digital-signatures/) belgeleme makalesi.

```csharp
public class SignatureLine
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [AllowComments](../../aspose.words.drawing/signatureline/allowcomments/) { get; set; } | İmzalayanın İmza iletişim kutusuna yorum ekleyebileceğini belirten bir değer alır veya ayarlar. Bu özellik için varsayılan değer`YANLIŞ` . |
| [DefaultInstructions](../../aspose.words.drawing/signatureline/defaultinstructions/) { get; set; } | İşaret iletişim kutusunda varsayılan talimatların gösterildiğini belirten bir değer alır veya ayarlar. Bu özellik için varsayılan değer`doğru` . |
| [Email](../../aspose.words.drawing/signatureline/email/) { get; set; } | Önerilen imzalayanın e-posta adresini alır veya ayarlar. Bu özellik için varsayılan değer**boş dize** (Empty ). |
| [Id](../../aspose.words.drawing/signatureline/id/) { get; set; } | Bu imza satırı için tanımlayıcıyı alır veya ayarlar. |
| [Instructions](../../aspose.words.drawing/signatureline/instructions/) { get; set; } | İmza satırının imzalanması sırasında görüntülenen imzalayana yönelik talimatları alır veya ayarlar. Bu özellik, aşağıdaki durumlarda göz ardı edilir:[`DefaultInstructions`](./defaultinstructions/) set. Bu özellik için varsayılan değer**boş dize** (Empty ). |
| [IsSigned](../../aspose.words.drawing/signatureline/issigned/) { get; } | İmza satırının dijital imza ile imzalandığını belirtir. |
| [IsValid](../../aspose.words.drawing/signatureline/isvalid/) { get; } | İmza satırının dijital imza ile imzalandığını ve bu dijital imzanın geçerli olduğunu belirtir. |
| [ProviderId](../../aspose.words.drawing/signatureline/providerid/) { get; set; } | Bu imza satırı için imza sağlayıcı tanımlayıcısını alır veya ayarlar. Varsayılan değer "{00000000-0000-0000-0000-000000000000}"'dir. |
| [ShowDate](../../aspose.words.drawing/signatureline/showdate/) { get; set; } | İmza satırında imza tarihinin gösterildiğini belirten bir değer alır veya ayarlar. Bu özellik için varsayılan değer`doğru` . |
| [Signer](../../aspose.words.drawing/signatureline/signer/) { get; set; } | İmza satırının önerilen imzalayıcısını alır veya ayarlar. Bu özellik için varsayılan değer**boş dize** (Empty ). |
| [SignerTitle](../../aspose.words.drawing/signatureline/signertitle/) { get; set; } | Önerilen imzalayanın unvanını alır veya ayarlar (örneğin, Yönetici). Bu özellik için varsayılan değer**boş dize** (Empty ). |

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

* ad alanı [Aspose.Words.Drawing](../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../)
