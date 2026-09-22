---
title: "Aspose::Words::Fonts::PhysicalFontInfo::get_FullFontName طريقة"
linktitle: "get_FullFontName"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fonts::PhysicalFontInfo::get_FullFontName طريقة. الاسم الكامل للخط في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.fonts/physicalfontinfo/get_fullfontname/
---
## PhysicalFontInfo::get_FullFontName method


الاسم الكامل للخط.

```cpp
System::String Aspose::Words::Fonts::PhysicalFontInfo::get_FullFontName() const
```


## أمثلة



يظهر كيفية سرد الخطوط المتاحة.
```cpp
// قم بتكوين Aspose.Words للحصول على الخطوط من مجلد مخصص، ثم اطبع كل خط متاح.
System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> folderFontSource = System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), true)});

for (auto&& fontInfo : System::IterateOver(folderFontSource[0]->GetAvailableFonts()))
{
    std::cout << "FontFamilyName : " << fontInfo->get_FontFamilyName() << std::endl;
    std::cout << "FullFontName  : " << fontInfo->get_FullFontName() << std::endl;
    std::cout << "Version  : " << fontInfo->get_Version() << std::endl;
    std::cout << "FilePath : " << fontInfo->get_FilePath() << "\n" << std::endl;
}
```

## انظر أيضًا

* Class [PhysicalFontInfo](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
