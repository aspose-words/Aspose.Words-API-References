---
title: License.SetLicense
linktitle: SetLicense
articleTitle: SetLicense
second_title: Aspose.Words لـ .NET
description: License SetLicense طريقة. ترخيص المكون في C#.
type: docs
weight: 20
url: /ar/net/aspose.words/license/setlicense/
---
## SetLicense(*string*) {#setlicense_1}

ترخيص المكون.

```csharp
public void SetLicense(string licenseName)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| licenseName | String | يمكن أن يكون اسم ملف كاملاً أو قصيرًا أو اسمًا لمورد مضمن. استخدم سلسلة فارغة للتبديل إلى وضع التقييم. |

## ملاحظات

يحاول العثور على الترخيص في المواقع التالية:

1. المسار الصريح.

2. المجلد الذي يحتوي على مجموعة مكونات Aspose.

3. المجلد الذي يحتوي على مجموعة الاستدعاء الخاصة بالعميل.

4. المجلد الذي يحتوي على مجموعة الإدخال (بدء التشغيل).

5. مورد مضمن في تجميع الاستدعاء الخاص بالعميل.

**ملحوظة:**في .NET Compact Framework، يحاول العثور على الترخيص في هذه المواقع فقط:

1. المسار الصريح.

2. مورد مضمن في تجميع الاستدعاء الخاص بالعميل.

## أمثلة

يوضح كيفية تهيئة ترخيص Aspose.Words باستخدام ملف ترخيص في نظام الملفات المحلي.

```csharp
// قم بتعيين الترخيص لمنتج Aspose.Words الخاص بنا عن طريق تمرير اسم ملف نظام الملفات المحلي لملف ترخيص صالح.
string licenseFileName = Path.Combine(LicenseDir, "Aspose.Words.NET.lic");

License license = new License();
license.SetLicense(licenseFileName);

// قم بإنشاء نسخة من ملف الترخيص الخاص بنا في مجلد الثنائيات الخاص بتطبيقنا.
string licenseCopyFileName = Path.Combine(AssemblyDir, "Aspose.Words.NET.lic");
File.Copy(licenseFileName, licenseCopyFileName);

// إذا مررنا اسم ملف بدون مسار،
// سيبحث SetLicense في العديد من مواقع نظام الملفات المحلية لهذا الملف.
// سيكون أحد هذه المواقع هو المجلد "bin"، الذي يحتوي على نسخة من ملف الترخيص الخاص بنا.
license.SetLicense("Aspose.Words.NET.lic");
```

### أنظر أيضا

* class [License](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## SetLicense(*Stream*) {#setlicense}

ترخيص المكون.

```csharp
public void SetLicense(Stream stream)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| stream | Stream | دفق يحتوي على الترخيص. |

## ملاحظات

استخدم هذه الطريقة لتحميل ترخيص من الدفق.

## أمثلة

يوضح كيفية تهيئة ترخيص Aspose.Words من التدفق.

```csharp
// قم بتعيين الترخيص لمنتج Aspose.Words الخاص بنا عن طريق تمرير دفق لملف ترخيص صالح في نظام الملفات المحلي الخاص بنا.
using (Stream myStream = File.OpenRead(Path.Combine(LicenseDir, "Aspose.Words.NET.lic")))
{
    License license = new License();
    license.SetLicense(myStream);
}
```

### أنظر أيضا

* class [License](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
