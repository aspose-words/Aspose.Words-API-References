---
title: Class PdfDigitalSignatureDetails
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Saving.PdfDigitalSignatureDetails فصل. يحتوي على تفاصيل توقيع مستند PDF بتوقيع رقمي.
type: docs
weight: 5430
url: /ar/net/aspose.words.saving/pdfdigitalsignaturedetails/
---
## PdfDigitalSignatureDetails class

يحتوي على تفاصيل توقيع مستند PDF بتوقيع رقمي.

```csharp
public class PdfDigitalSignatureDetails
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [PdfDigitalSignatureDetails](pdfdigitalsignaturedetails/#constructor)() | تهيئة مثيل لهذه الفئة. |
| [PdfDigitalSignatureDetails](pdfdigitalsignaturedetails/#constructor_1)(CertificateHolder, string, string, DateTime) | تهيئة مثيل لهذه الفئة. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [CertificateHolder](../../aspose.words.saving/pdfdigitalsignaturedetails/certificateholder/) { get; set; } | إرجاع كائن حامل الشهادة الذي يحتوي على الشهادة المستخدمة لتوقيع المستند. |
| [HashAlgorithm](../../aspose.words.saving/pdfdigitalsignaturedetails/hashalgorithm/) { get; set; } | الحصول على خوارزمية التجزئة أو تعيينها. |
| [Location](../../aspose.words.saving/pdfdigitalsignaturedetails/location/) { get; set; } | الحصول على أو تعيين موقع التوقيع. |
| [Reason](../../aspose.words.saving/pdfdigitalsignaturedetails/reason/) { get; set; } | الحصول على سبب التوقيع أو تحديده. |
| [SignatureDate](../../aspose.words.saving/pdfdigitalsignaturedetails/signaturedate/) { get; set; } | الحصول على أو تحديد تاريخ التوقيع. |
| [TimestampSettings](../../aspose.words.saving/pdfdigitalsignaturedetails/timestampsettings/) { get; set; } | الحصول على إعدادات الطابع الزمني للتوقيع الرقمي أو تعيينها. |

### ملاحظات

في الوقت الحالي، يتوفر التوقيع الرقمي لمستندات PDF فقط على .NET 2.0 أو أعلى.

لتوقيع مستند PDF رقميًا عند إنشائه بواسطة Aspose.Words، قم بتعيين الإعداد[`DigitalSignatureDetails`](../pdfsaveoptions/digitalsignaturedetails/) خاصية صالحة`PdfDigitalSignatureDetails` الكائن ثم احفظ المستند بتنسيق PDF بتمرير إلى ملف[`PdfSaveOptions`](../pdfsaveoptions/) كمعلمة في[`Save`](../../aspose.words/document/save/) طريقة.

يقوم Aspose.Words بإنشاء توقيع PKCS#7 على مستند PDF بالكامل ويستخدم مرشح "Adobe.PPKMS" ومرشح "adbe.pkcs7.sha1" عند إنشاء توقيع رقمي.

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

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)


