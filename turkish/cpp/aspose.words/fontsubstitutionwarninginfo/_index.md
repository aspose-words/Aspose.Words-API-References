---
title: "Aspose::Words::FontSubstitutionWarningInfo sınıfı"
linktitle: "FontSubstitutionWarningInfo"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::FontSubstitutionWarningInfo sınıfı. Aspose.Words tarafından belge yükleme veya kaydetme sırasında C++'ta verilen bir yazı tipi ikame uyarısı hakkında bilgi içerir."
type: docs
weight: 29500
url: /tr/cpp/aspose.words/fontsubstitutionwarninginfo/
---
## FontSubstitutionWarningInfo class


Aspose.Words tarafından belge yükleme veya kaydetme sırasında verilen bir yazı tipi ikame uyarısı hakkında bilgi içerir.

```cpp
class FontSubstitutionWarningInfo : public Aspose::Words::WarningInfo
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_Description](../warninginfo/get_description/)() const | Uyarının açıklamasını döndürür. |
| [get_Reason](./get_reason/)() const | [Font](../font/) ikame nedeni. |
| [get_RequestedBold](./get_requestedbold/)() const | Kalın stilinin istenip istenmediğini gösterir. |
| [get_RequestedFamilyName](./get_requestedfamilyname/)() const | İstenen yazı tipi ailesi adı. |
| [get_RequestedItalic](./get_requesteditalic/)() const | İtalik stilinin istenip istenmediğini gösterir. |
| [get_ResolvedFont](./get_resolvedfont/)() const | Çözülmüş yazı tipi. |
| [get_Source](../warninginfo/get_source/)() const | Uyarının kaynağını döndürür. |
| [get_WarningType](../warninginfo/get_warningtype/)() const | Uyarının türünü döndürür. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

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

* Class [WarningInfo](../warninginfo/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
