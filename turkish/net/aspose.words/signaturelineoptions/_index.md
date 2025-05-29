---
title: SignatureLineOptions Class
linktitle: SignatureLineOptions
articleTitle: SignatureLineOptions
second_title: .NET için Aspose.Words
description: Belgelerinizdeki imza satırlarını kolayca özelleştirmek için Aspose.Words.SignatureLineOptions'ı keşfedin. DocumentBuilder deneyiminizi bugün geliştirin!
type: docs
weight: 6940
url: /tr/net/aspose.words/signaturelineoptions/
---
## SignatureLineOptions class

Eklenen imza satırı için seçeneklerin belirtilmesine izin verir. İçinde kullanılır[`DocumentBuilder`](../documentbuilder/) .

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Dijital İmzalarla Çalışın](https://docs.aspose.com/words/net/working-with-digital-signatures/) belgeleme makalesi.

```csharp
public class SignatureLineOptions
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [SignatureLineOptions](signaturelineoptions/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [AllowComments](../../aspose.words/signaturelineoptions/allowcomments/) { get; set; } | İmzalayanın İmza iletişim kutusuna yorum ekleyebileceğini belirten bir değer alır veya ayarlar. Bu özellik için varsayılan değer`YANLIŞ` . |
| [DefaultInstructions](../../aspose.words/signaturelineoptions/defaultinstructions/) { get; set; } | İşaret iletişim kutusunda varsayılan talimatların gösterildiğini belirten bir değer alır veya ayarlar. Bu özellik için varsayılan değer`doğru` . |
| [Email](../../aspose.words/signaturelineoptions/email/) { get; set; } | Önerilen imzalayanın e-posta adresini alır veya ayarlar. Bu özellik için varsayılan değer**boş dize** (Empty ). |
| [Instructions](../../aspose.words/signaturelineoptions/instructions/) { get; set; } | İmza satırının imzalanması sırasında görüntülenen imzalayana talimatları alır veya ayarlar. Bu özellik için varsayılan değer**boş dize** (Empty ). |
| [ShowDate](../../aspose.words/signaturelineoptions/showdate/) { get; set; } | İmza satırında imza tarihinin gösterildiğini belirten bir değer alır veya ayarlar. Bu özellik için varsayılan değer`doğru` . |
| [Signer](../../aspose.words/signaturelineoptions/signer/) { get; set; } | İmza satırının önerilen imzalayıcısını alır veya ayarlar. Bu özellik için varsayılan değer**boş dize** (Empty ). |
| [SignerTitle](../../aspose.words/signaturelineoptions/signertitle/) { get; set; } | Önerilen imzalayanın unvanını alır veya ayarlar. Bu özellik için varsayılan değer**boş dize** (Empty ). |

## Örnekler

Kişisel sertifika ve imza satırı ile bir belgenin nasıl imzalanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

SignatureLineOptions signatureLineOptions = new SignatureLineOptions
{
    Signer = "vderyushev",
    SignerTitle = "QA",
    Email = "vderyushev@aspose.com",
    ShowDate = true,
    DefaultInstructions = false,
    Instructions = "Please sign here.",
    AllowComments = true
};

SignatureLine signatureLine = builder.InsertSignatureLine(signatureLineOptions).SignatureLine;
signatureLine.ProviderId = Guid.Parse("CF5A7BB4-8F3C-4756-9DF6-BEF7F13259A2");

Assert.False(signatureLine.IsSigned);
Assert.False(signatureLine.IsValid);

doc.Save(ArtifactsDir + "DocumentBuilder.SignatureLineProviderId.docx");

SignOptions signOptions = new SignOptions
{
    SignatureLineId = signatureLine.Id,
    ProviderId = signatureLine.ProviderId,
    Comments = "Document was signed by vderyushev",
    SignTime = DateTime.Now
};

CertificateHolder certHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

DigitalSignatureUtil.Sign(ArtifactsDir + "DocumentBuilder.SignatureLineProviderId.docx", 
    ArtifactsDir + "DocumentBuilder.SignatureLineProviderId.Signed.docx", certHolder, signOptions);

// Kaydedilen belgemizi yeniden açın ve "IsSigned" ve "IsValid" özelliklerinin her ikisinin de "true" değerine eşit olduğunu doğrulayın,
// imza satırının bir imza içerdiğini belirtir.
doc = new Document(ArtifactsDir + "DocumentBuilder.SignatureLineProviderId.Signed.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
signatureLine = shape.SignatureLine;

Assert.True(signatureLine.IsSigned);
Assert.True(signatureLine.IsValid);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
