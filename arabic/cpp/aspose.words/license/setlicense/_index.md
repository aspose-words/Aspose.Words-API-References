---
title: "طريقة Aspose::Words::License::SetLicense"
linktitle: "SetLicense"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::License::SetLicense. تقوم بترخيص المكوّن في لغة C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words/license/setlicense/
---
## License::SetLicense(const System::SharedPtr\<System::IO::Stream\>\&) method


يرخص المكوّن.

```cpp
void Aspose::Words::License::SetLicense(const System::SharedPtr<System::IO::Stream> &stream)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| تدفق | const System::SharedPtr\<System::IO::Stream\>\& | دفق يحتوي على الترخيص. |
## ملاحظات


استخدم هذه الطريقة لتحميل الترخيص من دفق.

## أمثلة



يظهر كيفية تهيئة ترخيص لـ Aspose.Words من دفق.
```cpp
System::String testLicenseFileName = u"Aspose.Words.Cpp.lic";
// قم بتعيين الترخيص لمنتج Aspose.Words الخاص بنا عن طريق تمرير دفق لملف ترخيص صالح في نظام الملفات المحلي.
{
    System::SharedPtr<System::IO::Stream> myStream = System::IO::File::OpenRead(System::IO::Path::Combine(get_LicenseDir(), testLicenseFileName));
    auto license = System::MakeObject<Aspose::Words::License>();
    license->SetLicense(myStream);
}
```

## انظر أيضًا

* Class [License](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## License::SetLicense(const System::String\&) method


يرخص المكوّن.

```cpp
void Aspose::Words::License::SetLicense(const System::String &licenseName)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| licenseName | const System::String\& | يمكن أن يكون اسم ملف كامل أو مختصر. استخدم سلسلة فارغة للتبديل إلى وضع التقييم. |
## ملاحظات


يحاول العثور على الترخيص في المواقع التالية:

1. مسار صريح.
1. المجلد الذي يحتوي على مكتبة Aspose.Words.
1. المجلد الذي يحتوي على تطبيق العميل.



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
## License::SetLicense(std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> void Aspose::Words::License::SetLicense(std::basic_istream<CharType, Traits> &stream)
```

## انظر أيضًا

* Class [License](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
