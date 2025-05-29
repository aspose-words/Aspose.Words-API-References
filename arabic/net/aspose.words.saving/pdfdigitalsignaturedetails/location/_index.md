---
title: PdfDigitalSignatureDetails.Location
linktitle: Location
articleTitle: Location
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية موقع PdfDigitalSignatureDetails لإدارة موقع توقيع المستندات وتخصيصه بسهولة لتحسين الأمان والكفاءة.
type: docs
weight: 40
url: /ar/net/aspose.words.saving/pdfdigitalsignaturedetails/location/
---
## PdfDigitalSignatureDetails.Location property

يحصل على موقع التوقيع أو يعينه.

```csharp
public string Location { get; set; }
```

## ملاحظات

القيمة الافتراضية هي`باطل` .

## أمثلة

يوضح كيفية توقيع مستند PDF تم إنشاؤه.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Contents of signed PDF.");

CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// قم بتكوين كائن "DigitalSignatureDetails" من كائن "SaveOptions" إلى
// قم بتوقيع المستند رقميًا أثناء عرضه باستخدام طريقة "الحفظ".
DateTime signingTime = new DateTime(2015, 7, 20);
options.DigitalSignatureDetails =
    new PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "My Office", signingTime);
options.DigitalSignatureDetails.HashAlgorithm = PdfDigitalSignatureHashAlgorithm.RipeMD160;

Assert.AreEqual("Test Signing", options.DigitalSignatureDetails.Reason);
Assert.AreEqual("My Office", options.DigitalSignatureDetails.Location);
Assert.AreEqual(signingTime, options.DigitalSignatureDetails.SignatureDate.ToLocalTime());
Assert.AreEqual(certificateHolder, options.DigitalSignatureDetails.CertificateHolder);

doc.Save(ArtifactsDir + "PdfSaveOptions.PdfDigitalSignature.pdf", options);
```

### أنظر أيضا

* class [PdfDigitalSignatureDetails](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
