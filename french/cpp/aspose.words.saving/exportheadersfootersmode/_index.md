---
title: "Énumération Aspose::Words::Saving::ExportHeadersFootersMode"
linktitle: "ExportHeadersFootersMode"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Énumération Aspose::Words::Saving::ExportHeadersFootersMode. Spécifie comment les en-têtes et pieds de page sont exportés vers HTML, MHTML ou EPUB en C++."
type: docs
weight: 55000
url: /fr/cpp/aspose.words.saving/exportheadersfootersmode/
---
## ExportHeadersFootersMode enum


Spécifie comment les en-têtes et pieds de page sont exportés vers HTML, MHTML ou EPUB.

```cpp
enum class ExportHeadersFootersMode
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| None | 0 | Les en-têtes et pieds de page ne sont pas exportés. |
| PerSection | 1 | Les en-têtes et pieds de page principaux sont exportés au début et à la fin de chaque section. |
| FirstSectionHeaderLastSectionFooter | 2 | L'en-tête principal de la première section est exporté au début du document et le pied de page principal est à la fin. |
| FirstPageHeaderFooterPerSection | 3 | L'en-tête et le pied de page de la première page sont exportés au début et à la fin de chaque section. |


## Exemples



Montre comment omettre les en-têtes/pieds de page lors de l'enregistrement d'un document au format HTML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Header and footer types.docx");

// Ce document contient des en-têtes et des pieds de page. Nous pouvons y accéder via la collection "HeadersFooters".
ASSERT_EQ(u"First header", doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::HeaderFirst)->GetText().Trim());

// Les formats tels que .html ne divisent pas le document en pages, donc les en-têtes/pieds de page ne fonctionneront pas de la même manière
// comme ils le feraient lorsque nous ouvrons le document au format .docx avec Microsoft Word.
// Si nous convertissons un document avec des en-têtes/pieds de page en html, la conversion intégrera les en-têtes/pieds de page dans le texte du corps.
// Nous pouvons utiliser un objet SaveOptions pour omettre les en-têtes/pieds de page lors de la conversion en html.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Html);
saveOptions->set_ExportHeadersFootersMode(Aspose::Words::Saving::ExportHeadersFootersMode::None);

doc->Save(get_ArtifactsDir() + u"HeaderFooter.ExportMode.html", saveOptions);

// Ouvrez notre document enregistré et vérifiez qu'il ne contient pas le texte de l'en-tête
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"HeaderFooter.ExportMode.html");

ASSERT_FALSE(doc->get_Range()->get_Text().Contains(u"First header"));
```

## Voir aussi

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
