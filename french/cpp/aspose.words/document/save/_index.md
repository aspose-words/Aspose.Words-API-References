---
title: "Méthode Aspose::Words::Document::Save"
linktitle: "Save"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Document::Save. Enregistre le document dans un flux en utilisant le format spécifié en C++."
type: docs
weight: 72000
url: /fr/cpp/aspose.words/document/save/
---
## Document::Save(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) method


Enregistre le document dans un flux en utilisant le format spécifié.

```cpp
System::SharedPtr<Aspose::Words::Saving::SaveOutputParameters> Aspose::Words::Document::Save(const System::SharedPtr<System::IO::Stream> &stream, Aspose::Words::SaveFormat saveFormat)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| flux | const System::SharedPtr\<System::IO::Stream\>\& | Flux où enregistrer le document. |
| saveFormat | Aspose::Words::SaveFormat | Le format dans lequel enregistrer le document. |

### ReturnValue

Informations supplémentaires que vous pouvez éventuellement utiliser.

## Exemples



Montre comment enregistrer un document en image via un flux, puis lire l'image depuis ce flux.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Times New Roman");
builder->get_Font()->set_Size(24);
builder->Writeln(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder->InsertImage(get_ImageDir() + u"Logo.jpg");
```


Montre comment enregistrer un document dans un flux.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

{
    auto dstStream = System::MakeObject<System::IO::MemoryStream>();
    doc->Save(dstStream, Aspose::Words::SaveFormat::Docx);

    // Vérifiez que le flux contient le document.
    ASSERT_EQ(u"Hello World!\r\rHello Word!\r\r\rHello World!", System::MakeObject<Aspose::Words::Document>(dstStream)->GetText().Trim());
}
```

## Voir aussi

* Class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* Enum [SaveFormat](../../saveformat/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Save(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) method


Enregistre le document dans un flux en utilisant les options d'enregistrement spécifiées.

```cpp
System::SharedPtr<Aspose::Words::Saving::SaveOutputParameters> Aspose::Words::Document::Save(const System::SharedPtr<System::IO::Stream> &stream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| flux | const System::SharedPtr\<System::IO::Stream\>\& | Flux où enregistrer le document. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Spécifie les options qui contrôlent la façon dont le document est enregistré. Peut être **null**. Si c'est **null**, le document sera enregistré au format binaire DOC. |

### ReturnValue

Informations supplémentaires que vous pouvez éventuellement utiliser.

## Voir aussi

* Class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Save(const System::String\&) method


Enregistre le document dans un fichier. Détermine automatiquement le format d'enregistrement à partir de l'extension.

```cpp
System::SharedPtr<Aspose::Words::Saving::SaveOutputParameters> Aspose::Words::Document::Save(const System::String &fileName)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| fileName | const System::String\& | Le nom du document. Si un document portant le nom de fichier spécifié existe déjà, le document existant est écrasé. |

### ReturnValue

Informations supplémentaires que vous pouvez éventuellement utiliser.

## Exemples



Montre comment ouvrir un document et le convertir en .PDF.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

doc->Save(get_ArtifactsDir() + u"Document.ConvertToPdf.pdf");
```

## Voir aussi

* Class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Save(const System::String\&, Aspose::Words::SaveFormat) method


Enregistre le document dans un fichier au format spécifié.

```cpp
System::SharedPtr<Aspose::Words::Saving::SaveOutputParameters> Aspose::Words::Document::Save(const System::String &fileName, Aspose::Words::SaveFormat saveFormat)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| fileName | const System::String\& | Le nom du document. Si un document portant le nom de fichier spécifié existe déjà, le document existant est écrasé. |
| saveFormat | Aspose::Words::SaveFormat | Le format dans lequel enregistrer le document. |

### ReturnValue

Informations supplémentaires que vous pouvez éventuellement utiliser.

## Exemples



Montre comment convertir du format DOCX vers le format HTML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

doc->Save(get_ArtifactsDir() + u"Document.ConvertToHtml.html", Aspose::Words::SaveFormat::Html);
```

## Voir aussi

* Class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* Enum [SaveFormat](../../saveformat/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Save(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) method


Enregistre le document dans un fichier en utilisant les options d'enregistrement spécifiées.

```cpp
System::SharedPtr<Aspose::Words::Saving::SaveOutputParameters> Aspose::Words::Document::Save(const System::String &fileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| fileName | const System::String\& | Le nom du document. Si un document portant le nom de fichier spécifié existe déjà, le document existant est écrasé. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Spécifie les options qui contrôlent la façon dont le document est enregistré. Peut être **null**. |

### ReturnValue

Informations supplémentaires que vous pouvez éventuellement utiliser.

## Exemples



Montre comment améliorer la qualité d'un document rendu avec SaveOptions.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Size(60);
builder->Writeln(u"Some text.");

System::SharedPtr<Aspose::Words::Saving::SaveOptions> options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);

doc->Save(get_ArtifactsDir() + u"Document.ImageSaveOptions.Default.jpg", options);

options->set_UseAntiAliasing(true);
options->set_UseHighQualityRendering(true);

doc->Save(get_ArtifactsDir() + u"Document.ImageSaveOptions.HighQuality.jpg", options);
```


Montre comment rendre une page d'un document en image JPEG.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 2.");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 3.");

// Créez un objet "ImageSaveOptions" que nous pouvons transmettre à la méthode "Save" du document
// pour modifier la façon dont cette méthode rend le document en image.
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);
// Définissez "PageSet" à "1" pour sélectionner la deuxième page via
// l'index basé sur zéro à partir duquel commencer le rendu du document.
options->set_PageSet(System::MakeObject<Aspose::Words::Saving::PageSet>(1));

// Lorsque nous enregistrons le document au format JPEG, Aspose.Words ne rend qu'une seule page.
// Cette image contiendra une page à partir de la page deux,
// qui sera simplement la deuxième page du document original.
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.OnePage.jpg", options);
```


Montre comment rendre chaque page d'un document en une image TIFF distincte.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 2.");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 3.");

// Créez un objet "ImageSaveOptions" que nous pouvons transmettre à la méthode "Save" du document
// pour modifier la façon dont cette méthode rend le document en image.
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Tiff);

for (int32_t i = 0; i < doc->get_PageCount(); i++)
{
    // Définissez la propriété "PageSet" au numéro de la première page à partir de
    // à partir de laquelle commencer le rendu du document.
    options->set_PageSet(System::MakeObject<Aspose::Words::Saving::PageSet>(i));
    // Exporter la page à 2325x5325 pixels et 600 dpi.
    options->set_Resolution(600.0f);
    options->set_ImageSize(System::Drawing::Size(2325, 5325));

    doc->Save(get_ArtifactsDir() + System::String::Format(u"ImageSaveOptions.PageByPage.{0}.tiff", i + 1), options);
}
```


Montre comment configurer la compression lors de l'enregistrement d'un document au format JPEG.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Créez un objet "ImageSaveOptions" que nous pouvons transmettre à la méthode "Save" du document
// pour modifier la façon dont cette méthode rend le document en image.
auto imageOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);
// Définissez la propriété "JpegQuality" sur "10" pour utiliser une compression plus forte lors du rendu du document.
// Cela réduira la taille du fichier du document, mais l'image affichera des artefacts de compression plus visibles.
imageOptions->set_JpegQuality(10);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

// Définissez la propriété "JpegQuality" sur "100" pour utiliser une compression plus faible lors du rendu du document.
// Cela améliorera la qualité de l'image au prix d'une taille de fichier accrue.
imageOptions->set_JpegQuality(100);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);
```

## Voir aussi

* Class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Save(std::basic_ostream\<CharType, Traits\>\&, Aspose::Words::SaveFormat) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Saving::SaveOutputParameters> Aspose::Words::Document::Save(std::basic_ostream<CharType, Traits> &stream, Aspose::Words::SaveFormat saveFormat)
```

## Voir aussi

* Class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* Enum [SaveFormat](../../saveformat/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Save(std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Saving::SaveOutputParameters> Aspose::Words::Document::Save(std::basic_ostream<CharType, Traits> &stream, System::SharedPtr<Aspose::Words::Saving::SaveOptions> saveOptions)
```

## Voir aussi

* Class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
