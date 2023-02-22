---
title: DigitalSignatureUtil.LoadSignatures
second_title: Aspose.Words لمراجع .NET API
description: DigitalSignatureUtil طريقة. تحميل التوقيعات الرقمية من المستند.
type: docs
weight: 10
url: /ar/net/aspose.words.digitalsignatures/digitalsignatureutil/loadsignatures/
---
## LoadSignatures(string) {#loadsignatures_1}

تحميل التوقيعات الرقمية من المستند.

```csharp
public static DigitalSignatureCollection LoadSignatures(string fileName)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fileName | String | مسار الوثيقة. |

### قيمة الإرجاع

مجموعة التوقيعات الرقمية. إرجاع مجموعة فارغة إذا لم يتم توقيع الملف.

### أمثلة

يوضح كيفية تحميل التوقيعات من مستند موقع رقميًا.

```csharp
// هناك طريقتان لتحميل مجموعة التوقيعات الرقمية الخاصة بوثيقة موقعة باستخدام فئة DigitalSignatureUtil.
// 1 - تحميل من مستند من اسم ملف نظام ملفات محلي:
DigitalSignatureCollection digitalSignatures = 
    DigitalSignatureUtil.LoadSignatures(MyDir + "Digitally signed.docx");

// إذا كانت هذه المجموعة غير فارغة ، فيمكننا التحقق من توقيع المستند رقميًا.
Assert.AreEqual(1, digitalSignatures.Count);

// 2 - تحميل من مستند من FileStream:
using (Stream stream = new FileStream(MyDir + "Digitally signed.docx", FileMode.Open))
{
    digitalSignatures = DigitalSignatureUtil.LoadSignatures(stream);
    Assert.AreEqual(1, digitalSignatures.Count);
}
```

يوضح كيفية إزالة التواقيع الرقمية من مستند موقع رقميًا.

```csharp
// هناك طريقتان لاستخدام فئة DigitalSignatureUtil لإزالة التوقيعات الرقمية
// من مستند موقع عن طريق حفظ نسخة غير موقعة منه في مكان آخر في نظام الملفات المحلي.
// 1 - تحديد مواقع كل من المستند الموقع والنسخة غير الموقعة بواسطة سلاسل اسم الملف:
DigitalSignatureUtil.RemoveAllSignatures(MyDir + "Digitally signed.docx",
    ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromString.docx");

// 2 - تحديد مواقع كل من المستند الموقع والنسخة غير الموقعة بواسطة تدفقات الملفات:
using (Stream streamIn = new FileStream(MyDir + "Digitally signed.docx", FileMode.Open))
{
    using (Stream streamOut = new FileStream(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromStream.docx", FileMode.Create))
    {
        DigitalSignatureUtil.RemoveAllSignatures(streamIn, streamOut);
    }
}

// تحقق من أن كلا من وثيقتنا المخرجة لا تحتوي على توقيعات رقمية.
Assert.That(DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromString.docx"), Is.Empty);
Assert.That(DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromStream.docx"), Is.Empty);
```

### أنظر أيضا

* class [DigitalSignatureCollection](../../digitalsignaturecollection/)
* class [DigitalSignatureUtil](../)
* مساحة الاسم [Aspose.Words.DigitalSignatures](../../digitalsignatureutil/)
* المجسم [Aspose.Words](../../../)

---

## LoadSignatures(Stream) {#loadsignatures}

تحميل التوقيعات الرقمية من المستند باستخدام الدفق.

```csharp
public static DigitalSignatureCollection LoadSignatures(Stream stream)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| stream | Stream | دفق مع المستند. |

### قيمة الإرجاع

مجموعة التوقيعات الرقمية. إرجاع مجموعة فارغة إذا لم يتم توقيع الملف.

### أمثلة

يوضح كيفية تحميل التوقيعات من مستند موقع رقميًا.

```csharp
// هناك طريقتان لتحميل مجموعة التوقيعات الرقمية الخاصة بوثيقة موقعة باستخدام فئة DigitalSignatureUtil.
// 1 - تحميل من مستند من اسم ملف نظام ملفات محلي:
DigitalSignatureCollection digitalSignatures = 
    DigitalSignatureUtil.LoadSignatures(MyDir + "Digitally signed.docx");

// إذا كانت هذه المجموعة غير فارغة ، فيمكننا التحقق من توقيع المستند رقميًا.
Assert.AreEqual(1, digitalSignatures.Count);

// 2 - تحميل من مستند من FileStream:
using (Stream stream = new FileStream(MyDir + "Digitally signed.docx", FileMode.Open))
{
    digitalSignatures = DigitalSignatureUtil.LoadSignatures(stream);
    Assert.AreEqual(1, digitalSignatures.Count);
}
```

### أنظر أيضا

* class [DigitalSignatureCollection](../../digitalsignaturecollection/)
* class [DigitalSignatureUtil](../)
* مساحة الاسم [Aspose.Words.DigitalSignatures](../../digitalsignatureutil/)
* المجسم [Aspose.Words](../../../)


