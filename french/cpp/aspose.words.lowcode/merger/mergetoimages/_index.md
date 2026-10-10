---
title: "Méthode MergeToImages de Aspose::Words::LowCode::Merger"
linktitle: "MergeToImages"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode MergeToImages de Aspose::Words::LowCode::Merger. Fusionne les flux de documents d'entrée fournis en un seul document de sortie en utilisant les options d'enregistrement d'image spécifiées. Rend la sortie sous forme d'images en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.lowcode/merger/mergetoimages/
---
## Merger::MergeToImages(const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) method


Fusionne les flux de documents d'entrée fournis en un seul document de sortie en utilisant les options d'enregistrement d'image spécifiées. Rend la sortie sous forme d'images.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Merger::MergeToImages(const System::ArrayPtr<System::SharedPtr<System::IO::Stream>> &inputStreams, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions, Aspose::Words::LowCode::MergeFormatMode mergeFormatMode)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| inputStreams | const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\& | Les flux de fichiers d'entrée. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Les options d'enregistrement. |
| mergeFormatMode | Aspose::Words::LowCode::MergeFormatMode | Spécifie comment fusionner le formatage qui entre en conflit. |

## Voir aussi

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Enum [MergeFormatMode](../../mergeformatmode/)
* Class [Merger](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Merger::MergeToImages(const System::ArrayPtr\<System::String\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) method


Fusionne les documents d'entrée fournis en un seul document de sortie en utilisant les noms de fichiers d'entrée et de sortie spécifiés et les options d'enregistrement. Rend la sortie sous forme d'images.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Merger::MergeToImages(const System::ArrayPtr<System::String> &inputFiles, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions, Aspose::Words::LowCode::MergeFormatMode mergeFormatMode)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| inputFiles | const System::ArrayPtr\<System::String\>\& | Les noms de fichiers d'entrée. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Les options d'enregistrement. |
| mergeFormatMode | Aspose::Words::LowCode::MergeFormatMode | Spécifie comment fusionner le formatage qui entre en conflit. |

## Voir aussi

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Enum [MergeFormatMode](../../mergeformatmode/)
* Class [Merger](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
