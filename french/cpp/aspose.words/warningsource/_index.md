---
title: "Aspose::Words::WarningSource enum"
linktitle: "WarningSource"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::WarningSource enum. Spécifie le module qui génère un avertissement lors du chargement ou de l'enregistrement d'un document en C++."
type: docs
weight: 128000
url: /fr/cpp/aspose.words/warningsource/
---
## WarningSource enum


Spécifie le module qui génère un avertissement lors du chargement ou de l'enregistrement du document.

```cpp
enum class WarningSource
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| Inconnu | 0 | La source de l'avertissement n'est pas spécifiée. |
| Disposition | 1 | Module qui crée la mise en page d'un document. |
| DrawingML | 2 | Module qui rend les formes DrawingML. |
| OfficeMath | 3 | Module qui rend OfficeMath. |
| Formes | 4 | Module qui rend les formes ordinaires. |
| Metafile | 5 | Module qui rend les métafichiers. |
| Xps | 6 | Module qui rend XPS. |
| Pdf | 7 | Module qui rend PDF. |
| Image | 8 | Module qui rend les images. |
| Docx | 9 | Module qui lit/écrit les fichiers DOCX. |
| Doc | 10 | Module qui lit/écrit les fichiers DOC binaires. |
| Texte | 11 | Module qui lit/écrit les fichiers texte brut. |
| Rtf | 12 | Module qui lit/écrit les fichiers RTF. |
| WordML | 13 | Module qui lit/écrit les fichiers WML. |
| Nrx | 14 | Modules communs qui sont partagés entre les modules de lecture/écriture DOCX/WML. |
| Odt | 15 | Module qui lit/écrit les fichiers ODT. |
| Html | 16 | Module qui lit/écrit les fichiers HTML/MHTML. |
| Validateur | 17 | Module qui vérifie la cohérence et la validité du modèle. |
| Xaml | 18 | Module qui lit/écrit les fichiers Xaml. |
| Svm | 19 | Module qui lit les fichiers Svm. |
| MathML | 20 | Module qui lit les fichiers MathML de W3C. |
| Police | 21 | Module qui lit les fichiers de police. |
| Svg | 22 | Module qui lit les fichiers SVG. |
| Markdown | 23 | Module qui lit/écrit les fichiers Markdown. |
| Chm | 24 | Module qui lit les fichiers CHM. |
| Epub | 25 | Module qui lit/écrit les fichiers EPUB. |
| Xml | 26 | Module qui lit les fichiers XML. |
| Xlsx | 27 | Module qui écrit les fichiers XLSX. |
| Docling | 28 | Module qui écrit les fichiers Docling JSON. |


## Exemples



Montre comment travailler avec la source d’avertissement.
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


Montre comment obtenir des informations supplémentaires sur la substitution de police.
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

## Voir aussi

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
