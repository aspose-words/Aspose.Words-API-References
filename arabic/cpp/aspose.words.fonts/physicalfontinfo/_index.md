---
title: "Aspose::Words::Fonts::PhysicalFontInfo فئة"
linktitle: "PhysicalFontInfo"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fonts::PhysicalFontInfo فئة. يحدد معلومات حول الخط الفعلي المتاح لمحرك خطوط Aspose.Words. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 15000
url: /ar/cpp/aspose.words.fonts/physicalfontinfo/
---
## PhysicalFontInfo class


يحدد معلومات حول الخط الفيزيائي المتاح لمحرك خطوط Aspose.Words. لمزيد من المعلومات، قم بزيارة مقالة الوثائق [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class PhysicalFontInfo : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_EmbeddingLicensingRights](./get_embeddinglicensingrights/)() const | تضمين حقوق الترخيص للخط. |
| [get_FilePath](./get_filepath/)() const | مسار ملف الخط إذا كان موجودًا. |
| [get_FontFamilyName](./get_fontfamilyname/)() const | اسم عائلة الخط. |
| [get_FullFontName](./get_fullfontname/)() const | الاسم الكامل للخط. |
| [get_Version](./get_version/)() const | سلسلة إصدار الخط. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
