---
title: DigitalSignatureUtil.RemoveAllSignatures
linktitle: RemoveAllSignatures
articleTitle: RemoveAllSignatures
second_title: Aspose.Words لـ .NET
description: أزل جميع التوقيعات الرقمية بسهولة باستخدام طريقة RemoveAllSignatures من DigitalSignatureUtil. حوّل ملفاتك الموقعة إلى نسخ نظيفة وغير موقعة بسهولة!
type: docs
weight: 20
url: /ar/net/aspose.words.digitalsignatures/digitalsignatureutil/removeallsignatures/
---
## RemoveAllSignatures(*string, string*) {#removeallsignatures_1}

يزيل جميع التوقيعات الرقمية من ملف المصدر ويكتب الملف غير الموقع إلى ملف الوجهة.

التنسيقات التالية متوافقة لإزالة التوقيع الرقمي: Doc ، Dot ، Docx ، Dotx ، Docm ، Dotm ، Odt ، Ott.

```csharp
public static void RemoveAllSignatures(string srcFileName, string dstFileName)
```

## أمثلة

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

* class [DigitalSignatureUtil](../)
* مساحة الاسم [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* المجسم [Aspose.Words](../../../)

---

## RemoveAllSignatures(*Stream, Stream*) {#removeallsignatures}

يزيل جميع التوقيعات الرقمية من المستند في مجرى المصدر ويكتب المستند غير الموقع في مجرى الوجهة.

**سيتم كتابة الإخراج في بداية التدفق وسيتم تحديث حجم التدفق بطول المحتوى.**

التنسيقات التالية متوافقة لإزالة التوقيع الرقمي: Doc ، Dot ، Docx ، Dotx ، Docm ، Dotm ، Odt ، Ott.

```csharp
public static void RemoveAllSignatures(Stream srcStream, Stream dstStream)
```

## أمثلة

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

* class [DigitalSignatureUtil](../)
* مساحة الاسم [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* المجسم [Aspose.Words](../../../)
