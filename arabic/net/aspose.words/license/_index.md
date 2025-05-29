---
title: License Class
linktitle: License
articleTitle: License
second_title: Aspose.Words لـ .NET
description: أطلق العنان لإمكانات Aspose.Words الكاملة مع فئة الترخيص لدينا. أدر التراخيص بسهولة لمعالجة مستندات سلسة وتحسين الوظائف.
type: docs
weight: 3870
url: /ar/net/aspose.words/license/
---
## License class

يوفر طرقًا لترخيص المكون.

لمعرفة المزيد، قم بزيارة[الترخيص والاشتراك](https://docs.aspose.com/words/net/licensing/) مقالة توثيقية.

```csharp
public class License
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [License](license/)() | يقوم بتهيئة مثيل جديد لهذه الفئة. |

## طُرق

| اسم | وصف |
| --- | --- |
| [SetLicense](../../aspose.words/license/setlicense/#setlicense)(*Stream*) | يرخص المكون. |
| [SetLicense](../../aspose.words/license/setlicense/#setlicense_1)(*string*) | يرخص المكون. |

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

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
