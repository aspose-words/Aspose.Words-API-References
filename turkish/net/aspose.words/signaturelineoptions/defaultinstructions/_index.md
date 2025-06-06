---
title: SignatureLineOptions.DefaultInstructions
linktitle: DefaultInstructions
articleTitle: DefaultInstructions
second_title: .NET için Aspose.Words
description: SignatureLineOptions DefaultInstructions özelliğinin, sorunsuz bir kullanıcı deneyimi için İmza iletişim kutunuzu özelleştirilebilir varsayılan talimatlarla nasıl geliştirdiğini keşfedin.
type: docs
weight: 30
url: /tr/net/aspose.words/signaturelineoptions/defaultinstructions/
---
## SignatureLineOptions.DefaultInstructions property

İşaret iletişim kutusunda varsayılan talimatların gösterildiğini belirten bir değer alır veya ayarlar. Bu özellik için varsayılan değer`doğru` .

```csharp
public bool DefaultInstructions { get; set; }
```

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

* class [SignatureLineOptions](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
