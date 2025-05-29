---
title: DigitalSignatureUtil.LoadSignatures
linktitle: LoadSignatures
articleTitle: LoadSignatures
second_title: Aspose.Words لـ .NET
description: حمّل التوقيعات الرقمية من مستنداتك بسهولة باستخدام طريقة DigitalSignatureUtil LoadSignatures. حسّن سير عملك اليوم!
type: docs
weight: 10
url: /ar/net/aspose.words.digitalsignatures/digitalsignatureutil/loadsignatures/
---
## LoadSignatures(*string*) {#loadsignatures_1}

يقوم بتحميل التوقيعات الرقمية من المستند.

```csharp
public static DigitalSignatureCollection LoadSignatures(string fileName)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fileName | String | المسار إلى المستند. |

### قيمة الإرجاع

مجموعة من التوقيعات الرقمية. تُرجع المجموعة فارغة إذا لم يكن الملف مُوقّعًا.

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

* class [DigitalSignatureCollection](../../digitalsignaturecollection/)
* class [DigitalSignatureUtil](../)
* مساحة الاسم [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* المجسم [Aspose.Words](../../../)

---

## LoadSignatures(*Stream*) {#loadsignatures}

يقوم بتحميل التوقيعات الرقمية من المستند باستخدام stream.

```csharp
public static DigitalSignatureCollection LoadSignatures(Stream stream)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| stream | Stream | البث مع المستند. |

### قيمة الإرجاع

مجموعة من التوقيعات الرقمية. تُرجع المجموعة فارغة إذا لم يكن الملف مُوقّعًا.

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

### أنظر أيضا

* class [DigitalSignatureCollection](../../digitalsignaturecollection/)
* class [DigitalSignatureUtil](../)
* مساحة الاسم [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* المجسم [Aspose.Words](../../../)
