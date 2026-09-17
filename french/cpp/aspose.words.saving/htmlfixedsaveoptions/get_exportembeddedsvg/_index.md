---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedSvg méthode"
linktitle: "get_ExportEmbeddedSvg"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedSvg méthode. Spécifie si les ressources SVG doivent être intégrées dans le document Html. La valeur par défaut est true en C++."
type: docs
weight: 8000
url: /fr/cpp/aspose.words.saving/htmlfixedsaveoptions/get_exportembeddedsvg/
---
## HtmlFixedSaveOptions::get_ExportEmbeddedSvg method


Spécifie si les ressources SVG doivent être incorporées dans le document Html. La valeur par défaut est **true**.

```cpp
bool Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedSvg() const
```


## Exemples



Montre comment déterminer où stocker les objets SVG lors de l'exportation d'un document vers Html.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

// Lorsque nous exportons un document avec des objets SVG vers .html,
// Aspose.Words peut placer ces objets dans deux emplacements possibles.
// Définir le drapeau "ExportEmbeddedSvg" sur "true" intégrera toutes les données brutes des objets SVG
// dans le HTML de sortie, à l'intérieur des balises <image>.
// Définir ce drapeau sur "false" créera un fichier dans le système de fichiers local pour chaque objet SVG.
// Le HTML liera chaque fichier en utilisant l'attribut "data" d'une balise <object>.
auto htmlFixedSaveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
htmlFixedSaveOptions->set_ExportEmbeddedSvg(exportSvgs);

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedSvgs.html", htmlFixedSaveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedSvgs.html");

if (exportSvgs)
{
    ASSERT_FALSE(System::IO::File::Exists(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedSvgs/svg001.svg"));
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"<image id=\"image004\" xlink:href=.+/>")->get_Success());
}
else
{
    ASSERT_TRUE(System::IO::File::Exists(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedSvgs/svg001.svg"));
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"<object type=\"image/svg[+]xml\" data=\"HtmlFixedSaveOptions.ExportEmbeddedSvgs/svg001[.]svg\"></object>")->get_Success());
}
```

## Voir aussi

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
