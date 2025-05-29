---
title: PdfDigitalSignatureDetails Class
linktitle: PdfDigitalSignatureDetails
articleTitle: PdfDigitalSignatureDetails
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.PdfDigitalSignatureDetails لتوقيع رقمي سلس لملفات PDF. عزز أمان المستندات من خلال التكامل السهل والميزات القوية.
type: docs
weight: 6220
url: /ar/net/aspose.words.saving/pdfdigitalsignaturedetails/
---
## PdfDigitalSignatureDetails class

يحتوي على تفاصيل حول توقيع مستند PDF باستخدام توقيع رقمي.

```csharp
public class PdfDigitalSignatureDetails
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [PdfDigitalSignatureDetails](pdfdigitalsignaturedetails/#constructor)() | يقوم بتهيئة مثيل لهذه الفئة. |
| [PdfDigitalSignatureDetails](pdfdigitalsignaturedetails/#constructor_1)(*[CertificateHolder](../../aspose.words.digitalsignatures/certificateholder/), string, string, DateTime*) | يقوم بتهيئة مثيل لهذه الفئة. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [CertificateHolder](../../aspose.words.saving/pdfdigitalsignaturedetails/certificateholder/) { get; set; } | يعيد كائن حامل الشهادة الذي يحتوي على الشهادة التي تم استخدامها لتوقيع المستند. |
| [HashAlgorithm](../../aspose.words.saving/pdfdigitalsignaturedetails/hashalgorithm/) { get; set; } | يحصل على خوارزمية التجزئة أو يعينها. |
| [Location](../../aspose.words.saving/pdfdigitalsignaturedetails/location/) { get; set; } | يحصل على موقع التوقيع أو يعينه. |
| [Reason](../../aspose.words.saving/pdfdigitalsignaturedetails/reason/) { get; set; } | يحصل على سبب التوقيع أو يحدده. |
| [SignatureDate](../../aspose.words.saving/pdfdigitalsignaturedetails/signaturedate/) { get; set; } | يحصل على تاريخ التوقيع أو يعينه. |
| [TimestampSettings](../../aspose.words.saving/pdfdigitalsignaturedetails/timestampsettings/) { get; set; } | يحصل على إعدادات طابع زمني للتوقيع الرقمي أو يعينها. |

## ملاحظات

في الوقت الحالي، يتوفر التوقيع الرقمي على مستندات PDF فقط على .NET 3.5 أو أعلى.

لتوقيع مستند PDF رقميًا عند إنشائه بواسطة Aspose.Words، اضبط[`DigitalSignatureDetails`](../pdfsaveoptions/digitalsignaturedetails/) الخاصية إلى صالحة`PdfDigitalSignatureDetails` الكائن ثم احفظ المستند بتنسيق PDF عن طريق تمرير [`PdfSaveOptions`](../pdfsaveoptions/) كمعلمة في[`Save`](../../aspose.words/document/save/) طريقة.

يقوم Aspose.Words بإنشاء توقيع PKCS#7 على مستند PDF بأكمله ويستخدم مرشح "Adobe.PPKMS" ومرشح فرعي "adbe.pkcs7.sha1" عند إنشاء توقيع رقمي.

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

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
