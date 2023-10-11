---
title: DigitalSignatureUtil.RemoveAllSignatures
second_title: Aspose.Words لمراجع .NET API
description: DigitalSignatureUtil طريقة. إزالة كافة التوقيعات الرقمية من الملف المصدر وكتابة الملف غير الموقع إلى الملف الوجهة.
type: docs
weight: 20
url: /ar/net/aspose.words.digitalsignatures/digitalsignatureutil/removeallsignatures/
---
## RemoveAllSignatures(string, string) {#removeallsignatures_1}

إزالة كافة التوقيعات الرقمية من الملف المصدر وكتابة الملف غير الموقع إلى الملف الوجهة.

التنسيقات التالية متوافقة لإزالة التوقيع الرقمي: DocDotDocxDotxDocmOdtOtt.

```csharp
public static void RemoveAllSignatures(string srcFileName, string dstFileName)
```

### أمثلة

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

* class [DigitalSignatureUtil](../)
* مساحة الاسم [Aspose.Words.DigitalSignatures](../../digitalsignatureutil/)
* المجسم [Aspose.Words](../../../)

---

## RemoveAllSignatures(Stream, Stream) {#removeallsignatures}

إزالة كافة التوقيعات الرقمية من المستند في التدفق المصدر وكتابة المستند غير الموقع إلى التدفق الوجهة.

**ستتم كتابة الإخراج في بداية الدفق وسيتم تحديث حجم الدفق بطول المحتوى.**

التنسيقات التالية متوافقة لإزالة التوقيع الرقمي: DocDotDocxDotxDocmOdtOtt.

```csharp
public static void RemoveAllSignatures(Stream srcStream, Stream dstStream)
```

### أمثلة

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

* class [DigitalSignatureUtil](../)
* مساحة الاسم [Aspose.Words.DigitalSignatures](../../digitalsignatureutil/)
* المجسم [Aspose.Words](../../../)


