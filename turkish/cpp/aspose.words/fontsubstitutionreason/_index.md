---
title: "Aspose::Words::FontSubstitutionReason enum"
linktitle: "FontSubstitutionReason"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::FontSubstitutionReason enum. C++'da font ikamesinin nedenini belirtir."
type: docs
weight: 89500
url: /tr/cpp/aspose.words/fontsubstitutionreason/
---
## FontSubstitutionReason enum


Yazı tipi ikamesinin nedenini belirtir.

```cpp
enum class FontSubstitutionReason
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| AlternativeName | 0 | [Font](../font/) belgeden alternatif adla ikame. |
| FontNameSubstitutionRule | 1 | [Font](../font/) font adı kuralına göre ikame. |
| FontConfigSubstitutionRule | 2 | [Font](../font/) font yapılandırma kuralına göre ikame. |
| TableSubstitutionRule | 3 | [Font](../font/) tablo kuralına göre ikame. |
| FontInfoSubstitutionRule | 4 | [Font](../font/) değişimi font bilgisi kuralına göre. |
| DefaultFontSubstitutionRule | 5 | [Font](../font/) değişimi varsayılan font kuralına göre. |
| FirstAvailableFont | 6 | [Font](../font/) değişimi ilk kullanılabilir font ile. |


## Örnekler



Yazı tipi ikamesi hakkında ek bilgi almanın nasıl yapılacağını gösterir.
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

## Ayrıca Bakınız

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
