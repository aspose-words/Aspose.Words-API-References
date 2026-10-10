---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_MetafileFormat méthode"
linktitle: "get_MetafileFormat"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_MetafileFormat méthode. Spécifie dans quel format les métafichiers sont enregistrés lors de l'exportation vers HTML, MHTML ou EPUB. La valeur par défaut est Png, ce qui signifie que les métafichiers sont rendus en images PNG raster en C++."
type: docs
weight: 40000
url: /fr/cpp/aspose.words.saving/htmlsaveoptions/get_metafileformat/
---
## HtmlSaveOptions::get_MetafileFormat method


Spécifie dans quel format les métafichiers sont enregistrés lors de l'exportation vers HTML, MHTML ou EPUB. La valeur par défaut est [Png](../../htmlmetafileformat/), ce qui signifie que les métafichiers sont rendus en images PNG raster.

```cpp
Aspose::Words::Saving::HtmlMetafileFormat Aspose::Words::Saving::HtmlSaveOptions::get_MetafileFormat() const
```

## Remarques


Les métafichiers ne sont pas affichés nativement par les navigateurs HTML. Par défaut, Aspose.Words convertit les images WMF et EMF en fichiers PNG lors de l'exportation vers HTML. D'autres options consistent à convertir les métafichiers en images SVG ou à les exporter tels quels sans conversion.

Certaines transformations d'image, en particulier le recadrage, ne seront pas appliquées aux images de métafichiers si elles sont exportées vers HTML sans conversion.

## Exemples



Montre comment convertir des objets SVG en un format différent lors de l'enregistrement de documents HTML.
```cpp
System::String html = u"<html>\r\n                    <svg xmlns='http://www.w3.org/2000/svg' width='500' height='40' viewBox='0 0 500 40'>\r\n                        <text x='0' y='35' font-family='Verdana' font-size='35'>Hello world!</text>\r\n                    </svg>\r\n                </html>";

// Utilisez 'ConvertSvgToEmf' pour rétablir le comportement hérité
// où toutes les images SVG chargées depuis un document HTML étaient converties en EMF.
// Désormais, les images SVG sont chargées sans conversion
// si la version de MS Word spécifiée dans les options de chargement prend en charge les images SVG nativement.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>();
loadOptions->set_ConvertSvgToEmf(true);

auto doc = System::MakeObject<Aspose::Words::Document>(System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_UTF8()->GetBytes(html)), loadOptions);

// Ce document contient un élément <svg> sous forme de texte.
// Lorsque nous enregistrons le document au format HTML, nous pouvons transmettre un objet SaveOptions
// pour déterminer comment l'opération d'enregistrement gère cet objet.
// Définir la propriété "MetafileFormat" sur "HtmlMetafileFormat.Png" pour le convertir en image PNG.
// Définir la propriété "MetafileFormat" sur "HtmlMetafileFormat.Svg" pour le conserver en tant qu'objet SVG.
// Définir la propriété "MetafileFormat" sur "HtmlMetafileFormat.EmfOrWmf" pour le convertir en métafichier.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_MetafileFormat(htmlMetafileFormat);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.MetafileFormat.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.MetafileFormat.html");

switch (htmlMetafileFormat)
{
    case Aspose::Words::Saving::HtmlMetafileFormat::Png:
        ASSERT_TRUE(outDocContents.Contains(System::String(u"<p style=\"margin-top:0pt; margin-bottom:0pt\">") + u"<img src=\"HtmlSaveOptions.MetafileFormat.001.png\" width=\"500\" height=\"40\" alt=\"\" " + u"style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />" + u"</p>"));
        break;

    case Aspose::Words::Saving::HtmlMetafileFormat::Svg:
        ASSERT_TRUE(outDocContents.Contains(System::String(u"<span style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\">") + u"<svg xmlns=\"http://www.w3.org/2000/svg\" xmlns:xlink=\"http://www.w3.org/1999/xlink\" version=\"1.1\" width=\"499\" height=\"40\">"));
        break;

    case Aspose::Words::Saving::HtmlMetafileFormat::EmfOrWmf:
        ASSERT_TRUE(outDocContents.Contains(System::String(u"<p style=\"margin-top:0pt; margin-bottom:0pt\">") + u"<img src=\"HtmlSaveOptions.MetafileFormat.001.emf\" width=\"500\" height=\"40\" alt=\"\" " + u"style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />" + u"</p>"));
        break;

}
```

## Voir aussi

* Enum [HtmlMetafileFormat](../../htmlmetafileformat/)
* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
