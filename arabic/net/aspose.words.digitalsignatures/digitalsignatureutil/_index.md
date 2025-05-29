---
title: DigitalSignatureUtil Class
linktitle: DigitalSignatureUtil
articleTitle: DigitalSignatureUtil
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.DigitalSignatures.DigitalSignatureUtil لتوقيع المستندات بسهولة باستخدام توقيعات رقمية آمنة. عزز سلامة مستنداتك اليوم!
type: docs
weight: 610
url: /ar/net/aspose.words.digitalsignatures/digitalsignatureutil/
---
## DigitalSignatureUtil class

يوفر طرقًا لتوقيع المستند.

لمعرفة المزيد، قم بزيارة[العمل مع التوقيعات الرقمية](https://docs.aspose.com/words/net/working-with-digital-signatures/) مقالة توثيقية.

```csharp
public static class DigitalSignatureUtil
```

## طُرق

| اسم | وصف |
| --- | --- |
| static [LoadSignatures](../../aspose.words.digitalsignatures/digitalsignatureutil/loadsignatures/#loadsignatures)(*Stream*) | يقوم بتحميل التوقيعات الرقمية من المستند باستخدام stream. |
| static [LoadSignatures](../../aspose.words.digitalsignatures/digitalsignatureutil/loadsignatures/#loadsignatures_1)(*string*) | يقوم بتحميل التوقيعات الرقمية من المستند. |
| static [RemoveAllSignatures](../../aspose.words.digitalsignatures/digitalsignatureutil/removeallsignatures/#removeallsignatures)(*Stream, Stream*) | يزيل جميع التوقيعات الرقمية من المستند في مجرى المصدر ويكتب المستند غير الموقع في مجرى الوجهة. |
| static [RemoveAllSignatures](../../aspose.words.digitalsignatures/digitalsignatureutil/removeallsignatures/#removeallsignatures_1)(*string, string*) | يزيل جميع التوقيعات الرقمية من ملف المصدر ويكتب الملف غير الموقع إلى ملف الوجهة. |
| static [Sign](../../aspose.words.digitalsignatures/digitalsignatureutil/sign/#sign)(*Stream, Stream, [CertificateHolder](../certificateholder/)*) | يوقع مستند المصدر باستخدام المحدد[`CertificateHolder`](../certificateholder/) مع التوقيع الرقمي ويكتب المستند الموقّع إلى مجرى الوجهة. |
| static [Sign](../../aspose.words.digitalsignatures/digitalsignatureutil/sign/#sign_2)(*string, string, [CertificateHolder](../certificateholder/)*) | يوقع مستند المصدر باستخدام المحدد[`CertificateHolder`](../certificateholder/) مع التوقيع الرقمي ويكتب المستند الموقع إلى ملف الوجهة. |
| static [Sign](../../aspose.words.digitalsignatures/digitalsignatureutil/sign/#sign_1)(*Stream, Stream, [CertificateHolder](../certificateholder/), [SignOptions](../signoptions/)*) | يوقع مستند المصدر باستخدام المحدد[`CertificateHolder`](../certificateholder/) و[`SignOptions`](../signoptions/) مع التوقيع الرقمي ويكتب المستند الموقع إلى مجرى الوجهة. |
| static [Sign](../../aspose.words.digitalsignatures/digitalsignatureutil/sign/#sign_3)(*string, string, [CertificateHolder](../certificateholder/), [SignOptions](../signoptions/)*) | يوقع مستند المصدر باستخدام المحدد[`CertificateHolder`](../certificateholder/) و[`SignOptions`](../signoptions/) مع التوقيع الرقمي ويكتب المستند الموقع إلى ملف الوجهة. |

## ملاحظات

نظرًا لأن التوقيع الرقمي يعمل مع محتوى الملف وليس نموذج كائن المستند، يتم وضع هذه الأساليب في فئة منفصلة.

التنسيقات المدعومة هي: Doc ، Dot ، Docx ، Dotx ، Docm ، Dotm ، Odt ، Ott.

## أمثلة

يوضح كيفية تحميل التوقيعات من مستند موقّع رقميًا.

```csharp
// هناك طريقتان لتحميل مجموعة التوقيعات الرقمية للمستند الموقّع باستخدام فئة DigitalSignatureUtil.
// 1 - تحميل من مستند من نظام ملفات محلي اسم الملف:
DigitalSignatureCollection digitalSignatures = 
    DigitalSignatureUtil.LoadSignatures(MyDir + "Digitally signed.docx");

// إذا كانت هذه المجموعة غير فارغة، فيمكننا التحقق من أن المستند موقّع رقميًا.
Assert.AreEqual(1, digitalSignatures.Count);

// 2 - التحميل من مستند من FileStream:
using (Stream stream = new FileStream(MyDir + "Digitally signed.docx", FileMode.Open))
{
    digitalSignatures = DigitalSignatureUtil.LoadSignatures(stream);
    Assert.AreEqual(1, digitalSignatures.Count);
}
```

يوضح كيفية إزالة التوقيعات الرقمية من مستند موقّع رقميًا.

```csharp
// هناك طريقتان لاستخدام فئة DigitalSignatureUtil لإزالة التوقيعات الرقمية
// من مستند موقّع عن طريق حفظ نسخة غير موقعة منه في مكان آخر في نظام الملفات المحلي.
// 1 - تحديد مواقع كل من المستند الموقع والنسخة غير الموقعة من خلال سلاسل أسماء الملفات:
DigitalSignatureUtil.RemoveAllSignatures(MyDir + "Digitally signed.docx",
    ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromString.docx");

// 2 - تحديد مواقع كل من المستند الموقع والنسخة غير الموقعة من خلال تدفقات الملفات:
using (Stream streamIn = new FileStream(MyDir + "Digitally signed.docx", FileMode.Open))
{
    using (Stream streamOut = new FileStream(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromStream.docx", FileMode.Create))
    {
        DigitalSignatureUtil.RemoveAllSignatures(streamIn, streamOut);
    }
}

// تأكد من أن كلا مستندي الإخراج لا يحتويان على توقيعات رقمية.
Assert.AreEqual(0, DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromString.docx").Count);
Assert.AreEqual(0, DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromStream.docx").Count);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* المجسم [Aspose.Words](../../)
