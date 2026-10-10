---
title: "Aspose::Words::Fonts::FontInfo::get_Name طريقة"
linktitle: "get_Name"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Fonts::FontInfo::get_Name. يحصل على اسم الخط في C++."
type: docs
weight: 6000
url: /ar/cpp/aspose.words.fonts/fontinfo/get_name/
---
## FontInfo::get_Name method


يحصل على اسم الخط.

```cpp
System::String Aspose::Words::Fonts::FontInfo::get_Name() const
```

## ملاحظات


لا يمكن أن تكون **null**. يمكن أن تكون سلسلة فارغة.

## أمثلة



يعرض كيفية طباعة تفاصيل الخطوط الموجودة في المستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Embedded font.docx");

System::SharedPtr<Aspose::Words::Fonts::FontInfoCollection> allFonts = doc->get_FontInfos();

// اطبع جميع الخطوط المستخدمة وغير المستخدمة في المستند.
for (int32_t i = 0; i < allFonts->get_Count(); i++)
{
    std::cout << System::String::Format(u"Font index #{0}", i) << std::endl;
    std::cout << System::String::Format(u"\tName: {0}", allFonts->idx_get(i)->get_Name()) << std::endl;
    std::cout << System::String::Format(u"\tIs {0}a trueType font", (allFonts->idx_get(i)->get_IsTrueType() ? System::String(u"") : System::String(u"not "))) << std::endl;
}
```

## انظر أيضًا

* Class [FontInfo](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
