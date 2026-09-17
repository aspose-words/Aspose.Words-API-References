---
title: "Méthode CompareToImages de Aspose::Words::LowCode::Comparer"
linktitle: "CompareToImages"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode CompareToImages de Aspose::Words::LowCode::Comparer. Compare deux documents et enregistre les différences sous forme d'images. Chaque élément du tableau retourné représente une page unique de la sortie rendue comme une image en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.lowcode/comparer/comparetoimages/
---
## Comparer::CompareToImages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, System::DateTime) method


Compare deux documents et enregistre les différences sous forme d'images. Chaque élément du tableau retourné représente une page unique de la sortie rendue sous forme d'image.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Comparer::CompareToImages(const System::SharedPtr<System::IO::Stream> &v1, const System::SharedPtr<System::IO::Stream> &v2, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &imageSaveOptions, const System::String &author, System::DateTime dateTime)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| v1 | const System::SharedPtr\<System::IO::Stream\>\& | Le document original. |
| v2 | const System::SharedPtr\<System::IO::Stream\>\& | Le document modifié. |
| imageSaveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Les options d'enregistrement d'image de la sortie. |
| auteur | const System::String\& | Initiales de l’auteur à utiliser pour les révisions. |
| dateTime | System::DateTime | La date et l'heure à utiliser pour les révisions. |

## Voir aussi

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::CompareToImages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) method


Compare deux documents et enregistre les différences sous forme d'images. Chaque élément du tableau retourné représente une page unique de la sortie rendue sous forme d'image.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Comparer::CompareToImages(const System::SharedPtr<System::IO::Stream> &v1, const System::SharedPtr<System::IO::Stream> &v2, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &imageSaveOptions, const System::String &author, System::DateTime dateTime, const System::SharedPtr<Aspose::Words::Comparing::CompareOptions> &compareOptions)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| v1 | const System::SharedPtr\<System::IO::Stream\>\& | Le document original. |
| v2 | const System::SharedPtr\<System::IO::Stream\>\& | Le document modifié. |
| imageSaveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Les options d'enregistrement d'image de la sortie. |
| auteur | const System::String\& | Initiales de l’auteur à utiliser pour les révisions. |
| dateTime | System::DateTime | La date et l'heure à utiliser pour les révisions. |
| compareOptions | const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\& | [Document](../../../aspose.words/document/) options de comparaison. |

## Voir aussi

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::CompareToImages(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, System::DateTime) method


Compare deux documents et enregistre les différences sous forme d'images. Chaque élément du tableau retourné représente une page unique de la sortie rendue sous forme d'image.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Comparer::CompareToImages(const System::String &v1, const System::String &v2, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &imageSaveOptions, const System::String &author, System::DateTime dateTime)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| v1 | const System::String\& | Le document original. |
| v2 | const System::String\& | Le document modifié. |
| imageSaveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Les options d'enregistrement d'image de la sortie. |
| auteur | const System::String\& | Initiales de l’auteur à utiliser pour les révisions. |
| dateTime | System::DateTime | La date et l'heure à utiliser pour les révisions. |

## Voir aussi

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::CompareToImages(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) method


Compare deux documents et enregistre les différences sous forme d'images. Chaque élément du tableau retourné représente une page unique de la sortie rendue sous forme d'image.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Comparer::CompareToImages(const System::String &v1, const System::String &v2, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &imageSaveOptions, const System::String &author, System::DateTime dateTime, const System::SharedPtr<Aspose::Words::Comparing::CompareOptions> &compareOptions)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| v1 | const System::String\& | Le document original. |
| v2 | const System::String\& | Le document modifié. |
| imageSaveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Les options d'enregistrement d'image de la sortie. |
| auteur | const System::String\& | Initiales de l’auteur à utiliser pour les révisions. |
| dateTime | System::DateTime | La date et l'heure à utiliser pour les révisions. |
| compareOptions | const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\& | [Document](../../../aspose.words/document/) options de comparaison. |

## Voir aussi

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
