---
title: License.SetLicense
linktitle: SetLicense
articleTitle: SetLicense
second_title: Aspose.Words لـ .NET
description: رخّص مكوناتك بسهولة باستخدام طريقة SetLicense. تمتع بكامل وظائف مشروعك اليوم وعزّز إمكاناته!
type: docs
weight: 20
url: /ar/net/aspose.words/license/setlicense/
---
## SetLicense(*string*) {#setlicense_1}

يرخص المكون.

```csharp
public void SetLicense(string licenseName)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| licenseName | String | يمكن أن يكون اسم ملف كامل أو قصير أو اسم مورد مضمن. استخدم سلسلة فارغة للتبديل إلى وضع التقييم. |

## ملاحظات

يحاول العثور على الترخيص في المواقع التالية:

1. المسار الصريح.

2. المجلد الذي يحتوي على مجموعة مكونات Aspose.

3. المجلد الذي يحتوي على مجموعة استدعاء العميل.

4. المجلد الذي يحتوي على تجميع الإدخالات (بدء التشغيل).

5. مورد مضمن في تجميع الاستدعاء الخاص بالعميل.

**ملحوظة:**في .NET Compact Framework، حاول العثور على الترخيص فقط في هذه المواقع:

1. المسار الصريح.

2. مورد مضمن في تجميع الاستدعاء الخاص بالعميل.

## أمثلة

يوضح كيفية تهيئة ترخيص لـ Aspose.Words باستخدام ملف ترخيص في نظام الملفات المحلي.

```csharp
// قم بتعيين الترخيص لمنتج Aspose.Words الخاص بنا عن طريق تمرير اسم ملف نظام الملفات المحلي لملف ترخيص صالح.
string licenseFileName = Path.Combine(LicenseDir, "Aspose.Words.NET.lic");

License license = new License();
license.SetLicense(licenseFileName);

// قم بإنشاء نسخة من ملف الترخيص الخاص بنا في مجلد الملفات الثنائية في تطبيقنا.
string licenseCopyFileName = Path.Combine(AssemblyDir, "Aspose.Words.NET.lic");
File.Copy(licenseFileName, licenseCopyFileName);

// إذا مررنا اسم الملف بدون مسار،
// سوف يقوم SetLicense بالبحث في عدة مواقع لنظام الملفات المحلي عن هذا الملف.
// سيكون أحد هذه المواقع هو مجلد "bin"، الذي يحتوي على نسخة من ملف الترخيص الخاص بنا.
license.SetLicense("Aspose.Words.NET.lic");
```

### أنظر أيضا

* class [License](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## SetLicense(*Stream*) {#setlicense}

يرخص المكون.

```csharp
public void SetLicense(Stream stream)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| stream | Stream | تيار يحتوي على الترخيص. |

## ملاحظات

استخدم هذه الطريقة لتحميل ترخيص من مجرى.

## أمثلة

يوضح كيفية تهيئة ترخيص لـ Aspose.Words من مجرى.

```csharp
// قم بتعيين الترخيص لمنتج Aspose.Words الخاص بنا عن طريق تمرير مجرى لملف ترخيص صالح في نظام الملفات المحلي الخاص بنا.
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
