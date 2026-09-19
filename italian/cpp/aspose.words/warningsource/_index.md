---
title: "Aspose::Words::WarningSource enum"
linktitle: "WarningSource"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::WarningSource enum. Specifica il modulo che genera un avviso durante il caricamento o il salvataggio del documento in C++."
type: docs
weight: 128000
url: /it/cpp/aspose.words/warningsource/
---
## WarningSource enum


Specifica il modulo che genera un avviso durante il caricamento o il salvataggio del documento.

```cpp
enum class WarningSource
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Sconosciuto | 0 | La sorgente dell'avviso non è specificata. |
| Layout | 1 | Modulo che crea il layout di un documento. |
| DrawingML | 2 | Modulo che rende le forme DrawingML. |
| OfficeMath | 3 | Modulo che rende OfficeMath. |
| Forme | 4 | Modulo che rende forme ordinarie. |
| Metafile | 5 | Modulo che rende metafile. |
| Xps | 6 | Modulo che rende XPS. |
| Pdf | 7 | Modulo che rende PDF. |
| Immagine | 8 | Modulo che rende immagini. |
| Docx | 9 | Modulo che legge/scrive file DOCX. |
| Doc | 10 | Modulo che legge/scrive file DOC binari. |
| Testo | 11 | Modulo che legge/scrive file di testo semplice. |
| Rtf | 12 | Modulo che legge/scrive file RTF. |
| WordML | 13 | Modulo che legge/scrive file WML. |
| Nrx | 14 | Moduli comuni condivisi tra i moduli lettore/scrittore DOCX/WML. |
| Odt | 15 | Modulo che legge/scrive file ODT. |
| Html | 16 | Modulo che legge/scrive file HTML/MHTML. |
| Validatore | 17 | Modulo che verifica la coerenza e la validità del modello. |
| Xaml | 18 | Modulo che legge/scrive file Xaml. |
| Svm | 19 | Modulo che legge file Svm. |
| MathML | 20 | Modulo che legge file MathML W3C. |
| Font | 21 | Modulo che legge file di font. |
| Svg | 22 | Modulo che legge file SVG. |
| Markdown | 23 | Modulo che legge/scrive file Markdown. |
| Chm | 24 | Modulo che legge file CHM. |
| Epub | 25 | Modulo che legge/scrive file EPUB. |
| Xml | 26 | Modulo che legge file XML. |
| Xlsx | 27 | Modulo che scrive file XLSX. |
| Docling | 28 | Modulo che scrive file Docling JSON. |


## Esempi



Mostra come lavorare con la sorgente di avviso.
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


Mostra come ottenere informazioni aggiuntive sulla sostituzione del carattere.
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

## Vedi anche

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
