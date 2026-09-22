---
title: "Aspose::Words::Fonts::FontInfo class"
linktitle: "FontInfo"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fonts::FontInfo class. يحدد معلومات حول خط مستخدم في المستند. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 6000
url: /ar/cpp/aspose.words.fonts/fontinfo/
---
## FontInfo class


يحدد معلومات حول خط مستخدم في المستند. لمعرفة المزيد، زر مقالة الوثائق [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class FontInfo : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_AltName](./get_altname/)() const | يحصل أو يعيّن الاسم البديل للخط. |
| [get_Charset](./get_charset/)() | يحصل أو يعيّن مجموعة الأحرف للخط. |
| [get_EmbeddingLicensingRights](./get_embeddinglicensingrights/)() | يحصل على حقوق ترخيص الخط المدمج. |
| [get_Family](./get_family/)() const | يحصل أو يعيّن عائلة الخط التي ينتمي إليها هذا الخط. |
| [get_IsTrueType](./get_istruetype/)() const | يشير إلى أن هذا الخط هو خط TrueType أو OpenType على عكس الخط النقطي أو الخطي. القيمة الافتراضية هي **true**. |
| [get_Name](./get_name/)() const | يحصل على اسم الخط. |
| [get_Panose](./get_panose/)() const | يحصل على أو يضبط رقم تصنيف الخط PANOSE. |
| [get_Pitch](./get_pitch/)() const | تشير قيمة pitch إلى ما إذا كان الخط ثابت العرض، أو متباعد بنسبية، أو يعتمد على الإعداد الافتراضي. |
| [GetEmbeddedFont](./getembeddedfont/)(Aspose::Words::Fonts::EmbeddedFontFormat, Aspose::Words::Fonts::EmbeddedFontStyle) | يحصل على ملف خط مضمّن محدد. |
| [GetEmbeddedFontAsOpenType](./getembeddedfontasopentype/)(Aspose::Words::Fonts::EmbeddedFontStyle) | يحصل على ملف خط مضمّن بتنسيق OpenType. [Fonts](../) بتنسيق Embedded OpenType يتم تحويله إلى OpenType. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AltName](./set_altname/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Fonts::FontInfo::get_AltName](./get_altname/). |
| [set_Charset](./set_charset/)(int32_t) | مُعيّن لـ [Aspose::Words::Fonts::FontInfo::get_Charset](./get_charset/). |
| [set_Family](./set_family/)(Aspose::Words::Fonts::FontFamily) | مُعيّن لـ [Aspose::Words::Fonts::FontInfo::get_Family](./get_family/). |
| [set_IsTrueType](./set_istruetype/)(bool) | مُعيّن لـ [Aspose::Words::Fonts::FontInfo::get_IsTrueType](./get_istruetype/). |
| [set_Panose](./set_panose/)(const System::ArrayPtr\<uint8_t\>\&) | مُعيّن لـ [Aspose::Words::Fonts::FontInfo::get_Panose](./get_panose/). |
| [set_Pitch](./set_pitch/)(Aspose::Words::Fonts::FontPitch) | مُعيّن لـ [Aspose::Words::Fonts::FontInfo::get_Pitch](./get_pitch/). |
| static [Type](./type/)() |  |
## ملاحظات


لا تقوم بإنشاء مثيلات من هذه الفئة مباشرة. استخدم الخاصية [FontInfos](../../aspose.words/documentbase/get_fontinfos/) للوصول إلى مجموعة الخطوط المعرفة في المستند.

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

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
