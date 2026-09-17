---
title: "Aspose::Words::LowCode::Splitter::ExtractPages méthode"
linktitle: "ExtractPages"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::LowCode::Splitter::ExtractPages méthode. Extrait une plage spécifiée de pages d'un flux de document et enregistre les pages extraites dans un flux de sortie en utilisant le format de sauvegarde spécifié en C++."
type: docs
weight: 1000
url: /fr/cpp/aspose.words.lowcode/splitter/extractpages/
---
## Splitter::ExtractPages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, int32_t, int32_t) method


Extrait une plage spécifiée de pages d'un flux de document et enregistre les pages extraites dans un flux de sortie en utilisant le format d'enregistrement spécifié.

```cpp
static void Aspose::Words::LowCode::Splitter::ExtractPages(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, int32_t startPageIndex, int32_t pageCount)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Le flux d'entrée. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Le flux de sortie. |
| saveFormat | Aspose::Words::SaveFormat | Le format d'enregistrement. |
| startPageIndex | int32_t | L'index basé sur zéro de la première page à extraire. |
| pageCount | int32_t | Nombre de pages à extraire. |

## Voir aussi

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::ExtractPages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, int32_t, int32_t) method


Extrait une plage spécifiée de pages d'un flux de document et enregistre les pages extraites dans un flux de sortie en utilisant le format d'enregistrement spécifié.

```cpp
static void Aspose::Words::LowCode::Splitter::ExtractPages(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, int32_t startPageIndex, int32_t pageCount)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Le flux d'entrée. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Le flux de sortie. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Les options d'enregistrement. |
| startPageIndex | int32_t | L'index basé sur zéro de la première page à extraire. |
| pageCount | int32_t | Nombre de pages à extraire. |

## Voir aussi

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::ExtractPages(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, int32_t, int32_t) method


Extrait une plage spécifiée de pages d'un fichier de document et enregistre les pages extraites dans un nouveau fichier en utilisant le format d'enregistrement spécifié.

```cpp
static void Aspose::Words::LowCode::Splitter::ExtractPages(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, int32_t startPageIndex, int32_t pageCount)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| inputFileName | const System::String\& | Le nom du fichier d'entrée. |
| outputFileName | const System::String\& | Le nom du fichier de sortie. |
| saveFormat | Aspose::Words::SaveFormat | Le format d'enregistrement. |
| startPageIndex | int32_t | L'index basé sur zéro de la première page à extraire. |
| pageCount | int32_t | Nombre de pages à extraire. |

## Voir aussi

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::ExtractPages(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, int32_t, int32_t) method


Extrait une plage spécifiée de pages d'un fichier de document et enregistre les pages extraites dans un nouveau fichier en utilisant le format d'enregistrement spécifié.

```cpp
static void Aspose::Words::LowCode::Splitter::ExtractPages(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, int32_t startPageIndex, int32_t pageCount)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| inputFileName | const System::String\& | Le nom du fichier d'entrée. |
| outputFileName | const System::String\& | Le nom du fichier de sortie. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Les options d'enregistrement. |
| startPageIndex | int32_t | L'index basé sur zéro de la première page à extraire. |
| pageCount | int32_t | Nombre de pages à extraire. |

## Voir aussi

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::ExtractPages(const System::String\&, const System::String\&, int32_t, int32_t) method


Extrait une plage spécifiée de pages d'un fichier de document et enregistre les pages extraites dans un nouveau fichier. Le format du fichier de sortie est déterminé par l'extension du nom du fichier de sortie.

```cpp
static void Aspose::Words::LowCode::Splitter::ExtractPages(const System::String &inputFileName, const System::String &outputFileName, int32_t startPageIndex, int32_t pageCount)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| inputFileName | const System::String\& | Le nom du fichier d'entrée. |
| outputFileName | const System::String\& | Le nom du fichier de sortie. |
| startPageIndex | int32_t | L'index basé sur zéro de la première page à extraire. |
| pageCount | int32_t | Nombre de pages à extraire. |

## Voir aussi

* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
