---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportHeadersFootersMode méthode"
linktitle: "get_ExportHeadersFootersMode"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportHeadersFootersMode méthode. Spécifie comment les en-têtes et pieds de page sont exportés vers HTML, MHTML ou EPUB. La valeur par défaut est PerSection pour HTML/MHTML et None pour EPUB en C++."
type: docs
weight: 18000
url: /fr/cpp/aspose.words.saving/htmlsaveoptions/get_exportheadersfootersmode/
---
## HtmlSaveOptions::get_ExportHeadersFootersMode method


Spécifie comment les en-têtes et pieds de page sont exportés vers HTML, MHTML ou EPUB. La valeur par défaut est [PerSection](../../exportheadersfootersmode/) pour HTML/MHTML et [None](../../exportheadersfootersmode/) pour EPUB.

```cpp
Aspose::Words::Saving::ExportHeadersFootersMode Aspose::Words::Saving::HtmlSaveOptions::get_ExportHeadersFootersMode() const
```

## Remarques


Il est difficile d'exporter de manière significative les en-têtes et pieds de page vers HTML parce que HTML n'est pas paginé.

Lorsque cette propriété est [PerSection](../../exportheadersfootersmode/), Aspose.Words exporte uniquement les en-têtes et pieds de page principaux au début et à la fin de chaque section.

Lorsque c'est [FirstSectionHeaderLastSectionFooter](../../exportheadersfootersmode/), seul le premier en-tête principal et le dernier pied de page principal (y compris ceux liés au précédent) sont exportés.

Vous pouvez désactiver complètement l'exportation des en-têtes et pieds de page en définissant cette propriété sur [None](../../exportheadersfootersmode/).

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

* Enum [ExportHeadersFootersMode](../../exportheadersfootersmode/)
* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
