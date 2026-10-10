---
title: "Aspose::Words::Fonts::FontInfo::get_IsTrueType طريقة"
linktitle: "get_IsTrueType"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fonts::FontInfo::get_IsTrueType طريقة. يشير إلى أن هذا الخط هو خط TrueType أو OpenType على عكس الخط النقطي أو الخط المتجه. القيمة الافتراضية هي true في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words.fonts/fontinfo/get_istruetype/
---
## FontInfo::get_IsTrueType method


يشير إلى أن هذا الخط هو خط TrueType أو OpenType على عكس الخط النقطي أو الخطي. القيمة الافتراضية هي **true**.

```cpp
bool Aspose::Words::Fonts::FontInfo::get_IsTrueType() const
```


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
