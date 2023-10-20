---
title: SignOptions.ProviderId
linktitle: ProviderId
articleTitle: ProviderId
second_title: Aspose.Words for .NET
description: SignOptions ProviderId mülk. İmza sağlayıcının sınıf kimliğini belirtir. Varsayılan değerBoş tümü sıfır Kılavuz  C#'da.
type: docs
weight: 40
url: /tr/net/aspose.words.digitalsignatures/signoptions/providerid/
---
## SignOptions.ProviderId property

İmza sağlayıcının sınıf kimliğini belirtir. Varsayılan değer:**Boş (tümü sıfır) Kılavuz** .

```csharp
public Guid ProviderId { get; set; }
```

## Notlar

Şifreleme servis sağlayıcısı (CSP), kimlik doğrulama, kodlama ve şifreleme için gerçekte şifreleme algoritmalarını gerçekleştiren bağımsız bir yazılım modülüdür. MS Office, varsayılan imza sağlayıcısı için {00000000-0000-0000-0000-000000000000} değerinin değerini ayırır.

Ek olarak yüklenen sağlayıcının GUID'i, sağlayıcıyla birlikte gönderilen belgelerden alınmalıdır.

Ayrıca, kurulu tüm şifreleme sağlayıcıları Windows kayıt defterinde numaralandırılmıştır. Şu yolda bulunabilir: HKLM\SOFTWARE\Microsoft\Cryptography\Defaults\Provider. Şuna karşılık gelen bir "CP Service UUID" anahtar adı vardır: imza sağlayıcısının GUID'i.

## Örnekler

Kişisel sertifika ve imza satırı içeren bir belgenin nasıl imzalanacağını gösterir.

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

* class [SignOptions](../)
* ad alanı [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* toplantı [Aspose.Words](../../../)
