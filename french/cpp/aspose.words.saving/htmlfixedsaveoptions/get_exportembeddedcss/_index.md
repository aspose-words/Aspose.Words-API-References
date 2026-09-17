---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedCss méthode"
linktitle: "get_ExportEmbeddedCss"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedCss méthode. Spécifie si le CSS (Cascading Style Sheet) doit être intégré dans le document Html en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words.saving/htmlfixedsaveoptions/get_exportembeddedcss/
---
## HtmlFixedSaveOptions::get_ExportEmbeddedCss method


Spécifie si le CSS (Cascading [Style](../../../aspose.words/style/) Sheet) doit être intégré dans le document Html.

```cpp
bool Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedCss() const
```


## Exemples



Montre comment déterminer où stocker les feuilles de style CSS lors de l'exportation d'un document vers Html.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Lorsque nous exportons un document vers html, Aspose.Words créera également une feuille de style CSS pour formater le document.
// Définir le drapeau "ExportEmbeddedCss" sur "true" enregistre la feuille de style CSS dans un fichier .css,
// et crée un lien vers le fichier depuis le document html en utilisant un élément <link>.
// Définir le drapeau sur "false" intégrera la feuille de style CSS dans le document Html,
// ce qui créera un seul fichier au lieu de deux.
auto htmlFixedSaveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
htmlFixedSaveOptions->set_ExportEmbeddedCss(exportEmbeddedCss);

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedCss.html", htmlFixedSaveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedCss.html");

if (exportEmbeddedCss)
{
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"<style type=\"text/css\">")->get_Success());
    ASSERT_FALSE(System::IO::File::Exists(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedCss/styles.css"));
}
else
{
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"<link rel=\"stylesheet\" type=\"text/css\" href=\"HtmlFixedSaveOptions[.]ExportEmbeddedCss/styles[.]css\" media=\"all\" />")->get_Success());
    ASSERT_TRUE(System::IO::File::Exists(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedCss/styles.css"));
}
```

## Voir aussi

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
