---
title: DigitalSignatureUtil.LoadSignatures
linktitle: LoadSignatures
articleTitle: LoadSignatures
second_title: Aspose.Words لـ .NET
description: DigitalSignatureUtil LoadSignatures طريقة. تحميل التوقيعات الرقمية من المستند في C#.
type: docs
weight: 10
url: /ar/net/aspose.words.digitalsignatures/digitalsignatureutil/loadsignatures/
---
## LoadSignatures(*string*) {#loadsignatures_1}

تحميل التوقيعات الرقمية من المستند.

```csharp
public static DigitalSignatureCollection LoadSignatures(string fileName)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fileName | String | المسار إلى الوثيقة. |

### قيمة الإرجاع

مجموعة من التوقيعات الرقمية. إرجاع مجموعة فارغة إذا لم يتم توقيع الملف.

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

* class [DigitalSignatureCollection](../../digitalsignaturecollection/)
* class [DigitalSignatureUtil](../)
* مساحة الاسم [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* المجسم [Aspose.Words](../../../)

---

## LoadSignatures(*Stream*) {#loadsignatures}

تحميل التوقيعات الرقمية من المستند باستخدام الدفق.

```csharp
public static DigitalSignatureCollection LoadSignatures(Stream stream)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| stream | Stream | الدفق مع المستند. |

### قيمة الإرجاع

مجموعة من التوقيعات الرقمية. إرجاع مجموعة فارغة إذا لم يتم توقيع الملف.

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

### أنظر أيضا

* class [DigitalSignatureCollection](../../digitalsignaturecollection/)
* class [DigitalSignatureUtil](../)
* مساحة الاسم [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* المجسم [Aspose.Words](../../../)
