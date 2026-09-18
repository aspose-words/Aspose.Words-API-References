---
title: "Aspose::Words::WarningSource‑Enum"
linktitle: "WarningSource"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::WarningSource enum. Gibt das Modul an, das während des Ladens oder Speicherns eines Dokuments in C++ eine Warnung erzeugt."
type: docs
weight: 128000
url: /de/cpp/aspose.words/warningsource/
---
## WarningSource enum


Gibt das Modul an, das während des Ladens oder Speicherns eines Dokuments eine Warnung erzeugt.

```cpp
enum class WarningSource
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Unbekannt | 0 | Die Warnungsquelle ist nicht angegeben. |
| Layout | 1 | Modul, das ein Dokumentlayout erstellt. |
| DrawingML | 2 | Modul, das DrawingML-Formen rendert. |
| OfficeMath | 3 | Modul, das OfficeMath rendert. |
| Shapes | 4 | Modul, das gewöhnliche Formen rendert. |
| Metafile | 5 | Modul, das Metadateien rendert. |
| Xps | 6 | Modul, das XPS rendert. |
| Pdf | 7 | Modul, das PDF rendert. |
| Image | 8 | Modul, das Bilder rendert. |
| Docx | 9 | Modul, das DOCX-Dateien liest/schreibt. |
| Doc | 10 | Modul, das binäre DOC-Dateien liest/schreibt. |
| Text | 11 | Modul, das Klartextdateien liest/schreibt. |
| Rtf | 12 | Modul, das RTF-Dateien liest/schreibt. |
| WordML | 13 | Modul, das WML-Dateien liest/schreibt. |
| Nrx | 14 | Gemeinsame Module, die zwischen DOCX/WML-Lese-/Schreibmodulen geteilt werden. |
| Odt | 15 | Modul zum Lesen/Schreiben von ODT-Dateien. |
| Html | 16 | Modul zum Lesen/Schreiben von HTML/MHTML-Dateien. |
| Validator | 17 | Modul, das die Konsistenz und Gültigkeit des Modells überprüft. |
| Xaml | 18 | Modul zum Lesen/Schreiben von Xaml-Dateien. |
| Svm | 19 | Modul zum Lesen von Svm-Dateien. |
| MathML | 20 | Modul zum Lesen von W3C MathML-Dateien. |
| Font | 21 | Modul zum Lesen von Font-Dateien. |
| Svg | 22 | Modul zum Lesen von SVG-Dateien. |
| Markdown | 23 | Modul zum Lesen/Schreiben von Markdown-Dateien. |
| Chm | 24 | Modul zum Lesen von CHM-Dateien. |
| Epub | 25 | Modul zum Lesen/Schreiben von EPUB-Dateien. |
| Xml | 26 | Modul zum Lesen von XML-Dateien. |
| Xlsx | 27 | Modul zum Schreiben von XLSX-Dateien. |
| Docling | 28 | Modul zum Schreiben von Docling JSON-Dateien. |


## Beispiele



Zeigt, wie man mit der Warnungsquelle arbeitet.
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


Zeigt, wie man zusätzliche Informationen zur Schriftart-Substitution erhält.
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

## Siehe auch

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
