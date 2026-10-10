---
title: "Méthode Aspose::Words::Watermark::SetImage"
linktitle: "SetImage"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Watermark::SetImage. Ajoute un filigrane image dans le document en C++."
type: docs
weight: 6000
url: /fr/cpp/aspose.words/watermark/setimage/
---
## Watermark::SetImage(const System::SharedPtr\<System::Drawing::Image\>\&) method


Ajoute un filigrane image dans le document.

```cpp
void Aspose::Words::Watermark::SetImage(const System::SharedPtr<System::Drawing::Image> &image)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| image | const System::SharedPtr\<System::Drawing::Image\>\& | Image affichée comme filigrane. |

## Exemples



Montre comment créer un filigrane à partir d'une image dans le système de fichiers local.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Modifiez l'apparence du filigrane d'image avec un objet ImageWatermarkOptions,
// puis transmettez-le lors de la création d'un filigrane à partir d'un fichier image.
auto imageWatermarkOptions = System::MakeObject<Aspose::Words::ImageWatermarkOptions>();
imageWatermarkOptions->set_Scale(5);
imageWatermarkOptions->set_IsWashout(false);

// Nous disposons d'options différentes pour insérer une image.
// Utilisez l'une des méthodes suivantes pour ajouter un filigrane d'image.
doc->get_Watermark()->SetImage(System::Drawing::Image::FromFile(get_ImageDir() + u"Logo.jpg"));

doc->get_Watermark()->SetImage(System::Drawing::Image::FromFile(get_ImageDir() + u"Logo.jpg"), imageWatermarkOptions);

doc->get_Watermark()->SetImage(get_ImageDir() + u"Logo.jpg", imageWatermarkOptions);

doc->Save(get_ArtifactsDir() + u"Document.ImageWatermark.docx");
```

## Voir aussi

* Class [Watermark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Watermark::SetImage(const System::SharedPtr\<System::Drawing::Image\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Ajoute un filigrane image dans le document.

```cpp
void Aspose::Words::Watermark::SetImage(const System::SharedPtr<System::Drawing::Image> &image, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| image | const System::SharedPtr\<System::Drawing::Image\>\& | Image affichée comme filigrane. |
| options | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Définit des options supplémentaires pour le filigrane image. |

## Exemples



Montre comment créer un filigrane à partir d'une image dans le système de fichiers local.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Modifiez l'apparence du filigrane d'image avec un objet ImageWatermarkOptions,
// puis transmettez-le lors de la création d'un filigrane à partir d'un fichier image.
auto imageWatermarkOptions = System::MakeObject<Aspose::Words::ImageWatermarkOptions>();
imageWatermarkOptions->set_Scale(5);
imageWatermarkOptions->set_IsWashout(false);

// Nous disposons d'options différentes pour insérer une image.
// Utilisez l'une des méthodes suivantes pour ajouter un filigrane d'image.
doc->get_Watermark()->SetImage(System::Drawing::Image::FromFile(get_ImageDir() + u"Logo.jpg"));

doc->get_Watermark()->SetImage(System::Drawing::Image::FromFile(get_ImageDir() + u"Logo.jpg"), imageWatermarkOptions);

doc->get_Watermark()->SetImage(get_ImageDir() + u"Logo.jpg", imageWatermarkOptions);

doc->Save(get_ArtifactsDir() + u"Document.ImageWatermark.docx");
```

## Voir aussi

* Class [ImageWatermarkOptions](../../imagewatermarkoptions/)
* Class [Watermark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Watermark::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Ajoute un filigrane image dans le document.

```cpp
void Aspose::Words::Watermark::SetImage(const System::SharedPtr<System::IO::Stream> &imageStream, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| imageStream | const System::SharedPtr\<System::IO::Stream\>\& | Le flux contenant les données d'image affichées comme filigrane. |
| options | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Définit des options supplémentaires pour le filigrane image. |

## Exemples



Montre comment créer un filigrane à partir d'un flux d'image.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Modifiez l'apparence du filigrane d'image avec un objet ImageWatermarkOptions,
// puis transmettez-le lors de la création d'un filigrane à partir d'un fichier image.
auto imageWatermarkOptions = System::MakeObject<Aspose::Words::ImageWatermarkOptions>();
imageWatermarkOptions->set_Scale(5);

{
    auto imageStream = System::MakeObject<System::IO::FileStream>(get_ImageDir() + u"Logo.jpg", System::IO::FileMode::Open, System::IO::FileAccess::Read);
    doc->get_Watermark()->SetImage(imageStream, imageWatermarkOptions);
}

doc->Save(get_ArtifactsDir() + u"Document.ImageWatermarkStream.docx");
```

## Voir aussi

* Class [ImageWatermarkOptions](../../imagewatermarkoptions/)
* Class [Watermark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Watermark::SetImage(const System::String\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Ajoute un filigrane image dans le document.

```cpp
void Aspose::Words::Watermark::SetImage(const System::String &imagePath, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| imagePath | const System::String\& | Chemin vers le fichier image affiché comme filigrane. |
| options | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Définit des options supplémentaires pour le filigrane image. |

## Exemples



Montre comment créer un filigrane à partir d'une image dans le système de fichiers local.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Modifiez l'apparence du filigrane d'image avec un objet ImageWatermarkOptions,
// puis transmettez-le lors de la création d'un filigrane à partir d'un fichier image.
auto imageWatermarkOptions = System::MakeObject<Aspose::Words::ImageWatermarkOptions>();
imageWatermarkOptions->set_Scale(5);
imageWatermarkOptions->set_IsWashout(false);

// Nous disposons d'options différentes pour insérer une image.
// Utilisez l'une des méthodes suivantes pour ajouter un filigrane d'image.
doc->get_Watermark()->SetImage(System::Drawing::Image::FromFile(get_ImageDir() + u"Logo.jpg"));

doc->get_Watermark()->SetImage(System::Drawing::Image::FromFile(get_ImageDir() + u"Logo.jpg"), imageWatermarkOptions);

doc->get_Watermark()->SetImage(get_ImageDir() + u"Logo.jpg", imageWatermarkOptions);

doc->Save(get_ArtifactsDir() + u"Document.ImageWatermark.docx");
```

## Voir aussi

* Class [ImageWatermarkOptions](../../imagewatermarkoptions/)
* Class [Watermark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
