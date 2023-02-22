---
title: SignOptions.Comments
second_title: Aspose.Words لمراجع .NET API
description: SignOptions ملكية. يحدد التعليقات على التوقيع الرقمي. القيمة الافتراضية هي سلسلة فارغة Empty  .
type: docs
weight: 20
url: /ar/net/aspose.words.digitalsignatures/signoptions/comments/
---
## SignOptions.Comments property

يحدد التعليقات على التوقيع الرقمي. القيمة الافتراضية هي **سلسلة فارغة** (Empty ) .

```csharp
public string Comments { get; set; }
```

### أمثلة

يوضح كيفية توقيع المستندات رقميًا.

```csharp
// أنشئ شهادة X.509 من متجر PKCS # 12 ، والتي يجب أن تحتوي على مفتاح خاص.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// أنشئ تعليقًا وتاريخًا سيتم تطبيقه بتوقيعنا الرقمي الجديد.
SignOptions signOptions = new SignOptions
{
    Comments = "My comment", 
    SignTime = DateTime.Now
};

// خذ مستندًا غير موقع من نظام الملفات المحلي عبر تدفق ملف ،
// ثم أنشئ نسخة موقعة منه يحددها اسم ملف تدفق ملف الإخراج.
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


