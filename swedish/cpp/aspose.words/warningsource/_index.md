---
title: "Aspose::Words::WarningSource enum"
linktitle: "WarningSource"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::WarningSource enum. Anger modulen som genererar en varning under dokumentladdning eller -sparande i C++."
type: docs
weight: 128000
url: /sv/cpp/aspose.words/warningsource/
---
## WarningSource enum


Anger modulen som genererar en varning under dokumentladdning eller -sparande.

```cpp
enum class WarningSource
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| Okänd | 0 | Varningskällan är inte specificerad. |
| Layout | 1 | Modul som bygger en dokumentlayout. |
| DrawingML | 2 | Modul som renderar DrawingML-former. |
| OfficeMath | 3 | Modul som renderar OfficeMath. |
| Shapes | 4 | Modul som renderar vanliga former. |
| Metafile | 5 | Modul som renderar metafiler. |
| Xps | 6 | Modul som renderar XPS. |
| Pdf | 7 | Modul som renderar PDF. |
| Image | 8 | Modul som renderar bilder. |
| Docx | 9 | Modul som läser/skriver DOCX-filer. |
| Doc | 10 | Modul som läser/skriver binära DOC-filer. |
| Text | 11 | Modul som läser/skriver klartextfiler. |
| Rtf | 12 | Modul som läser/skriver RTF-filer. |
| WordML | 13 | Modul som läser/skriver WML-filer. |
| Nrx | 14 | Vanliga moduler som delas mellan DOCX/WML läsare/skrivare-moduler. |
| Odt | 15 | Modul som läser/skriv ODT-filer. |
| Html | 16 | Modul som läser/skriv HTML/MHTML-filer. |
| Validator | 17 | Modul som verifierar modellens konsistens och giltighet. |
| Xaml | 18 | Modul som läser/skriv Xaml-filer. |
| Svm | 19 | Modul som läser Svm-filer. |
| MathML | 20 | Modul som läser W3C MathML-filer. |
| Typsnitt | 21 | Modul som läser typsnittsfiler. |
| Svg | 22 | Modul som läser SVG-filer. |
| Markdown | 23 | Modul som läser/skriv Markdown-filer. |
| Chm | 24 | Modul som läser CHM-filer. |
| Epub | 25 | Modul som läser/skriv EPUB-filer. |
| Xml | 26 | Modul som läser XML-filer. |
| Xlsx | 27 | Modul som skriver XLSX-filer. |
| Docling | 28 | Modul som skriver Docling JSON-filer. |


## Exempel



Visar hur man arbetar med varningskällan.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Emphases markdown warning.docx");

auto warnings = System::MakeObject<Aspose::Words::WarningInfoCollection>();
doc->set_WarningCallback(warnings);
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.EmphasesWarningSourceMarkdown.md");

for (auto&& warningInfo : warnings)
{
    if (warningInfo->get_Source() == Aspose::Words::WarningSource::Markdown)
    {
        ASSERT_EQ(u"The (*, 0:11) cannot be properly written into Markdown.", warningInfo->get_Description());
    }
}
```


Visar hur man får ytterligare information om teckensnittssubstitution.
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

## Se även

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
