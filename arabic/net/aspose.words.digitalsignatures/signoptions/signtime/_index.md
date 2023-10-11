---
title: SignOptions.SignTime
second_title: Aspose.Words لمراجع .NET API
description: SignOptions ملكية. تاريخ التوقيع. القيمة الافتراضية هي الوقت الحالي Now.
type: docs
weight: 70
url: /ar/net/aspose.words.digitalsignatures/signoptions/signtime/
---
## SignOptions.SignTime property

تاريخ التوقيع. القيمة الافتراضية هي **الوقت الحالي** (Now).

```csharp
public DateTime SignTime { get; set; }
```

### أمثلة

يوضح كيفية توقيع المستندات رقميًا.

```csharp
// أنشئ شهادة X.509 من متجر PKCS#12، والتي يجب أن تحتوي على مفتاح خاص.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// قم بإنشاء تعليق وتاريخ سيتم تطبيقه مع توقيعنا الرقمي الجديد.
SignOptions signOptions = new SignOptions
{
    Comments = "My comment", 
    SignTime = DateTime.Now
};

// خذ مستندًا غير موقع من نظام الملفات المحلي عبر دفق الملفات،
// ثم قم بإنشاء نسخة موقعة منه يحددها اسم ملف دفق ملف الإخراج.
using (Stream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (Stream streamOut = new FileStream(ArtifactsDir + "DigitalSignatureUtil.SignDocument.docx", FileMode.OpenOrCreate))
    {
        DigitalSignatureUtil.Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```

### أنظر أيضا

* class [SignOptions](../)
* مساحة الاسم [Aspose.Words.DigitalSignatures](../../signoptions/)
* المجسم [Aspose.Words](../../../)


