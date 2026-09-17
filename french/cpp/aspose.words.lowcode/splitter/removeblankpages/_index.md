---
title: "Aspose::Words::LowCode::Splitter::RemoveBlankPages méthode"
linktitle: "RemoveBlankPages"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::LowCode::Splitter::RemoveBlankPages méthode. Supprime les pages blanches d'un document fourni dans un flux d'entrée et enregistre le document mis à jour dans un flux de sortie au format d'enregistrement spécifié. Retourne une liste des numéros de pages qui ont été supprimés en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.lowcode/splitter/removeblankpages/
---
## Splitter::RemoveBlankPages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) method


Supprime les pages blanches d'un document fourni dans un flux d'entrée et enregistre le document mis à jour dans un flux de sortie au format d'enregistrement spécifié. Retourne une liste des numéros de pages qui ont été supprimés.

```cpp
static System::SharedPtr<System::Collections::Generic::List<int32_t>> Aspose::Words::LowCode::Splitter::RemoveBlankPages(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Le flux d'entrée. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Le flux de sortie. |
| saveFormat | Aspose::Words::SaveFormat | Le format d'enregistrement. |

### ReturnValue

La liste des numéros de page a été considérée comme vide et supprimée.

## Voir aussi

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::RemoveBlankPages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) method


Supprime les pages blanches d'un document fourni dans un flux d'entrée et enregistre le document mis à jour dans un flux de sortie au format d'enregistrement spécifié. Retourne une liste des numéros de pages qui ont été supprimés.

```cpp
static System::SharedPtr<System::Collections::Generic::List<int32_t>> Aspose::Words::LowCode::Splitter::RemoveBlankPages(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Le flux d'entrée. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Le flux de sortie. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Les options d'enregistrement. |

### ReturnValue

La liste des numéros de page a été considérée comme vide et supprimée.

## Voir aussi

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::RemoveBlankPages(const System::String\&, const System::String\&) method


Supprime les pages vides du document et enregistre la sortie. Retourne une liste des numéros de pages qui ont été supprimés.

```cpp
static System::SharedPtr<System::Collections::Generic::List<int32_t>> Aspose::Words::LowCode::Splitter::RemoveBlankPages(const System::String &inputFileName, const System::String &outputFileName)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| inputFileName | const System::String\& | Le nom du fichier d'entrée. |
| outputFileName | const System::String\& | Le nom du fichier de sortie. |

### ReturnValue

La liste des numéros de page a été considérée comme vide et supprimée.

## Voir aussi

* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::RemoveBlankPages(const System::String\&, const System::String\&, Aspose::Words::SaveFormat) method


Supprime les pages vides du document et enregistre la sortie dans le format spécifié. Retourne une liste des numéros de pages qui ont été supprimés.

```cpp
static System::SharedPtr<System::Collections::Generic::List<int32_t>> Aspose::Words::LowCode::Splitter::RemoveBlankPages(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| inputFileName | const System::String\& | Le nom du fichier d'entrée. |
| outputFileName | const System::String\& | Le nom du fichier de sortie. |
| saveFormat | Aspose::Words::SaveFormat | Le format d'enregistrement. |

### ReturnValue

La liste des numéros de page a été considérée comme vide et supprimée.

## Voir aussi

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::RemoveBlankPages(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) method


Supprime les pages vides du document et enregistre la sortie dans le format spécifié. Retourne une liste des numéros de pages qui ont été supprimés.

```cpp
static System::SharedPtr<System::Collections::Generic::List<int32_t>> Aspose::Words::LowCode::Splitter::RemoveBlankPages(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| inputFileName | const System::String\& | Le nom du fichier d'entrée. |
| outputFileName | const System::String\& | Le nom du fichier de sortie. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Les options d'enregistrement. |

### ReturnValue

La liste des numéros de page a été considérée comme vide et supprimée.

## Voir aussi

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
