---
title: "Aspose::Words::LowCode::Splitter::ExtractPages metod"
linktitle: "ExtractPages"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::LowCode::Splitter::ExtractPages metod. Extraherar ett specificerat sidintervall från ett dokumentflöde och sparar de extraherade sidorna till ett utflöde med det angivna sparformatet i C++."
type: docs
weight: 1000
url: /sv/cpp/aspose.words.lowcode/splitter/extractpages/
---
## Splitter::ExtractPages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, int32_t, int32_t) method


Extraherar ett specificerat sidintervall från en dokumentström och sparar de extraherade sidorna till en utdataström med det angivna sparformatet.

```cpp
static void Aspose::Words::LowCode::Splitter::ExtractPages(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, int32_t startPageIndex, int32_t pageCount)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Inmatningsströmmen. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Utdataflödet. |
| saveFormat | Aspose::Words::SaveFormat | Sparformatet. |
| startPageIndex | int32_t | Det nollbaserade indexet för den första sidan som ska extraheras. |
| pageCount | int32_t | Antal sidor som ska extraheras. |

## Se även

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::ExtractPages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, int32_t, int32_t) method


Extraherar ett specificerat sidintervall från en dokumentström och sparar de extraherade sidorna till en utdataström med det angivna sparformatet.

```cpp
static void Aspose::Words::LowCode::Splitter::ExtractPages(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, int32_t startPageIndex, int32_t pageCount)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Inmatningsströmmen. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Utdataflödet. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Sparalternativen. |
| startPageIndex | int32_t | Det nollbaserade indexet för den första sidan som ska extraheras. |
| pageCount | int32_t | Antal sidor som ska extraheras. |

## Se även

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::ExtractPages(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, int32_t, int32_t) method


Extraherar ett specificerat sidintervall från en dokumentfil och sparar de extraherade sidorna till en ny fil med det angivna sparformatet.

```cpp
static void Aspose::Words::LowCode::Splitter::ExtractPages(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, int32_t startPageIndex, int32_t pageCount)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputFileName | const System::String\& | Inmatningsfilnamnet. |
| outputFileName | const System::String\& | Utdatans filnamn. |
| saveFormat | Aspose::Words::SaveFormat | Sparformatet. |
| startPageIndex | int32_t | Det nollbaserade indexet för den första sidan som ska extraheras. |
| pageCount | int32_t | Antal sidor som ska extraheras. |

## Se även

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::ExtractPages(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, int32_t, int32_t) method


Extraherar ett specificerat sidintervall från en dokumentfil och sparar de extraherade sidorna till en ny fil med det angivna sparformatet.

```cpp
static void Aspose::Words::LowCode::Splitter::ExtractPages(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, int32_t startPageIndex, int32_t pageCount)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputFileName | const System::String\& | Inmatningsfilnamnet. |
| outputFileName | const System::String\& | Utdatans filnamn. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Sparalternativen. |
| startPageIndex | int32_t | Det nollbaserade indexet för den första sidan som ska extraheras. |
| pageCount | int32_t | Antal sidor som ska extraheras. |

## Se även

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::ExtractPages(const System::String\&, const System::String\&, int32_t, int32_t) method


Extraherar ett specificerat sidintervall från en dokumentfil och sparar de extraherade sidorna till en ny fil. Utdatafilens format bestäms av filnamnets filändelse.

```cpp
static void Aspose::Words::LowCode::Splitter::ExtractPages(const System::String &inputFileName, const System::String &outputFileName, int32_t startPageIndex, int32_t pageCount)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputFileName | const System::String\& | Inmatningsfilnamnet. |
| outputFileName | const System::String\& | Utdatans filnamn. |
| startPageIndex | int32_t | Det nollbaserade indexet för den första sidan som ska extraheras. |
| pageCount | int32_t | Antal sidor som ska extraheras. |

## Se även

* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
