---
title: "Aspose::Words::DocumentBuilder::InsertOnlineVideo method"
linktitle: "InsertOnlineVideo"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::DocumentBuilder::InsertOnlineVideo method. Insère un objet vidéo en ligne dans le document et le redimensionne à la taille spécifiée en C++."
type: docs
weight: 43000
url: /fr/cpp/aspose.words/documentbuilder/insertonlinevideo/
---
## DocumentBuilder::InsertOnlineVideo(const System::String\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


Insère un objet vidéo en ligne dans le document et le redimensionne à la taille spécifiée.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOnlineVideo(const System::String &videoUrl, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| videoUrl | const System::String\& | L’URL de la vidéo. |
| horzPos | Aspose::Words::Drawing::RelativeHorizontalPosition | Spécifie le point de référence à partir duquel la distance à l’image est mesurée. |
| left | double | Distance en points entre l’origine et le côté gauche de l’image. |
| vertPos | Aspose::Words::Drawing::RelativeVerticalPosition | Spécifie le point de référence à partir duquel la distance à l’image est mesurée. |
| top | double | Distance en points entre l’origine et le côté supérieur de l’image. |
| largeur | double | La largeur de l’image en points. Peut être une valeur négative ou zéro pour demander une échelle de 100 %. |
| hauteur | double | La hauteur de l’image en points. Peut être une valeur négative ou zéro pour demander une échelle de 100 %. |
| wrapType | Aspose::Words::Drawing::WrapType | Spécifie comment le texte s’enroule autour de l’image. |

### ReturnValue

Le nœud d’image qui vient d’être inséré.
## Remarques


Vous pouvez modifier la taille, l’emplacement, la méthode de positionnement et d’autres paramètres de l’image en utilisant l’objet [Shape](../../../aspose.words.drawing/shape/) retourné par cette méthode.

L’insertion de vidéos en ligne à partir des ressources suivantes est prise en charge :

* [https://www.youtube.com/](https://www.youtube.com/)
* [https://vimeo.com/](https://vimeo.com/)



Si votre vidéo en ligne ne s’affiche pas correctement, utilisez [InsertOnlineVideo()](../), qui accepte du code HTML intégré personnalisé.

Le code d’intégration vidéo peut varier selon les fournisseurs ; consultez le fournisseur correspondant de votre choix pour plus de détails.

## Voir aussi

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOnlineVideo(const System::String\&, const System::String\&, const System::ArrayPtr\<uint8_t\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


Insère un objet vidéo en ligne dans le document et le redimensionne à la taille spécifiée.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOnlineVideo(const System::String &videoUrl, const System::String &videoEmbedCode, const System::ArrayPtr<uint8_t> &thumbnailImageBytes, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| videoUrl | const System::String\& | L’URL de la vidéo. |
| videoEmbedCode | const System::String\& | Le code d’intégration de la vidéo. |
| thumbnailImageBytes | const System::ArrayPtr\<uint8_t\>\& | Les octets de l’image miniature. |
| horzPos | Aspose::Words::Drawing::RelativeHorizontalPosition | Spécifie le point de référence à partir duquel la distance à l’image est mesurée. |
| left | double | Distance en points entre l’origine et le côté gauche de l’image. |
| vertPos | Aspose::Words::Drawing::RelativeVerticalPosition | Spécifie le point de référence à partir duquel la distance à l’image est mesurée. |
| top | double | Distance en points entre l’origine et le côté supérieur de l’image. |
| largeur | double | La largeur de l’image en points. Peut être une valeur négative ou zéro pour demander une échelle de 100 %. |
| hauteur | double | La hauteur de l’image en points. Peut être une valeur négative ou zéro pour demander une échelle de 100 %. |
| wrapType | Aspose::Words::Drawing::WrapType | Spécifie comment le texte s’enroule autour de l’image. |

### ReturnValue

Le nœud d’image qui vient d’être inséré.
## Remarques


Vous pouvez modifier la taille, l’emplacement, la méthode de positionnement et d’autres paramètres de l’image en utilisant l’objet [Shape](../../../aspose.words.drawing/shape/) retourné par cette méthode.

## Exemples



Montre comment insérer une vidéo en ligne dans un document avec une miniature personnalisée.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::String videoUrl = u"https://vimeo.com/52477838";
System::String videoEmbedCode = System::String(u"<iframe src=\"https://player.vimeo.com/video/52477838\" width=\"640\" height=\"360\" frameborder=\"0\" ") + u"title=\"Aspose\" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>";

System::ArrayPtr<uint8_t> thumbnailImageBytes = System::IO::File::ReadAllBytes(get_ImageDir() + u"Logo.jpg");

{
    auto stream = System::MakeObject<System::IO::MemoryStream>(thumbnailImageBytes);
    {
        System::SharedPtr<System::Drawing::Image> image = System::Drawing::Image::FromStream(stream);
        // Voici deux façons de créer une forme avec une miniature personnalisée, qui renvoie à une vidéo en ligne
        // qui se lira lorsque nous cliquerons sur la forme dans Microsoft Word.
        // 1 -  Insérer une forme en ligne à l'emplacement du curseur d'insertion du nœud du constructeur :
        builder->InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes, image->get_Width(), image->get_Height());

        builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

        // 2 -  Insérer une forme flottante :
        double left = builder->get_PageSetup()->get_RightMargin() - image->get_Width();
        double top = builder->get_PageSetup()->get_BottomMargin() - image->get_Height();

        builder->InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes, Aspose::Words::Drawing::RelativeHorizontalPosition::RightMargin, left, Aspose::Words::Drawing::RelativeVerticalPosition::BottomMargin, top, image->get_Width(), image->get_Height(), Aspose::Words::Drawing::WrapType::Square);
    }
}

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertOnlineVideoCustomThumbnail.docx");
```

## Voir aussi

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOnlineVideo(const System::String\&, const System::String\&, const System::ArrayPtr\<uint8_t\>\&, double, double) method


Insère un objet vidéo en ligne dans le document et le redimensionne à la taille spécifiée.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOnlineVideo(const System::String &videoUrl, const System::String &videoEmbedCode, const System::ArrayPtr<uint8_t> &thumbnailImageBytes, double width, double height)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| videoUrl | const System::String\& | L’URL de la vidéo. |
| videoEmbedCode | const System::String\& | Le code d’intégration de la vidéo. |
| thumbnailImageBytes | const System::ArrayPtr\<uint8_t\>\& | Les octets de l’image miniature. |
| largeur | double | La largeur de l’image en points. Peut être une valeur négative ou zéro pour demander une échelle de 100 %. |
| hauteur | double | La hauteur de l’image en points. Peut être une valeur négative ou zéro pour demander une échelle de 100 %. |

### ReturnValue

Le nœud d’image qui vient d’être inséré.
## Remarques


Vous pouvez modifier la taille, l’emplacement, la méthode de positionnement et d’autres paramètres de l’image en utilisant l’objet [Shape](../../../aspose.words.drawing/shape/) retourné par cette méthode.

## Exemples



Montre comment insérer une vidéo en ligne dans un document avec une miniature personnalisée.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::String videoUrl = u"https://vimeo.com/52477838";
System::String videoEmbedCode = System::String(u"<iframe src=\"https://player.vimeo.com/video/52477838\" width=\"640\" height=\"360\" frameborder=\"0\" ") + u"title=\"Aspose\" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>";

System::ArrayPtr<uint8_t> thumbnailImageBytes = System::IO::File::ReadAllBytes(get_ImageDir() + u"Logo.jpg");

{
    auto stream = System::MakeObject<System::IO::MemoryStream>(thumbnailImageBytes);
    {
        System::SharedPtr<System::Drawing::Image> image = System::Drawing::Image::FromStream(stream);
        // Voici deux façons de créer une forme avec une miniature personnalisée, qui renvoie à une vidéo en ligne
        // qui se lira lorsque nous cliquerons sur la forme dans Microsoft Word.
        // 1 -  Insérer une forme en ligne à l'emplacement du curseur d'insertion du nœud du constructeur :
        builder->InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes, image->get_Width(), image->get_Height());

        builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

        // 2 -  Insérer une forme flottante :
        double left = builder->get_PageSetup()->get_RightMargin() - image->get_Width();
        double top = builder->get_PageSetup()->get_BottomMargin() - image->get_Height();

        builder->InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes, Aspose::Words::Drawing::RelativeHorizontalPosition::RightMargin, left, Aspose::Words::Drawing::RelativeVerticalPosition::BottomMargin, top, image->get_Width(), image->get_Height(), Aspose::Words::Drawing::WrapType::Square);
    }
}

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertOnlineVideoCustomThumbnail.docx");
```

## Voir aussi

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOnlineVideo(const System::String\&, double, double) method


Insère un objet vidéo en ligne dans le document et le redimensionne à la taille spécifiée.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOnlineVideo(const System::String &videoUrl, double width, double height)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| videoUrl | const System::String\& | L’URL de la vidéo. |
| largeur | double | La largeur de l’image en points. Peut être une valeur négative ou zéro pour demander une échelle de 100 %. |
| hauteur | double | La hauteur de l’image en points. Peut être une valeur négative ou zéro pour demander une échelle de 100 %. |

### ReturnValue

Le nœud d’image qui vient d’être inséré.
## Remarques


Vous pouvez modifier la taille, l’emplacement, la méthode de positionnement et d’autres paramètres de l’image en utilisant l’objet [Shape](../../../aspose.words.drawing/shape/) retourné par cette méthode.

L’insertion de vidéos en ligne à partir des ressources suivantes est prise en charge :

* [https://www.youtube.com/](https://www.youtube.com/)
* [https://vimeo.com/](https://vimeo.com/)



Si votre vidéo en ligne ne s’affiche pas correctement, utilisez [InsertOnlineVideo()](../), qui accepte du code HTML intégré personnalisé.

Le code d’intégration vidéo peut varier selon les fournisseurs ; consultez le fournisseur correspondant de votre choix pour plus de détails.

## Exemples



Montre comment insérer une vidéo en ligne dans un document à l'aide d'une URL.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertOnlineVideo(u"https://youtu.be/g1N9ke8Prmk", 360, 270);

// Nous pouvons regarder la vidéo depuis Microsoft Word en cliquant sur la forme.
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertVideoWithUrl.docx");
```

## Voir aussi

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
