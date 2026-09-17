---
title: "Méthode Aspose::Words::DocumentBuilder::InsertImage"
linktitle: "InsertImage"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::DocumentBuilder::InsertImage. Insère une image à partir d'un tableau d'octets dans le document. L'image est insérée en ligne et à 100 % d'échelle en C++."
type: docs
weight: 39000
url: /fr/cpp/aspose.words/documentbuilder/insertimage/
---
## DocumentBuilder::InsertImage(const System::ArrayPtr\<uint8_t\>\&) method


Insère une image à partir d'un tableau d'octets dans le document. L'image est insérée en ligne et à 100 % d'échelle.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::ArrayPtr<uint8_t> &imageBytes)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| imageBytes | const System::ArrayPtr\<uint8_t\>\& | Le tableau d'octets qui contient l'image. |

### ReturnValue

Le nœud d’image qui vient d’être inséré.
## Remarques


Vous pouvez modifier la taille, l’emplacement, la méthode de positionnement et d’autres paramètres de l’image en utilisant l’objet [Shape](../../../aspose.words.drawing/shape/) retourné par cette méthode.

## Exemples



Montre comment insérer une image à partir d'un tableau d'octets dans un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::ArrayPtr<uint8_t> imageByteArray = Aspose::Words::ApiExamples::TestUtil::ImageToByteArray(get_ImageDir() + u"Logo.jpg");

// Voici trois façons d'insérer une image à partir d'un tableau d'octets.
// 1 - Forme en ligne avec une taille par défaut basée sur les dimensions d'origine de l'image :
builder->InsertImage(imageByteArray);

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 - Forme en ligne avec des dimensions personnalisées :
builder->InsertImage(imageByteArray, Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 3 - Forme flottante avec des dimensions personnalisées :
builder->InsertImage(imageByteArray, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromByteArray.docx");
```

## Voir aussi

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::ArrayPtr\<uint8_t\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


Insère une image à partir d'un tableau d'octets à la position et à la taille spécifiées.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::ArrayPtr<uint8_t> &imageBytes, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| imageBytes | const System::ArrayPtr\<uint8_t\>\& | Le tableau d'octets qui contient l'image. |
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



Montre comment insérer une image à partir d'un tableau d'octets dans un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::ArrayPtr<uint8_t> imageByteArray = Aspose::Words::ApiExamples::TestUtil::ImageToByteArray(get_ImageDir() + u"Logo.jpg");

// Voici trois façons d'insérer une image à partir d'un tableau d'octets.
// 1 - Forme en ligne avec une taille par défaut basée sur les dimensions d'origine de l'image :
builder->InsertImage(imageByteArray);

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 - Forme en ligne avec des dimensions personnalisées :
builder->InsertImage(imageByteArray, Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 3 - Forme flottante avec des dimensions personnalisées :
builder->InsertImage(imageByteArray, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromByteArray.docx");
```

## Voir aussi

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::ArrayPtr\<uint8_t\>\&, double, double) method


Insère une image en ligne à partir d'un tableau d'octets dans le document et la redimensionne à la taille spécifiée.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::ArrayPtr<uint8_t> &imageBytes, double width, double height)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| imageBytes | const System::ArrayPtr\<uint8_t\>\& | Le tableau d'octets qui contient l'image. |
| largeur | double | La largeur de l’image en points. Peut être une valeur négative ou zéro pour demander une échelle de 100 %. |
| hauteur | double | La hauteur de l’image en points. Peut être une valeur négative ou zéro pour demander une échelle de 100 %. |

### ReturnValue

Le nœud d’image qui vient d’être inséré.
## Remarques


Vous pouvez modifier la taille, l’emplacement, la méthode de positionnement et d’autres paramètres de l’image en utilisant l’objet [Shape](../../../aspose.words.drawing/shape/) retourné par cette méthode.

## Exemples



Montre comment insérer une image à partir d'un tableau d'octets dans un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::ArrayPtr<uint8_t> imageByteArray = Aspose::Words::ApiExamples::TestUtil::ImageToByteArray(get_ImageDir() + u"Logo.jpg");

// Voici trois façons d'insérer une image à partir d'un tableau d'octets.
// 1 - Forme en ligne avec une taille par défaut basée sur les dimensions d'origine de l'image :
builder->InsertImage(imageByteArray);

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 - Forme en ligne avec des dimensions personnalisées :
builder->InsertImage(imageByteArray, Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 3 - Forme flottante avec des dimensions personnalisées :
builder->InsertImage(imageByteArray, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromByteArray.docx");
```

## Voir aussi

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::SharedPtr\<System::Drawing::Image\>\&) method


Insère une image à partir d'un objet **Image** dans le document. L'image est insérée en ligne et à 100 % d'échelle.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::SharedPtr<System::Drawing::Image> &image)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| image | const System::SharedPtr\<System::Drawing::Image\>\& | L'image à insérer dans le document. |

### ReturnValue

Le nœud d’image qui vient d’être inséré.
## Remarques


Vous pouvez modifier la taille, l’emplacement, la méthode de positionnement et d’autres paramètres de l’image en utilisant l’objet [Shape](../../../aspose.words.drawing/shape/) retourné par cette méthode.

## Exemples



Montre comment insérer une image à partir d'un objet dans un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::String imageFile = get_ImageDir() + u"Logo.jpg";

// Voici trois façons d'insérer une image à partir d'une instance d'objet Image.
// 1 - Forme en ligne avec une taille par défaut basée sur les dimensions d'origine de l'image :
builder->InsertImage(imageFile);

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 - Forme en ligne avec des dimensions personnalisées :
builder->InsertImage(imageFile, Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 3 - Forme flottante avec des dimensions personnalisées :
builder->InsertImage(imageFile, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromImageObject.docx");
```

## Voir aussi

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::SharedPtr\<System::Drawing::Image\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


Insère une image à partir d'un objet **Image** à la position et à la taille spécifiées.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::SharedPtr<System::Drawing::Image> &image, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| image | const System::SharedPtr\<System::Drawing::Image\>\& | L'image à insérer dans le document. |
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



Montre comment insérer une image à partir d'un objet dans un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::String imageFile = get_ImageDir() + u"Logo.jpg";

// Voici trois façons d'insérer une image à partir d'une instance d'objet Image.
// 1 - Forme en ligne avec une taille par défaut basée sur les dimensions d'origine de l'image :
builder->InsertImage(imageFile);

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 - Forme en ligne avec des dimensions personnalisées :
builder->InsertImage(imageFile, Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 3 - Forme flottante avec des dimensions personnalisées :
builder->InsertImage(imageFile, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromImageObject.docx");
```

## Voir aussi

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::SharedPtr\<System::Drawing::Image\>\&, double, double) method


Insère une image en ligne à partir d'un objet **Image** dans le document et la redimensionne à la taille spécifiée.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::SharedPtr<System::Drawing::Image> &image, double width, double height)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| image | const System::SharedPtr\<System::Drawing::Image\>\& | L'image à insérer dans le document. |
| largeur | double | La largeur de l’image en points. Peut être une valeur négative ou zéro pour demander une échelle de 100 %. |
| hauteur | double | La hauteur de l’image en points. Peut être une valeur négative ou zéro pour demander une échelle de 100 %. |

### ReturnValue

Le nœud d’image qui vient d’être inséré.
## Remarques


Vous pouvez modifier la taille, l’emplacement, la méthode de positionnement et d’autres paramètres de l’image en utilisant l’objet [Shape](../../../aspose.words.drawing/shape/) retourné par cette méthode.

## Exemples



Montre comment insérer une image à partir d'un objet dans un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::String imageFile = get_ImageDir() + u"Logo.jpg";

// Voici trois façons d'insérer une image à partir d'une instance d'objet Image.
// 1 - Forme en ligne avec une taille par défaut basée sur les dimensions d'origine de l'image :
builder->InsertImage(imageFile);

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 - Forme en ligne avec des dimensions personnalisées :
builder->InsertImage(imageFile, Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 3 - Forme flottante avec des dimensions personnalisées :
builder->InsertImage(imageFile, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromImageObject.docx");
```

## Voir aussi

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::SharedPtr\<System::IO::Stream\>\&) method


Insère une image à partir d'un flux dans le document. L'image est insérée en ligne et à 100 % d'échelle.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::SharedPtr<System::IO::Stream> &stream)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| flux | const System::SharedPtr\<System::IO::Stream\>\& | Le flux qui contient l'image. |

### ReturnValue

Le nœud d’image qui vient d’être inséré.
## Remarques


Vous pouvez modifier la taille, l’emplacement, la méthode de positionnement et d’autres paramètres de l’image en utilisant l’objet [Shape](../../../aspose.words.drawing/shape/) retourné par cette méthode.

## Exemples



Montre comment insérer une image à partir d'un flux dans un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_ImageDir() + u"Logo.jpg");
    // Voici trois façons d'insérer une image à partir d'un flux.
    // 1 - Forme en ligne avec une taille par défaut basée sur les dimensions d'origine de l'image :
    builder->InsertImage(stream);

    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

    // 2 - Forme en ligne avec des dimensions personnalisées :
    builder->InsertImage(stream, Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

    // 3 - Forme flottante avec des dimensions personnalisées :
    builder->InsertImage(stream, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);
}

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromStream.docx");
```


Montre comment insérer une forme avec une image provenant d'un flux dans un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_ImageDir() + u"Logo.jpg");
    builder->Write(u"Image from stream: ");
    builder->InsertImage(stream);
}

doc->Save(get_ArtifactsDir() + u"Image.FromStream.docx");
```

## Voir aussi

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


Insère une image à partir d'un flux à la position et à la taille spécifiées.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::SharedPtr<System::IO::Stream> &stream, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| flux | const System::SharedPtr\<System::IO::Stream\>\& | Le flux qui contient l'image. |
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



Montre comment insérer une image à partir d'un flux dans un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_ImageDir() + u"Logo.jpg");
    // Voici trois façons d'insérer une image à partir d'un flux.
    // 1 - Forme en ligne avec une taille par défaut basée sur les dimensions d'origine de l'image :
    builder->InsertImage(stream);

    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

    // 2 - Forme en ligne avec des dimensions personnalisées :
    builder->InsertImage(stream, Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

    // 3 - Forme flottante avec des dimensions personnalisées :
    builder->InsertImage(stream, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);
}

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromStream.docx");
```

## Voir aussi

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::SharedPtr\<System::IO::Stream\>\&, double, double) method


Insère une image en ligne à partir d'un flux dans le document et la redimensionne à la taille spécifiée.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::SharedPtr<System::IO::Stream> &stream, double width, double height)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| flux | const System::SharedPtr\<System::IO::Stream\>\& | Le flux qui contient l'image. |
| largeur | double | La largeur de l’image en points. Peut être une valeur négative ou zéro pour demander une échelle de 100 %. |
| hauteur | double | La hauteur de l’image en points. Peut être une valeur négative ou zéro pour demander une échelle de 100 %. |

### ReturnValue

Le nœud d’image qui vient d’être inséré.
## Remarques


Vous pouvez modifier la taille, l’emplacement, la méthode de positionnement et d’autres paramètres de l’image en utilisant l’objet [Shape](../../../aspose.words.drawing/shape/) retourné par cette méthode.

## Exemples



Montre comment insérer une image à partir d'un flux dans un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_ImageDir() + u"Logo.jpg");
    // Voici trois façons d'insérer une image à partir d'un flux.
    // 1 - Forme en ligne avec une taille par défaut basée sur les dimensions d'origine de l'image :
    builder->InsertImage(stream);

    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

    // 2 - Forme en ligne avec des dimensions personnalisées :
    builder->InsertImage(stream, Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

    // 3 - Forme flottante avec des dimensions personnalisées :
    builder->InsertImage(stream, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);
}

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromStream.docx");
```

## Voir aussi

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::String\&) method


Insère une image à partir d'un fichier ou d'une URL dans le document. L'image est insérée en ligne et à 100 % d'échelle.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::String &fileName)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| fileName | const System::String\& | Le fichier contenant l'image. Peut être n'importe quel URI local ou distant valide. |

### ReturnValue

Le nœud d’image qui vient d’être inséré.
## Remarques


Cette surcharge téléchargera automatiquement l'image avant de l'insérer dans le document si vous spécifiez un URI distant.

Vous pouvez modifier la taille, l’emplacement, la méthode de positionnement et d’autres paramètres de l’image en utilisant l’objet [Shape](../../../aspose.words.drawing/shape/) retourné par cette méthode.

## Exemples



Montre comment insérer une image à partir du système de fichiers local dans un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Voici trois façons d'insérer une image à partir d'un nom de fichier système local.
// 1 - Forme en ligne avec une taille par défaut basée sur les dimensions d'origine de l'image :
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 - Forme en ligne avec des dimensions personnalisées :
builder->InsertImage(get_ImageDir() + u"Transparent background logo.png", Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 3 - Forme flottante avec des dimensions personnalisées :
builder->InsertImage(get_ImageDir() + u"Windows MetaFile.wmf", Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromFilename.docx");
```


Montre comment déterminer quelle image sera insérée.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertImage(get_ImageDir() + u"Scalable Vector Graphics.svg");

// Aspose.Words insère une image SVG dans le document en tant que PNG avec l'extension svgBlip
// qui contient la représentation vectorielle SVG originale de l'image.
doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertSvgImage.SvgWithSvgBlip.docx");

// Aspose.Words insère une image SVG dans le document en tant que PNG, tout comme Microsoft Word le fait pour les anciens formats.
doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertSvgImage.Svg.doc");

doc->get_CompatibilityOptions()->OptimizeFor(Aspose::Words::Settings::MsWordVersion::Word2003);

// Aspose.Words insère une image SVG dans le document en tant que métafichier EMF pour conserver l'image en représentation vectorielle.
doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertSvgImage.Emf.docx");
```


Montre comment insérer une image gif dans le document.
```cpp
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();

// Nous pouvons insérer une image gif en utilisant un chemin ou un tableau d'octets.
// Ça ne fonctionne que si DocumentBuilder est optimisé pour la version Word 2010 ou supérieure.
// Notez que l'accès aux octets de l'image entraîne la conversion de Gif en Png.
System::SharedPtr<Aspose::Words::Drawing::Shape> gifImage = builder->InsertImage(get_ImageDir() + u"Graphics Interchange Format.gif");

gifImage = builder->InsertImage(System::IO::File::ReadAllBytes(get_ImageDir() + u"Graphics Interchange Format.gif"));

builder->get_Document()->Save(get_ArtifactsDir() + u"InsertGif.docx");
```


Montre comment insérer une forme avec une image dans un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Voici deux emplacements où la méthode "InsertShape" du constructeur de document
// peut fournir l'image que la forme affichera.
// 1 -  Passez un nom de fichier du système de fichiers local d'une image :
builder->Write(u"Image from local file: ");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");
builder->Writeln();

// 2 -  Passez une URL qui pointe vers une image.
builder->Write(u"Image from a URL: ");
builder->InsertImage(get_ImageUrl());
builder->Writeln();

doc->Save(get_ArtifactsDir() + u"Image.FromUrl.docx");
```


Montre comment insérer une image flottante au centre d'une page.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insérez une image flottante qui apparaîtra derrière le texte qui se chevauche et alignez‑la au centre de la page.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);
shape->set_BehindText(true);
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_HorizontalAlignment(Aspose::Words::Drawing::HorizontalAlignment::Center);
shape->set_VerticalAlignment(Aspose::Words::Drawing::VerticalAlignment::Center);

doc->Save(get_ArtifactsDir() + u"Image.CreateFloatingPageCenter.docx");
```


Montre comment insérer une image WebP.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertImage(get_ImageDir() + u"WebP image.webp");

doc->Save(get_ArtifactsDir() + u"Image.InsertWebpImage.docx");
```

## Voir aussi

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::String\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


Insère une image à partir d'un fichier ou d'une URL à la position et à la taille spécifiées.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::String &fileName, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| fileName | const System::String\& | Le fichier qui contient l'image. |
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



Montre comment insérer une image.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Il existe deux façons d'utiliser un constructeur de document pour fournir une image puis l'insérer en tant que forme flottante.
// 1 -  À partir d'un fichier du système de fichiers local :
builder->InsertImage(get_ImageDir() + u"Transparent background logo.png", Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 0.0, 200.0, 200.0, Aspose::Words::Drawing::WrapType::Square);

// 2 -  À partir d'une URL :
builder->InsertImage(get_ImageUrl(), Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 250.0, 200.0, 200.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertFloatingImage.docx");
```


Montre comment insérer une image du système de fichiers local dans un document tout en préservant ses dimensions.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// La méthode InsertImage crée une forme flottante avec l'image transmise dans ses données d'image.
// Nous pouvons spécifier les dimensions de la forme en les passant à cette méthode.
System::SharedPtr<Aspose::Words::Drawing::Shape> imageShape = builder->InsertImage(get_ImageDir() + u"Logo.jpg", Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 0.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 0.0, -1.0, -1.0, Aspose::Words::Drawing::WrapType::Square);

// Passer des valeurs négatives comme dimensions prévues définira automatiquement
// les dimensions de la forme en fonction des dimensions de son image.
ASPOSE_ASSERT_EQ(300.0, imageShape->get_Width());
ASPOSE_ASSERT_EQ(300.0, imageShape->get_Height());

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertImageOriginalSize.docx");
```


Montre comment insérer une image à partir du système de fichiers local dans un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Voici trois façons d'insérer une image à partir d'un nom de fichier système local.
// 1 - Forme en ligne avec une taille par défaut basée sur les dimensions d'origine de l'image :
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 - Forme en ligne avec des dimensions personnalisées :
builder->InsertImage(get_ImageDir() + u"Transparent background logo.png", Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 3 - Forme flottante avec des dimensions personnalisées :
builder->InsertImage(get_ImageDir() + u"Windows MetaFile.wmf", Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromFilename.docx");
```

## Voir aussi

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::String\&, double, double) method


Insère une image en ligne à partir d'un fichier ou d'une URL dans le document et la redimensionne à la taille spécifiée.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::String &fileName, double width, double height)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| fileName | const System::String\& | Le fichier qui contient l'image. |
| largeur | double | La largeur de l’image en points. Peut être une valeur négative ou zéro pour demander une échelle de 100 %. |
| hauteur | double | La hauteur de l’image en points. Peut être une valeur négative ou zéro pour demander une échelle de 100 %. |

### ReturnValue

Le nœud d’image qui vient d’être inséré.
## Remarques


Vous pouvez modifier la taille, l’emplacement, la méthode de positionnement et d’autres paramètres de l’image en utilisant l’objet [Shape](../../../aspose.words.drawing/shape/) retourné par cette méthode.

## Exemples



Montre comment insérer une image à partir du système de fichiers local dans un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Voici trois façons d'insérer une image à partir d'un nom de fichier système local.
// 1 - Forme en ligne avec une taille par défaut basée sur les dimensions d'origine de l'image :
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 - Forme en ligne avec des dimensions personnalisées :
builder->InsertImage(get_ImageDir() + u"Transparent background logo.png", Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 3 - Forme flottante avec des dimensions personnalisées :
builder->InsertImage(get_ImageDir() + u"Windows MetaFile.wmf", Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromFilename.docx");
```

## Voir aussi

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(std::basic_istream<CharType, Traits> &stream)
```

## Voir aussi

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(std::basic_istream\<CharType, Traits\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(std::basic_istream<CharType, Traits> &stream, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```

## Voir aussi

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(std::basic_istream\<CharType, Traits\>\&, double, double) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(std::basic_istream<CharType, Traits> &stream, double width, double height)
```

## Voir aussi

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
