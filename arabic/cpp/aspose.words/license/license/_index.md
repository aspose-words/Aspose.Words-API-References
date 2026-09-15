---
title: "Aspose::Words::License::License منشئ"
linktitle: "License"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::License::License منشئ. يقوم بتهيئة نسخة جديدة من هذه الفئة في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words/license/license/
---
## License::License constructor


يُنشئ مثيلًا جديدًا لهذه الفئة.

```cpp
Aspose::Words::License::License()
```


## أمثلة



يوضح كيفية تهيئة ترخيص لـ Aspose.Words باستخدام ملف ترخيص في نظام الملفات المحلي.
```cpp
System::String testLicenseFileName = u"Aspose.Words.Cpp.lic";

// قم بتعيين الترخيص لمنتج Aspose.Words الخاص بنا بتمرير اسم ملف الترخيص الصالح في نظام الملفات المحلي.
System::String licenseFileName = System::IO::Path::Combine(get_LicenseDir(), testLicenseFileName);

auto license = System::MakeObject<Aspose::Words::License>();
license->SetLicense(licenseFileName);

// أنشئ نسخة من ملف الترخيص الخاص بنا في مجلد الثنائيات لتطبيقنا.
System::String licenseCopyFileName = System::IO::Path::Combine(get_AssemblyDir(), testLicenseFileName);
System::IO::File::Copy(licenseFileName, licenseCopyFileName);

// إذا مررنا اسم ملف دون مسار،
// ستبحث الدالة SetLicense في عدة مواقع على نظام الملفات المحلي عن هذا الملف.
// إحدى تلك المواقع ستكون مجلد "bin"، الذي يحتوي على نسخة من ملف الترخيص الخاص بنا.
license->SetLicense(testLicenseFileName);
```

## انظر أيضًا

* Class [License](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
