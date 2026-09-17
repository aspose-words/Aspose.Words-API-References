---
title: "Aspose::Words::LowCode::Splitter::Split méthode"
linktitle: "Diviser"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::LowCode::Splitter::Split méthode. Divise un document à partir d'un flux d'entrée en plusieurs parties en fonction des options de division spécifiées et renvoie les parties résultantes sous forme d'un tableau de flux dans le format de sauvegarde spécifié en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.lowcode/splitter/split/
---
## Splitter::Split(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) method


Divise un document provenant d'un flux d'entrée en plusieurs parties en fonction des options de division spécifiées et renvoie les parties résultantes sous forme d'un tableau de flux au format d'enregistrement spécifié.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Splitter::Split(const System::SharedPtr<System::IO::Stream> &inputStream, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<Aspose::Words::LowCode::SplitOptions> &options)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Le flux d'entrée. |
| saveFormat | Aspose::Words::SaveFormat | Le format d'enregistrement. |
| options | const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\& | [Document](../../../aspose.words/document/) options de division. |

## Voir aussi

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [SplitOptions](../../splitoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::Split(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) method


Divise un document provenant d'un flux d'entrée en plusieurs parties en fonction des options de division spécifiées et renvoie les parties résultantes sous forme d'un tableau de flux au format d'enregistrement spécifié.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Splitter::Split(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<Aspose::Words::LowCode::SplitOptions> &options)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Le flux d'entrée. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Les options d'enregistrement. |
| options | const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\& | [Document](../../../aspose.words/document/) options de division. |

## Voir aussi

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [SplitOptions](../../splitoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::Split(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) method


Divise un document en plusieurs parties en fonction des options de division spécifiées et enregistre les parties résultantes dans des fichiers au format d'enregistrement spécifié.

```cpp
static void Aspose::Words::LowCode::Splitter::Split(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<Aspose::Words::LowCode::SplitOptions> &options)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| inputFileName | const System::String\& | Le nom du fichier d'entrée. |
| outputFileName | const System::String\& | Le nom de fichier de sortie utilisé pour générer le nom de fichier des parties du document selon la règle "outputFile_partIndex.extension" |
| saveFormat | Aspose::Words::SaveFormat | Le format d'enregistrement. |
| options | const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\& | [Document](../../../aspose.words/document/) options de division. |

## Voir aussi

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [SplitOptions](../../splitoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::Split(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) method


Divise un document en plusieurs parties en fonction des options de division spécifiées et enregistre les parties résultantes dans des fichiers. Le format du fichier de sortie est déterminé par l'extension du nom du fichier de sortie.

```cpp
static void Aspose::Words::LowCode::Splitter::Split(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::LowCode::SplitOptions> &options)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| inputFileName | const System::String\& | Le nom du fichier d'entrée. |
| outputFileName | const System::String\& | Le nom de fichier de sortie utilisé pour générer le nom de fichier des parties du document selon la règle "outputFile_partIndex.extension" |
| options | const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\& | [Document](../../../aspose.words/document/) options de division. |

## Voir aussi

* Class [SplitOptions](../../splitoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::Split(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) method


Divise un document en plusieurs parties en fonction des options de division spécifiées et enregistre les parties résultantes dans des fichiers au format d'enregistrement spécifié.

```cpp
static void Aspose::Words::LowCode::Splitter::Split(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<Aspose::Words::LowCode::SplitOptions> &options)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| inputFileName | const System::String\& | Le nom du fichier d'entrée. |
| outputFileName | const System::String\& | Le nom de fichier de sortie utilisé pour générer le nom de fichier des parties du document selon la règle "outputFile_partIndex.extension" |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Les options d'enregistrement. |
| options | const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\& | [Document](../../../aspose.words/document/) options de division. |

## Voir aussi

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [SplitOptions](../../splitoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
