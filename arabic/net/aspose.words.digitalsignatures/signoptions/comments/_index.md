---
title: SignOptions.Comments
linktitle: Comments
articleTitle: Comments
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية تعليقات SignOptions لتحسين توقيعك الرقمي بملاحظات مخصصة. حسّن الوضوح والتواصل بسهولة!
type: docs
weight: 20
url: /ar/net/aspose.words.digitalsignatures/signoptions/comments/
---
## SignOptions.Comments property

يحدد التعليقات على التوقيع الرقمي. القيمة الافتراضية هي**سلسلة فارغة**(Empty ).

```csharp
public string Comments { get; set; }
```

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

* class [SignOptions](../)
* مساحة الاسم [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* المجسم [Aspose.Words](../../../)
