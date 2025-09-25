---
title: Aspose::Words::WarningSource enum
linktitle: WarningSource
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::WarningSource enum. Specifies the module that produces a warning during document loading or saving in C++.'
type: docs
weight: 128000
url: /cpp/aspose.words/warningsource/
---
## WarningSource enum


Specifies the module that produces a warning during document loading or saving.

```cpp
enum class WarningSource
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Unknown | 0 | The warning source is not specified. |
| Layout | 1 | Module that builds a document layout. |
| DrawingML | 2 | Module that renders DrawingML shapes. |
| OfficeMath | 3 | Module that renders OfficeMath. |
| Shapes | 4 | Module that renders ordinary shapes. |
| Metafile | 5 | Module that renders metafiles. |
| Xps | 6 | Module that renders XPS. |
| Pdf | 7 | Module that renders PDF. |
| Image | 8 | Module that renders images. |
| Docx | 9 | Module that reads/writes DOCX files. |
| Doc | 10 | Module that reads/writes binary DOC files. |
| Text | 11 | Module that reads/writes plaintext files. |
| Rtf | 12 | Module that reads/writes RTF files. |
| WordML | 13 | Module that reads/writes WML files. |
| Nrx | 14 | Common modules that are shared between DOCX/WML reader/writer modules. |
| Odt | 15 | Module that reads/writes ODT files. |
| Html | 16 | Module that reads/writes HTML/MHTML files. |
| Validator | 17 | Module that verifies model consistency and validity. |
| Xaml | 18 | Module that reads/writes Xaml files. |
| Svm | 19 | Module that reads Svm files. |
| MathML | 20 | Module that reads W3C MathML files. |
| Font | 21 | Module that reads font files. |
| Svg | 22 | Module that reads SVG files. |
| Markdown | 23 | Module that reads/writes Markdown files. |
| Chm | 24 | Module that reads CHM files. |
| Epub | 25 | Module that reads/writes EPUB files. |
| Xml | 26 | Module that reads XML files. |
| Xlsx | 27 | Module that writes XLSX files. |


## Examples



Shows how to work with the warning source. 
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


Shows how to get additional information about font substitution. 
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

## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
