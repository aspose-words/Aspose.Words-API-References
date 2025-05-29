---
title: DocumentBuilder.InsertSignatureLine
linktitle: InsertSignatureLine
articleTitle: InsertSignatureLine
second_title: .NET için Aspose.Words
description: DocumentBuilder InsertSignatureLine yöntemi ile belgelerinize zahmetsizce profesyonel imza satırları ekleyin. İş akışınızı bugün geliştirin!
type: docs
weight: 470
url: /tr/net/aspose.words/documentbuilder/insertsignatureline/
---
## InsertSignatureLine(*[SignatureLineOptions](../../signaturelineoptions/)*) {#insertsignatureline}

Geçerli konuma bir imza satırı ekler.

```csharp
public Shape InsertSignatureLine(SignatureLineOptions signatureLineOptions)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| signatureLineOptions | SignatureLineOptions | İmza satırı oluşturma parametrelerinin saklandığı nesne. |

### Geri dönüş değeri

Az önce eklenen imza satırı düğümü.

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

* class [Shape](../../../aspose.words.drawing/shape/)
* class [SignatureLineOptions](../../signaturelineoptions/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## InsertSignatureLine(*[SignatureLineOptions](../../signaturelineoptions/), [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/), double, [WrapType](../../../aspose.words.drawing/wraptype/)*) {#insertsignatureline_1}

Belirtilen konuma bir imza satırı ekler.

```csharp
public Shape InsertSignatureLine(SignatureLineOptions signatureLineOptions, 
    RelativeHorizontalPosition horzPos, double left, RelativeVerticalPosition vertPos, double top, 
    WrapType wrapType)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| signatureLineOptions | SignatureLineOptions | İmza satırı oluşturma parametrelerinin saklandığı nesne. |
| horzPos | RelativeHorizontalPosition | İmza satırına olan mesafenin nereden ölçüleceğini belirtir. |
| left | Double | İmza çizgisinin sol tarafına kadar olan başlangıç noktasından noktasal uzaklık. |
| vertPos | RelativeVerticalPosition | İmza satırına olan mesafenin nereden ölçüleceğini belirtir. |
| top | Double | İmza çizgisinin başlangıç noktasından üst kısmına kadar olan mesafe. |
| wrapType | WrapType | İmza satırının etrafına metnin nasıl sarılacağını belirtir. |

### Geri dönüş değeri

Az önce eklenen imza satırı düğümü.

## Notlar

kullanarak görüntü boyutunu, konumunu, konumlandırma yöntemini ve diğer ayarları değiştirebilirsiniz.[`Shape`](../../../aspose.words.drawing/shape/) Bu metot tarafından döndürülen nesne.

## Örnekler

Bir belgeye satır içi imza satırının nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

SignatureLineOptions options = new SignatureLineOptions
{
    Signer = "John Doe",
    SignerTitle = "Manager",
    Email = "johndoe@aspose.com",
    ShowDate = true,
    DefaultInstructions = false,
    Instructions = "Please sign here.",
    AllowComments = true
};

builder.InsertSignatureLine(options, RelativeHorizontalPosition.RightMargin, 2.0,
    RelativeVerticalPosition.Page, 3.0, WrapType.Inline);

// Microsoft Word'de imza satırına çift tıklanarak imza atılabilir.
doc.Save(ArtifactsDir + "DocumentBuilder.SignatureLineInline.docx");
```

### Ayrıca bakınız

* class [Shape](../../../aspose.words.drawing/shape/)
* class [SignatureLineOptions](../../signaturelineoptions/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
