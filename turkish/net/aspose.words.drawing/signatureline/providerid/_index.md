---
title: SignatureLine.ProviderId
second_title: Aspose.Words for .NET API Referansı
description: SignatureLine mülk. Bu imza satırı için imza sağlayıcı tanımlayıcısını alır veya ayarlar. Varsayılan değer 00000000000000000000000000000000dır.
type: docs
weight: 80
url: /tr/net/aspose.words.drawing/signatureline/providerid/
---
## SignatureLine.ProviderId property

Bu imza satırı için imza sağlayıcı tanımlayıcısını alır veya ayarlar. Varsayılan değer "{00000000-0000-0000-0000-000000000000}"dır.

```csharp
public Guid ProviderId { get; set; }
```

### Notlar

Şifreleme hizmeti sağlayıcısı (CSP), kimlik doğrulama, kodlama ve şifreleme için gerçekten şifreleme algoritmaları gerçekleştiren bağımsız bir yazılım modülüdür. MS Office, varsayılan imza sağlayıcısı için {00000000-0000-0000-0000-000000000000} değerinde değerini saklı tutar.

Ek olarak kurulan sağlayıcının GUID'si, sağlayıcıyla birlikte gönderilen belgelerden alınmalıdır.

Ayrıca, kurulu tüm şifreleme sağlayıcıları Windows kayıt defterinde numaralandırılmıştır. Aşağıdaki yolda bulunabilir: HKLM\SOFTWARE\Microsoft\Cryptography\Defaults\Provider. Şuna karşılık gelen "CP Service UUID" anahtar adı vardır. imza sağlayıcı GUID'i.

### Örnekler

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

// Kaydedilmiş belgemizi yeniden açın ve "IsSigned" ve "IsValid" özelliklerinin her ikisinin de "true" değerine eşit olduğunu doğrulayın,
// imza satırının bir imza içerdiğini belirtir.
doc = new Document(ArtifactsDir + "DocumentBuilder.SignatureLineProviderId.Signed.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
signatureLine = shape.SignatureLine;

Assert.True(signatureLine.IsSigned);
Assert.True(signatureLine.IsValid);
```

### Ayrıca bakınız

* class [SignatureLine](../)
* ad alanı [Aspose.Words.Drawing](../../signatureline/)
* toplantı [Aspose.Words](../../../)


