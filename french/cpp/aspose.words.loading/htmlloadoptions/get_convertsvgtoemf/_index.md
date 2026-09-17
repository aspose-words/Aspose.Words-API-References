---
title: "Aspose::Words::Loading::HtmlLoadOptions::get_ConvertSvgToEmf méthode"
linktitle: "get_ConvertSvgToEmf"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Loading::HtmlLoadOptions::get_ConvertSvgToEmf méthode. Obtient ou définit une valeur indiquant s'il faut convertir les images SVG chargées au format EMF. La valeur par défaut est false et, si possible, les images SVG chargées sont conservées telles quelles sans conversion en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.loading/htmlloadoptions/get_convertsvgtoemf/
---
## HtmlLoadOptions::get_ConvertSvgToEmf method


Obtient ou définit une valeur indiquant s'il faut convertir les images SVG chargées au format EMF. La valeur par défaut est **false** et, si possible, les images SVG chargées sont conservées telles quelles sans conversion.

```cpp
bool Aspose::Words::Loading::HtmlLoadOptions::get_ConvertSvgToEmf() const
```

## Remarques


Les versions plus récentes de MS Word prennent en charge les images SVG nativement. Si la version de MS Word spécifiée dans les options de chargement prend en charge le SVG, Aspose.Words stockera les images SVG telles quelles sans conversion. Si le SVG n'est pas pris en charge, les images SVG chargées seront converties au format EMF.

Cependant, si cette option est définie sur **true**, Aspose.Words convertira les images SVG chargées en EMF même si les images SVG sont prises en charge par la version spécifiée de MS Word.

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

* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
