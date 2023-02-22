---
title: PdfDigitalSignatureDetails.SignatureDate
second_title: Aspose.Words لمراجع .NET API
description: PdfDigitalSignatureDetails ملكية. الحصول على تاريخ التوقيع أو تحديده.
type: docs
weight: 60
url: /ar/net/aspose.words.saving/pdfdigitalsignaturedetails/signaturedate/
---
## PdfDigitalSignatureDetails.SignatureDate property

الحصول على تاريخ التوقيع أو تحديده.

```csharp
public DateTime SignatureDate { get; set; }
```

### ملاحظات

القيمة الافتراضية هي الوقت الحالي.

ستظهر هذه القيمة في التوقيع الرقمي كوقت كمبيوتر لم يتم التحقق منه.

### أمثلة

يوضح كيفية التوقيع على مستند PDF تم إنشاؤه.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Contents of signed PDF.");

CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// قم بإنشاء كائن "PdfSaveOptions" يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة المستند إلى PDF.
PdfSaveOptions options = new PdfSaveOptions();

// تكوين كائن "DigitalSignatureDetails" من كائن "SaveOptions" إليه
// قم بالتوقيع رقميًا على المستند كما نعرضه بطريقة "حفظ".
DateTime signingTime = DateTime.Now;
options.DigitalSignatureDetails =
    new PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "My Office", signingTime);
options.DigitalSignatureDetails.HashAlgorithm = PdfDigitalSignatureHashAlgorithm.Sha256;

Assert.AreEqual("Test Signing", options.DigitalSignatureDetails.Reason);
Assert.AreEqual("My Office", options.DigitalSignatureDetails.Location);
Assert.AreEqual(signingTime.ToUniversalTime(), options.DigitalSignatureDetails.SignatureDate.ToUniversalTime());

doc.Save(ArtifactsDir + "PdfSaveOptions.PdfDigitalSignature.pdf", options);
```

### أنظر أيضا

* class [PdfDigitalSignatureDetails](../)
* مساحة الاسم [Aspose.Words.Saving](../../pdfdigitalsignaturedetails/)
* المجسم [Aspose.Words](../../../)


