---
title: "Méthode ConvertToImages de Aspose::Words::LowCode::Converter"
linktitle: "ConvertToImages"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode ConvertToImages de Aspose::Words::LowCode::Converter. Convertit les pages du document spécifié en images au format indiqué et renvoie un tableau de flux contenant les images en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.lowcode/converter/converttoimages/
---
## Converter::ConvertToImages(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::SaveFormat) method


Convertit les pages du document spécifié en images dans le format spécifié et renvoie un tableau de flux contenant les images.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Converter::ConvertToImages(const System::SharedPtr<Aspose::Words::Document> &doc, Aspose::Words::SaveFormat saveFormat)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::Document\>\& | Le document d'entrée. |
| saveFormat | Aspose::Words::SaveFormat | Format d'enregistrement. Seuls les formats d'image sont autorisés. |

### ReturnValue

Renvoie un tableau de flux d'images. Les flux doivent être libérés par l'utilisateur final.

## Voir aussi

* Class [Document](../../../aspose.words/document/)
* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::SharedPtr\<Aspose::Words::Document\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) method


Convertit les pages du document spécifié en images en utilisant les options d'enregistrement spécifiées et renvoie un tableau de flux contenant les images.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Converter::ConvertToImages(const System::SharedPtr<Aspose::Words::Document> &doc, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::Document\>\& | Le document d'entrée. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Options d'enregistrement d'image. |

### ReturnValue

Renvoie un tableau de flux d'images. Les flux doivent être libérés par l'utilisateur final.

## Voir aussi

* Class [Document](../../../aspose.words/document/)
* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) method


Convertit les pages du flux d'entrée spécifié en images dans le format spécifié et renvoie un tableau de flux contenant les images.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Converter::ConvertToImages(const System::SharedPtr<System::IO::Stream> &inputStream, Aspose::Words::SaveFormat saveFormat)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Le flux d'entrée. |
| saveFormat | Aspose::Words::SaveFormat | Format d'enregistrement. Seuls les formats d'image sont autorisés. |

### ReturnValue

Renvoie un tableau de flux d'images. Les flux doivent être libérés par l'utilisateur final.

## Voir aussi

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) method


Convertit les pages du flux d'entrée spécifié en images en utilisant les options de chargement et d'enregistrement fournies, et renvoie un tableau de flux contenant les images.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Converter::ConvertToImages(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Le flux d'entrée. |
| loadOptions | const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\& | Les options de chargement du document d'entrée. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Options d'enregistrement d'image. |

### ReturnValue

Renvoie un tableau de flux d'images. Les flux doivent être libérés par l'utilisateur final.

## Voir aussi

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) method


Convertit les pages du flux d'entrée spécifié en images en utilisant les options d'enregistrement spécifiées et renvoie un tableau de flux contenant les images.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Converter::ConvertToImages(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Le flux d'entrée. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Options d'enregistrement d'image. |

### ReturnValue

Renvoie un tableau de flux d'images. Les flux doivent être libérés par l'utilisateur final.

## Voir aussi

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::String\&, Aspose::Words::SaveFormat) method


Convertit les pages du fichier d'entrée spécifié en images dans le format spécifié et renvoie un tableau de flux contenant les images.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Converter::ConvertToImages(const System::String &inputFile, Aspose::Words::SaveFormat saveFormat)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| inputFile | const System::String\& | Le nom du fichier d'entrée. |
| saveFormat | Aspose::Words::SaveFormat | Format d'enregistrement. Seuls les formats d'image sont autorisés. |

### ReturnValue

Renvoie un tableau de flux d'images. Les flux doivent être libérés par l'utilisateur final.

## Voir aussi

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) method


Convertit les pages du fichier d'entrée spécifié en fichiers image en utilisant les options de chargement et d'enregistrement fournies.

```cpp
static void Aspose::Words::LowCode::Converter::ConvertToImages(const System::String &inputFile, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions, const System::String &outputFile, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| inputFile | const System::String\& | Le nom du fichier d'entrée. |
| loadOptions | const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\& | Les options de chargement du document d'entrée. |
| outputFile | const System::String\& | Le nom de fichier de sortie utilisé pour générer le nom de fichier des images de page selon la règle "outputFile_pageIndex.extension" |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Options d'enregistrement d'image. |

## Voir aussi

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) method


Convertit les pages du fichier d'entrée spécifié en images en utilisant les options d'enregistrement spécifiées et renvoie un tableau de flux contenant les images.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Converter::ConvertToImages(const System::String &inputFile, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| inputFile | const System::String\& | Le nom du fichier d'entrée. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Options d'enregistrement d'image. |

### ReturnValue

Renvoie un tableau de flux d'images. Les flux doivent être libérés par l'utilisateur final.

## Voir aussi

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::String\&, const System::String\&) method


Convertit les pages du fichier d'entrée spécifié en fichiers image.

```cpp
static void Aspose::Words::LowCode::Converter::ConvertToImages(const System::String &inputFile, const System::String &outputFile)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| inputFile | const System::String\& | Le nom du fichier d'entrée. |
| outputFile | const System::String\& | Le nom de fichier de sortie utilisé pour générer le nom de fichier des images de page selon la règle "outputFile_pageIndex.extension" |

## Voir aussi

* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::String\&, const System::String\&, Aspose::Words::SaveFormat) method


Convertit les pages du fichier d'entrée spécifié en fichiers image dans le format spécifié.

```cpp
static void Aspose::Words::LowCode::Converter::ConvertToImages(const System::String &inputFile, const System::String &outputFile, Aspose::Words::SaveFormat saveFormat)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| inputFile | const System::String\& | Le nom du fichier d'entrée. |
| outputFile | const System::String\& | Le nom de fichier de sortie utilisé pour générer le nom de fichier des images de page selon la règle "outputFile_pageIndex.extension" |
| saveFormat | Aspose::Words::SaveFormat | Format d'enregistrement. Seuls les formats d'image sont autorisés. |

## Voir aussi

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) method


Convertit les pages du fichier d'entrée spécifié en fichiers image en utilisant les options d'enregistrement spécifiées.

```cpp
static void Aspose::Words::LowCode::Converter::ConvertToImages(const System::String &inputFile, const System::String &outputFile, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| inputFile | const System::String\& | Le nom du fichier d'entrée. |
| outputFile | const System::String\& | Le nom de fichier de sortie utilisé pour générer le nom de fichier des images de page selon la règle "outputFile_pageIndex.extension" |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Options d'enregistrement d'image. |

## Voir aussi

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
