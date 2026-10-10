---
title: "Aspose::Words::LowCode::Splitter::RemoveBlankPages metod"
linktitle: "RemoveBlankPages"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::LowCode::Splitter::RemoveBlankPages metod. Tar bort tomma sidor från ett dokument som tillhandahålls i ett inmatningsflöde och sparar det uppdaterade dokumentet till ett utflöde i det angivna sparformatet. Returnerar en lista med sidnummer som togs bort i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.lowcode/splitter/removeblankpages/
---
## Splitter::RemoveBlankPages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) method


Tar bort blanka sidor från ett dokument som tillhandahålls i en inmatningsström och sparar det uppdaterade dokumentet till en utdataström i det angivna sparformatet. Returnerar en lista med sidnummer som togs bort.

```cpp
static System::SharedPtr<System::Collections::Generic::List<int32_t>> Aspose::Words::LowCode::Splitter::RemoveBlankPages(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Inmatningsströmmen. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Utdataflödet. |
| saveFormat | Aspose::Words::SaveFormat | Sparformatet. |

### ReturnValue

Lista med sidnummer har betraktats som tomma och tagits bort.

## Se även

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::RemoveBlankPages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) method


Tar bort blanka sidor från ett dokument som tillhandahålls i en inmatningsström och sparar det uppdaterade dokumentet till en utdataström i det angivna sparformatet. Returnerar en lista med sidnummer som togs bort.

```cpp
static System::SharedPtr<System::Collections::Generic::List<int32_t>> Aspose::Words::LowCode::Splitter::RemoveBlankPages(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Inmatningsströmmen. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Utdataflödet. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Sparalternativen. |

### ReturnValue

Lista med sidnummer har betraktats som tomma och tagits bort.

## Se även

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::RemoveBlankPages(const System::String\&, const System::String\&) method


Tar bort tomma sidor från dokumentet och sparar resultatet. Returnerar en lista med sidnummer som togs bort.

```cpp
static System::SharedPtr<System::Collections::Generic::List<int32_t>> Aspose::Words::LowCode::Splitter::RemoveBlankPages(const System::String &inputFileName, const System::String &outputFileName)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputFileName | const System::String\& | Inmatningsfilnamnet. |
| outputFileName | const System::String\& | Utdatans filnamn. |

### ReturnValue

Lista med sidnummer har betraktats som tomma och tagits bort.

## Se även

* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::RemoveBlankPages(const System::String\&, const System::String\&, Aspose::Words::SaveFormat) method


Tar bort tomma sidor från dokumentet och sparar resultatet i det specificerade formatet. Returnerar en lista med sidnummer som togs bort.

```cpp
static System::SharedPtr<System::Collections::Generic::List<int32_t>> Aspose::Words::LowCode::Splitter::RemoveBlankPages(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputFileName | const System::String\& | Inmatningsfilnamnet. |
| outputFileName | const System::String\& | Utdatans filnamn. |
| saveFormat | Aspose::Words::SaveFormat | Sparformatet. |

### ReturnValue

Lista med sidnummer har betraktats som tomma och tagits bort.

## Se även

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::RemoveBlankPages(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) method


Tar bort tomma sidor från dokumentet och sparar resultatet i det specificerade formatet. Returnerar en lista med sidnummer som togs bort.

```cpp
static System::SharedPtr<System::Collections::Generic::List<int32_t>> Aspose::Words::LowCode::Splitter::RemoveBlankPages(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputFileName | const System::String\& | Inmatningsfilnamnet. |
| outputFileName | const System::String\& | Utdatans filnamn. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Sparalternativen. |

### ReturnValue

Lista med sidnummer har betraktats som tomma och tagits bort.

## Se även

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
