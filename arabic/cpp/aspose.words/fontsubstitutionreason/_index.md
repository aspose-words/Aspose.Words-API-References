---
title: "Aspose::Words::FontSubstitutionReason عدد"
linktitle: "FontSubstitutionReason"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::FontSubstitutionReason عدد. يحدد سبب استبدال الخط في C++."
type: docs
weight: 89500
url: /ar/cpp/aspose.words/fontsubstitutionreason/
---
## FontSubstitutionReason enum


يحدد سبب استبدال الخط.

```cpp
enum class FontSubstitutionReason
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| AlternativeName | 0 | [Font](../font/) استبدال باسم بديل من المستند. |
| FontNameSubstitutionRule | 1 | [Font](../font/) استبدال وفق قاعدة اسم الخط. |
| FontConfigSubstitutionRule | 2 | [Font](../font/) استبدال وفق قاعدة إعداد الخط. |
| TableSubstitutionRule | 3 | [Font](../font/) استبدال وفق قاعدة الجدول. |
| FontInfoSubstitutionRule | 4 | استبدال [Font](../font/) وفق قاعدة معلومات الخط. |
| DefaultFontSubstitutionRule | 5 | استبدال [Font](../font/) وفق قاعدة الخط الافتراضي. |
| FirstAvailableFont | 6 | استبدال [Font](../font/) باستخدام أول خط متاح. |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
