---
title: PdfDigitalSignatureDetails.HashAlgorithm
second_title: Aspose.Words لمراجع .NET API
description: PdfDigitalSignatureDetails ملكية. الحصول على خوارزمية التجزئة أو تعيينها.
type: docs
weight: 30
url: /ar/net/aspose.words.saving/pdfdigitalsignaturedetails/hashalgorithm/
---
## PdfDigitalSignatureDetails.HashAlgorithm property

الحصول على خوارزمية التجزئة أو تعيينها.

```csharp
public PdfDigitalSignatureHashAlgorithm HashAlgorithm { get; set; }
```

### ملاحظات

القيمة الافتراضية هي خوارزمية SHA-256.

### أمثلة

يوضح كيفية التوقيع على مستند PDF تم إنشاؤه.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Contents of signed PDF.");

CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" المستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// قم بتكوين كائن "DigitalSignatureDetails" للكائن "SaveOptions" إلى
// قم بتوقيع المستند رقميًا أثناء عرضه باستخدام طريقة "الحفظ".
DateTime signingTime = new DateTime(2015, 7, 20);
options.DigitalSignatureDetails =
    new PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "My Office", signingTime);
options.DigitalSignatureDetails.HashAlgorithm = PdfDigitalSignatureHashAlgorithm.RipeMD160;

Assert.AreEqual("Test Signing", options.DigitalSignatureDetails.Reason);
Assert.AreEqual("My Office", options.DigitalSignatureDetails.Location);
Assert.AreEqual(signingTime, options.DigitalSignatureDetails.SignatureDate.ToLocalTime());

doc.Save(ArtifactsDir + "PdfSaveOptions.PdfDigitalSignature.pdf", options);
```

### أنظر أيضا

* enum [PdfDigitalSignatureHashAlgorithm](../../pdfdigitalsignaturehashalgorithm/)
* class [PdfDigitalSignatureDetails](../)
* مساحة الاسم [Aspose.Words.Saving](../../pdfdigitalsignaturedetails/)
* المجسم [Aspose.Words](../../../)


