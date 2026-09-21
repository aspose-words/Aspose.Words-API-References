---
title: "Aspose::Words::Fonts::FontSettings::get_DefaultInstance metod"
linktitle: "get_DefaultInstance"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fonts::FontSettings::get_DefaultInstance metod. Statisk standardinställning för teckensnitt i C++."
type: docs
weight: 1000
url: /sv/cpp/aspose.words.fonts/fontsettings/get_defaultinstance/
---
## FontSettings::get_DefaultInstance method


Statisk standardteckensnittsinställning.

```cpp
static System::SharedPtr<Aspose::Words::Fonts::FontSettings> Aspose::Words::Fonts::FontSettings::get_DefaultInstance()
```


## Exempel



Visar hur man konfigurerar standardinställningarna för teckensnitt.
```cpp
// Konfigurera standardinställningarna för teckensnitt så att de använder teckensnittet "Courier New"
// som en reservsubstitution när vi försöker använda ett okänt teckensnitt.
Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->get_SubstitutionSettings()->get_DefaultFontSubstitution()->set_DefaultFontName(u"Courier New");

ASSERT_TRUE(Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->get_SubstitutionSettings()->get_DefaultFontSubstitution()->get_Enabled());

auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Non-existent font");
builder->Write(u"Hello world!");

// Detta dokument har ingen FontSettings‑konfiguration. När vi renderar dokumentet,
// kommer standard‑FontSettings‑instansen att lösa det saknade teckensnittet.
// Aspose.Words kommer att använda "Courier New" för att rendera text som använder det okända teckensnittet.
ASSERT_TRUE(System::TestTools::IsNull(doc->get_FontSettings()));

doc->Save(get_ArtifactsDir() + u"FontSettings.DefaultFontInstance.pdf");
```

## Se även

* Class [FontSettings](../)
* Class [FontSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
