---
title: "فئة Aspose::Words::FontSubstitutionWarningInfo"
linktitle: "FontSubstitutionWarningInfo"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::FontSubstitutionWarningInfo فئة. تحتوي على معلومات حول تحذير استبدال الخط الذي أصدرته Aspose.Words أثناء تحميل أو حفظ المستند في C++."
type: docs
weight: 29500
url: /ar/cpp/aspose.words/fontsubstitutionwarninginfo/
---
## FontSubstitutionWarningInfo class


يحتوي على معلومات حول تحذير استبدال الخط الذي أصدره Aspose.Words أثناء تحميل أو حفظ المستند.

```cpp
class FontSubstitutionWarningInfo : public Aspose::Words::WarningInfo
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_Description](../warninginfo/get_description/)() const | يعيد وصف التحذير. |
| [get_Reason](./get_reason/)() const | سبب استبدال [Font](../font/). |
| [get_RequestedBold](./get_requestedbold/)() const | يشير إلى ما إذا كان النمط الغامق مطلوبًا. |
| [get_RequestedFamilyName](./get_requestedfamilyname/)() const | اسم عائلة الخط المطلوب. |
| [get_RequestedItalic](./get_requesteditalic/)() const | يشير إلى ما إذا كان النمط المائل مطلوبًا. |
| [get_ResolvedFont](./get_resolvedfont/)() const | الخط المُستبدَل. |
| [get_Source](../warninginfo/get_source/)() const | يعيد مصدر التحذير. |
| [get_WarningType](../warninginfo/get_warningtype/)() const | يعيد نوع التحذير. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## أمثلة



يوضح كيفية الحصول على معلومات إضافية حول استبدال الخط.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto callback = System::MakeObject<Aspose::Words::WarningInfoCollection>();
doc->set_WarningCallback(callback);

auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
fontSettings->get_SubstitutionSettings()->get_DefaultFontSubstitution()->set_DefaultFontName(u"Arial");
fontSettings->SetFontsFolder(get_FontsDir(), false);
fontSettings->get_SubstitutionSettings()->get_TableSubstitution()->AddSubstitutes(u"Arial", System::MakeArray<System::String>({u"Arvo", u"Slab"}));

doc->set_FontSettings(fontSettings);
doc->Save(get_ArtifactsDir() + u"FontSettings.SubstitutionWarnings.pdf");

auto warningInfo = System::ExplicitCast<Aspose::Words::FontSubstitutionWarningInfo>(callback->idx_get(0));
ASSERT_EQ(Aspose::Words::WarningSource::Layout, warningInfo->get_Source());
ASSERT_EQ(Aspose::Words::WarningType::FontSubstitution, warningInfo->get_WarningType());
ASSERT_EQ(Aspose::Words::FontSubstitutionReason::TableSubstitutionRule, warningInfo->get_Reason());
ASSERT_EQ(u"Font \'Arial\' has not been found. Using \'Arvo\' font instead. Reason: table substitution.", warningInfo->get_Description());
ASSERT_TRUE(warningInfo->get_RequestedBold());
ASSERT_FALSE(warningInfo->get_RequestedItalic());
ASSERT_EQ(u"Arial", warningInfo->get_RequestedFamilyName());
```

## انظر أيضًا

* Class [WarningInfo](../warninginfo/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
