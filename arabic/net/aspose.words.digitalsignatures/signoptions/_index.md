---
title: SignOptions Class
linktitle: SignOptions
articleTitle: SignOptions
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.DigitalSignatures.SignOptions لتخصيص عملية توقيع المستندات الخاصة بك باستخدام خيارات مرنة وآمنة لتحسين سير العمل.
type: docs
weight: 620
url: /ar/net/aspose.words.digitalsignatures/signoptions/
---
## SignOptions class

يسمح بتحديد خيارات توقيع المستند.

لمعرفة المزيد، قم بزيارة[العمل مع التوقيعات الرقمية](https://docs.aspose.com/words/net/working-with-digital-signatures/) مقالة توثيقية.

```csharp
public class SignOptions
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [SignOptions](signoptions/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [Comments](../../aspose.words.digitalsignatures/signoptions/comments/) { get; set; } | يحدد التعليقات على التوقيع الرقمي. القيمة الافتراضية هي**سلسلة فارغة**(Empty ). |
| [DecryptionPassword](../../aspose.words.digitalsignatures/signoptions/decryptionpassword/) { get; set; } | كلمة المرور لفك تشفير المستند المصدر. القيمة الافتراضية هي**سلسلة فارغة** (Empty ). |
| [ProviderId](../../aspose.words.digitalsignatures/signoptions/providerid/) { get; set; } | يحدد معرف فئة موفر التوقيع. القيمة الافتراضية هي**فارغ (كل الأصفار) معرف الدليل** . |
| [SignatureLineId](../../aspose.words.digitalsignatures/signoptions/signaturelineid/) { get; set; } | معرف سطر التوقيع. القيمة الافتراضية هي**فارغ (كل الأصفار) معرف الدليل** . |
| [SignatureLineImage](../../aspose.words.digitalsignatures/signoptions/signaturelineimage/) { get; set; } | الصورة التي سيتم عرضها في المرتبطة[`SignatureLine`](../../aspose.words.drawing/signatureline/) . القيمة الافتراضية هي`باطل` . |
| [SignTime](../../aspose.words.digitalsignatures/signoptions/signtime/) { get; set; } | تاريخ التوقيع. القيمة الافتراضية هي**الوقت الحالي** (Now) |
| [XmlDsigLevel](../../aspose.words.digitalsignatures/signoptions/xmldsiglevel/) { get; set; } | يحدد مستوى التوقيع الرقمي استنادًا إلى معيار XML-DSig. القيمة الافتراضية هيXmlDSig . |

## أمثلة

يوضح كيفية التوقيع الرقمي على المستندات.

```csharp
// قم بإنشاء شهادة X.509 من متجر PKCS#12، والتي يجب أن تحتوي على مفتاح خاص.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// قم بإنشاء تعليق وتاريخ سيتم تطبيقهما باستخدام توقيعنا الرقمي الجديد.
SignOptions signOptions = new SignOptions
{
    Comments = "My comment", 
    SignTime = DateTime.Now
};

// أخذ مستند غير موقع من نظام الملفات المحلي عبر مجرى ملف،
// ثم قم بإنشاء نسخة موقعة منه يتم تحديدها من خلال اسم ملف مجرى ملف الإخراج.
using (Stream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (Stream streamOut = new FileStream(ArtifactsDir + "DigitalSignatureUtil.SignDocument.docx", FileMode.OpenOrCreate))
    {
        DigitalSignatureUtil.Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* المجسم [Aspose.Words](../../)
