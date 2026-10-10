---
title: "Aspose::Words::Loading::LoadOptions::get_FontSettings yöntemi"
linktitle: "get_FontSettings"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Loading::LoadOptions::get_FontSettings yöntemi. C++'ta belge yazı tipi ayarlarını belirtmeye olanak tanır."
type: docs
weight: 7000
url: /tr/cpp/aspose.words.loading/loadoptions/get_fontsettings/
---
## LoadOptions::get_FontSettings method


Belge yazı tipi ayarlarını belirtmeye izin verir.

```cpp
System::SharedPtr<Aspose::Words::Fonts::FontSettings> Aspose::Words::Loading::LoadOptions::get_FontSettings() const
```

## Açıklamalar


Bazı biçimler yüklenirken, Aspose.Words yazı tiplerini çözümlemesi gerekebilir. Örneğin, HTML belgeleri yüklerken [Aspose.Words](../../../aspose.words/) yazı tiplerini çözümleyerek yedekleme (fallback) yapabilir.

Eğer **null** olarak ayarlanırsa, varsayılan sabit yazı tipi ayarları [DefaultInstance](../../../aspose.words.fonts/fontsettings/get_defaultinstance/) kullanılacaktır.

Varsayılan değer **null**'dır.

## Örnekler



Yükleme sırasında yazı tipi ikamelerini nasıl belirleyeceğinizi gösterir.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());

// Bir LoadOptions nesnesi için yazı tipi ikame kuralı ayarlayın.
// Yüklediğimiz belge, sahip olmadığımız bir yazı tipi kullanıyorsa,
// bu kural mevcut olmayan yazı tipini var olan bir yazı tipiyle ikame eder.
// Bu durumda, "MissingFont" ifadesinin tüm kullanımları "Comic Sans MS" olarak dönüştürülecektir.
System::SharedPtr<Aspose::Words::Fonts::TableSubstitutionRule> substitutionRule = loadOptions->get_FontSettings()->get_SubstitutionSettings()->get_TableSubstitution();
substitutionRule->AddSubstitutes(u"MissingFont", System::MakeArray<System::String>({u"Comic Sans MS"}));

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Missing font.html", loadOptions);

// Bu noktada böyle metin hâlâ "MissingFont" içinde olacaktır.
// Belgeyi render ettiğimizde yazı tipi ikamesi gerçekleşecektir.
ASSERT_EQ(u"MissingFont", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Font()->get_Name());

doc->Save(get_ArtifactsDir() + u"FontSettings.ResolveFontsBeforeLoadingDocument.pdf");
```


Bir belge yüklenirken yazı tipi ikamesi ayarlarının nasıl uygulanacağını gösterir.
```cpp
// "Times New Roman" yazı tipini ikame edecek bir FontSettings nesnesi oluşturun
// "MyFonts" klasörümüzden "Arvo" yazı tipiyle.
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
fontSettings->SetFontsFolder(get_FontsDir(), false);
fontSettings->get_SubstitutionSettings()->get_TableSubstitution()->AddSubstitutes(u"Times New Roman", System::MakeArray<System::String>({u"Arvo"}));

// O FontSettings nesnesini yeni oluşturulan bir LoadOptions nesnesinin özelliği olarak ayarlayın.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_FontSettings(fontSettings);

// Belgeyi yükleyin, ardından yazı tipi ikamesiyle PDF olarak render edin.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx", loadOptions);

doc->Save(get_ArtifactsDir() + u"LoadOptions.FontSettings.pdf");
```

## Ayrıca Bakınız

* Class [FontSettings](../../../aspose.words.fonts/fontsettings/)
* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
