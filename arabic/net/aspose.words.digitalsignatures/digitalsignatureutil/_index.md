---
title: DigitalSignatureUtil Class
linktitle: DigitalSignatureUtil
articleTitle: DigitalSignatureUtil
second_title: Aspose.Words لـ .NET
description: Aspose.Words.DigitalSignatures.DigitalSignatureUtil فصل. يوفر طرقًا لتوقيع المستند في C#.
type: docs
weight: 410
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
| static [LoadSignatures](../../aspose.words.digitalsignatures/digitalsignatureutil/loadsignatures/#loadsignatures)(*Stream*) | تحميل التوقيعات الرقمية من المستند باستخدام الدفق. |
| static [LoadSignatures](../../aspose.words.digitalsignatures/digitalsignatureutil/loadsignatures/#loadsignatures_1)(*string*) | تحميل التوقيعات الرقمية من المستند. |
| static [RemoveAllSignatures](../../aspose.words.digitalsignatures/digitalsignatureutil/removeallsignatures/#removeallsignatures)(*Stream, Stream*) | إزالة كافة التوقيعات الرقمية من المستند في التدفق المصدر وكتابة المستند غير الموقع إلى التدفق الوجهة. |
| static [RemoveAllSignatures](../../aspose.words.digitalsignatures/digitalsignatureutil/removeallsignatures/#removeallsignatures_1)(*string, string*) | إزالة كافة التوقيعات الرقمية من الملف المصدر وكتابة الملف غير الموقع إلى الملف الوجهة. |
| static [Sign](../../aspose.words.digitalsignatures/digitalsignatureutil/sign/#sign)(*Stream, Stream, [CertificateHolder](../certificateholder/)*) | يوقع المستند المصدر باستخدام المحدد[`CertificateHolder`](../certificateholder/)باستخدام التوقيع الرقمي ويكتب المستند الموقع إلى التدفق الوجهة. |
| static [Sign](../../aspose.words.digitalsignatures/digitalsignatureutil/sign/#sign_2)(*string, string, [CertificateHolder](../certificateholder/)*) | يوقع المستند المصدر باستخدام المحدد[`CertificateHolder`](../certificateholder/) باستخدام التوقيع الرقمي ويكتب المستند الموقع إلى الملف الوجهة. |
| static [Sign](../../aspose.words.digitalsignatures/digitalsignatureutil/sign/#sign_1)(*Stream, Stream, [CertificateHolder](../certificateholder/), [SignOptions](../signoptions/)*) | يوقع المستند المصدر باستخدام المحدد[`CertificateHolder`](../certificateholder/) و[`SignOptions`](../signoptions/) مع التوقيع الرقمي ويكتب المستند الموقع إلى التدفق الوجهة. |
| static [Sign](../../aspose.words.digitalsignatures/digitalsignatureutil/sign/#sign_3)(*string, string, [CertificateHolder](../certificateholder/), [SignOptions](../signoptions/)*) | يوقع المستند المصدر باستخدام المحدد[`CertificateHolder`](../certificateholder/) و[`SignOptions`](../signoptions/) مع التوقيع الرقمي ويكتب المستند الموقع إلى الملف الوجهة. |

## ملاحظات

وبما أن التوقيع الرقمي يعمل مع محتوى الملف بدلاً من نموذج كائن المستند، فقد تم وضع هذه الأساليب في فئة منفصلة.

التنسيقات المدعومة هيDoc وDocx.

## أمثلة

يوضح كيفية تحميل التوقيعات من مستند موقع رقميًا.

```csharp
// هناك طريقتان لتحميل مجموعة التوقيعات الرقمية الخاصة بالمستند الموقع باستخدام فئة DigitalSignatureUtil.
// 1 - التحميل من مستند من اسم ملف نظام ملفات محلي:
DigitalSignatureCollection digitalSignatures = 
    DigitalSignatureUtil.LoadSignatures(MyDir + "Digitally signed.docx");

// إذا كانت هذه المجموعة غير فارغة، فيمكننا التحقق من توقيع المستند رقميًا.
Assert.AreEqual(1, digitalSignatures.Count);

// 2 - التحميل من مستند من FileStream:
using (Stream stream = new FileStream(MyDir + "Digitally signed.docx", FileMode.Open))
{
    digitalSignatures = DigitalSignatureUtil.LoadSignatures(stream);
    Assert.AreEqual(1, digitalSignatures.Count);
}
```

يوضح كيفية إزالة التوقيعات الرقمية من مستند موقع رقميًا.

```csharp
// هناك طريقتان لاستخدام فئة DigitalSignatureUtil لإزالة التوقيعات الرقمية
// من مستند موقع عن طريق حفظ نسخة غير موقعة منه في مكان آخر في نظام الملفات المحلي.
// 1 - تحديد موقع كل من المستند الموقع والنسخة غير الموقعة من خلال سلاسل اسم الملف:
DigitalSignatureUtil.RemoveAllSignatures(MyDir + "Digitally signed.docx",
    ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromString.docx");

// 2 - تحديد موقع كل من المستند الموقع والنسخة غير الموقعة من خلال تدفقات الملفات:
using (Stream streamIn = new FileStream(MyDir + "Digitally signed.docx", FileMode.Open))
{
    using (Stream streamOut = new FileStream(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromStream.docx", FileMode.Create))
    {
        DigitalSignatureUtil.RemoveAllSignatures(streamIn, streamOut);
    }
}

// تحقق من أن كلا مستندي الإخراج لدينا لا يحتويان على توقيعات رقمية.
Assert.That(DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromString.docx"), Is.Empty);
Assert.That(DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromStream.docx"), Is.Empty);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* المجسم [Aspose.Words](../../)
