---
title: "Aspose::Words::LowCode::Comparer::CompareToImages‑Methode"
linktitle: "CompareToImages"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::LowCode::Comparer::CompareToImages‑Methode. Vergleicht zwei Dokumente und speichert die Unterschiede als Bilder. Jeder Eintrag im zurückgegebenen Array stellt eine einzelne Seite der Ausgabe dar, die in C++ als Bild gerendert wird."
type: docs
weight: 2000
url: /de/cpp/aspose.words.lowcode/comparer/comparetoimages/
---
## Comparer::CompareToImages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, System::DateTime) method


Vergleicht zwei Dokumente und speichert die Unterschiede als Bilder. Jeder Eintrag im zurückgegebenen Array stellt eine einzelne Seite der Ausgabe dar, die als Bild gerendert wird.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Comparer::CompareToImages(const System::SharedPtr<System::IO::Stream> &v1, const System::SharedPtr<System::IO::Stream> &v2, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &imageSaveOptions, const System::String &author, System::DateTime dateTime)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| v1 | const System::SharedPtr\<System::IO::Stream\>\& | Das Originaldokument. |
| v2 | const System::SharedPtr\<System::IO::Stream\>\& | Das geänderte Dokument. |
| imageSaveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Die Bildspeicheroptionen der Ausgabe. |
| Autor | const System::String\& | Initialen des Autors, die für Revisionen verwendet werden. |
| dateTime | System::DateTime | Das Datum und die Uhrzeit, die für Revisionen verwendet werden sollen. |

## Siehe auch

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::CompareToImages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) method


Vergleicht zwei Dokumente und speichert die Unterschiede als Bilder. Jeder Eintrag im zurückgegebenen Array stellt eine einzelne Seite der Ausgabe dar, die als Bild gerendert wird.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Comparer::CompareToImages(const System::SharedPtr<System::IO::Stream> &v1, const System::SharedPtr<System::IO::Stream> &v2, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &imageSaveOptions, const System::String &author, System::DateTime dateTime, const System::SharedPtr<Aspose::Words::Comparing::CompareOptions> &compareOptions)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| v1 | const System::SharedPtr\<System::IO::Stream\>\& | Das Originaldokument. |
| v2 | const System::SharedPtr\<System::IO::Stream\>\& | Das geänderte Dokument. |
| imageSaveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Die Bildspeicheroptionen der Ausgabe. |
| Autor | const System::String\& | Initialen des Autors, die für Revisionen verwendet werden. |
| dateTime | System::DateTime | Das Datum und die Uhrzeit, die für Revisionen verwendet werden sollen. |
| compareOptions | const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\& | Vergleichsoptionen für [Document](../../../aspose.words/document/). |

## Siehe auch

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::CompareToImages(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, System::DateTime) method


Vergleicht zwei Dokumente und speichert die Unterschiede als Bilder. Jeder Eintrag im zurückgegebenen Array stellt eine einzelne Seite der Ausgabe dar, die als Bild gerendert wird.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Comparer::CompareToImages(const System::String &v1, const System::String &v2, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &imageSaveOptions, const System::String &author, System::DateTime dateTime)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| v1 | const System::String\& | Das Originaldokument. |
| v2 | const System::String\& | Das geänderte Dokument. |
| imageSaveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Die Bildspeicheroptionen der Ausgabe. |
| Autor | const System::String\& | Initialen des Autors, die für Revisionen verwendet werden. |
| dateTime | System::DateTime | Das Datum und die Uhrzeit, die für Revisionen verwendet werden sollen. |

## Siehe auch

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::CompareToImages(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) method


Vergleicht zwei Dokumente und speichert die Unterschiede als Bilder. Jeder Eintrag im zurückgegebenen Array stellt eine einzelne Seite der Ausgabe dar, die als Bild gerendert wird.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Comparer::CompareToImages(const System::String &v1, const System::String &v2, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &imageSaveOptions, const System::String &author, System::DateTime dateTime, const System::SharedPtr<Aspose::Words::Comparing::CompareOptions> &compareOptions)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| v1 | const System::String\& | Das Originaldokument. |
| v2 | const System::String\& | Das geänderte Dokument. |
| imageSaveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Die Bildspeicheroptionen der Ausgabe. |
| Autor | const System::String\& | Initialen des Autors, die für Revisionen verwendet werden. |
| dateTime | System::DateTime | Das Datum und die Uhrzeit, die für Revisionen verwendet werden sollen. |
| compareOptions | const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\& | Vergleichsoptionen für [Document](../../../aspose.words/document/). |

## Siehe auch

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
