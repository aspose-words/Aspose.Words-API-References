---
title: "Aspose::Words::Loading::LoadOptions::get_FontSettings‑metod"
linktitle: "get_FontSettings"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Loading::LoadOptions::get_FontSettings‑metod. Tillåter att ange dokumentets teckensnittinställningar i C++."
type: docs
weight: 7000
url: /sv/cpp/aspose.words.loading/loadoptions/get_fontsettings/
---
## LoadOptions::get_FontSettings method


Tillåter att ange dokumentets teckensnittinställningar.

```cpp
System::SharedPtr<Aspose::Words::Fonts::FontSettings> Aspose::Words::Loading::LoadOptions::get_FontSettings() const
```

## Anmärkningar


När vissa format laddas kan Aspose.Words behöva lösa upp teckensnitten. Till exempel, när HTML‑dokument laddas kan [Aspose.Words](../../../aspose.words/) lösa teckensnitten för att utföra teckensnittsfallback.

Om den är satt till **null** kommer standardinställningarna för statiska teckensnitt [DefaultInstance](../../../aspose.words.fonts/fontsettings/get_defaultinstance/) att användas.

Standardvärdet är **null**.

## Exempel



Visar hur man anger teckensnittssubstitut vid laddning.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());

// Ställ in en teckensnittssubstitutionsregel för ett LoadOptions‑objekt.
// Om dokumentet vi laddar använder ett teckensnitt som vi inte har,
// kommer denna regel att ersätta det otillgängliga teckensnittet med ett som finns.
// I detta fall kommer alla förekomster av "MissingFont" att konverteras till "Comic Sans MS".
System::SharedPtr<Aspose::Words::Fonts::TableSubstitutionRule> substitutionRule = loadOptions->get_FontSettings()->get_SubstitutionSettings()->get_TableSubstitution();
substitutionRule->AddSubstitutes(u"MissingFont", System::MakeArray<System::String>({u"Comic Sans MS"}));

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Missing font.html", loadOptions);

// Vid detta tillfälle kommer sådan text fortfarande att vara i "MissingFont".
// Teckensnittssubstitution kommer att ske när vi renderar dokumentet.
ASSERT_EQ(u"MissingFont", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Font()->get_Name());

doc->Save(get_ArtifactsDir() + u"FontSettings.ResolveFontsBeforeLoadingDocument.pdf");
```


Visar hur man tillämpar teckensnittssubstitutionsinställningar vid laddning av ett dokument.
```cpp
// Skapa ett FontSettings-objekt som kommer att ersätta teckensnittet "Times New Roman"
// med teckensnittet "Arvo" från vår "MyFonts"-mapp.
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
fontSettings->SetFontsFolder(get_FontsDir(), false);
fontSettings->get_SubstitutionSettings()->get_TableSubstitution()->AddSubstitutes(u"Times New Roman", System::MakeArray<System::String>({u"Arvo"}));

// Ställ in det FontSettings-objektet som en egenskap i ett ny-skapat LoadOptions-objekt.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_FontSettings(fontSettings);

// Läs in dokumentet och rendera det sedan som en PDF med teckensnittsersättningen.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx", loadOptions);

doc->Save(get_ArtifactsDir() + u"LoadOptions.FontSettings.pdf");
```

## Se även

* Class [FontSettings](../../../aspose.words.fonts/fontsettings/)
* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
