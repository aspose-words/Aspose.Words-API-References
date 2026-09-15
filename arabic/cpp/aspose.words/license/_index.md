---
title: "فئة Aspose::Words::License"
linktitle: "License"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::License. توفر طرقًا لترخيص المكوّن. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 39000
url: /ar/cpp/aspose.words/license/
---
## License class


يوفر طرقًا لترخيص المكوّن. لمعرفة المزيد، زر مقالة الوثائق [Licensing and Subscription](https://docs.aspose.com/words/cpp/licensing/)

```cpp
class License : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [License](./license/)() | يُنشئ مثيلًا جديدًا لهذه الفئة. |
| [SetLicense](./setlicense/)(const System::String\&) | يرخص المكوّن. |
| [SetLicense](./setlicense/)(const System::SharedPtr\<System::IO::Stream\>\&) | يرخص المكوّن. |
| [SetLicense](./setlicense/)(std::basic_istream\<CharType, Traits\>\&) |  |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
