---
title: License
linktitle: License
articleTitle: License
second_title: Aspose.Words لـ .NET
description: أنشئ وأدر التراخيص بسهولة باستخدام فئة المُنشئ لدينا. بسّط عملية الترخيص لديك وحسّن كفاءتها اليوم!
type: docs
weight: 10
url: /ar/net/aspose.words/license/license/
---
## License constructor

يقوم بتهيئة مثيل جديد لهذه الفئة.

```csharp
public License()
```

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
