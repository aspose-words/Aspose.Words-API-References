---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedImages méthode"
linktitle: "get_ExportEmbeddedImages"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedImages méthode. Spécifie si les images doivent être intégrées dans le document Html au format Base64. Notez que la définition de ce drapeau peut augmenter considérablement la taille du fichier Html de sortie en C++."
type: docs
weight: 7000
url: /fr/cpp/aspose.words.saving/htmlfixedsaveoptions/get_exportembeddedimages/
---
## HtmlFixedSaveOptions::get_ExportEmbeddedImages method


Spécifie si les images doivent être incorporées dans le document Html au format Base64. Notez que l'activation de ce drapeau peut augmenter considérablement la taille du fichier Html de sortie.

```cpp
bool Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedImages() const
```


## Exemples



Montre comment déterminer où stocker les images lors de l'exportation d'un document vers Html.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

// Lorsque nous exportons un document avec des images intégrées vers .html,
// Aspose.Words peut placer les images à deux emplacements possibles.
// Définir le drapeau "ExportEmbeddedImages" sur "true" stockera les données brutes
// pour toutes les images du document HTML de sortie, dans l'attribut "src" des balises <image>.
// Définir ce drapeau sur "false" créera un fichier image dans le système de fichiers local pour chaque image,
// et stockera tous ces fichiers dans un dossier séparé.
auto htmlFixedSaveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
htmlFixedSaveOptions->set_ExportEmbeddedImages(exportImages);

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedImages.html", htmlFixedSaveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedImages.html");

if (exportImages)
{
    ASSERT_FALSE(System::IO::File::Exists(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedImages/image001.jpeg"));
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"<img class=\"awimg\" style=\"left:0pt; top:0pt; width:493.1pt; height:300.55pt;\" src=\".+\" />")->get_Success());
}
else
{
    ASSERT_TRUE(System::IO::File::Exists(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedImages/image001.jpeg"));
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, System::String(u"<img class=\"awimg\" style=\"left:0pt; top:0pt; width:493.1pt; height:300.55pt;\" ") + u"src=\"HtmlFixedSaveOptions[.]ExportEmbeddedImages/image001[.]jpeg\" />")->get_Success());
}
```

## Voir aussi

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
