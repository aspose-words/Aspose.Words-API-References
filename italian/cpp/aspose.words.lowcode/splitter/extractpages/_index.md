---
title: "Aspose::Words::LowCode::Splitter::ExtractPages metodo"
linktitle: "ExtractPages"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::LowCode::Splitter::ExtractPages metodo. Estrae un intervallo specificato di pagine da un flusso di documento e salva le pagine estratte in un flusso di output usando il formato di salvataggio specificato in C++."
type: docs
weight: 1000
url: /it/cpp/aspose.words.lowcode/splitter/extractpages/
---
## Splitter::ExtractPages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, int32_t, int32_t) method


Estrae un intervallo specificato di pagine da un flusso di documento e salva le pagine estratte in un flusso di output usando il formato di salvataggio specificato.

```cpp
static void Aspose::Words::LowCode::Splitter::ExtractPages(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, int32_t startPageIndex, int32_t pageCount)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Il flusso di input. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Lo stream di output. |
| saveFormat | Aspose::Words::SaveFormat | Il formato di salvataggio. |
| startPageIndex | int32_t | L'indice basato su zero della prima pagina da estrarre. |
| pageCount | int32_t | Numero di pagine da estrarre. |

## Vedi anche

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::ExtractPages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, int32_t, int32_t) method


Estrae un intervallo specificato di pagine da un flusso di documento e salva le pagine estratte in un flusso di output usando il formato di salvataggio specificato.

```cpp
static void Aspose::Words::LowCode::Splitter::ExtractPages(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, int32_t startPageIndex, int32_t pageCount)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Il flusso di input. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Lo stream di output. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Le opzioni di salvataggio. |
| startPageIndex | int32_t | L'indice basato su zero della prima pagina da estrarre. |
| pageCount | int32_t | Numero di pagine da estrarre. |

## Vedi anche

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::ExtractPages(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, int32_t, int32_t) method


Estrae un intervallo specificato di pagine da un file documento e salva le pagine estratte in un nuovo file utilizzando il formato di salvataggio specificato.

```cpp
static void Aspose::Words::LowCode::Splitter::ExtractPages(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, int32_t startPageIndex, int32_t pageCount)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | const System::String\& | Il nome del file di input. |
| outputFileName | const System::String\& | Il nome del file di output. |
| saveFormat | Aspose::Words::SaveFormat | Il formato di salvataggio. |
| startPageIndex | int32_t | L'indice basato su zero della prima pagina da estrarre. |
| pageCount | int32_t | Numero di pagine da estrarre. |

## Vedi anche

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::ExtractPages(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, int32_t, int32_t) method


Estrae un intervallo specificato di pagine da un file documento e salva le pagine estratte in un nuovo file utilizzando il formato di salvataggio specificato.

```cpp
static void Aspose::Words::LowCode::Splitter::ExtractPages(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, int32_t startPageIndex, int32_t pageCount)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | const System::String\& | Il nome del file di input. |
| outputFileName | const System::String\& | Il nome del file di output. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Le opzioni di salvataggio. |
| startPageIndex | int32_t | L'indice basato su zero della prima pagina da estrarre. |
| pageCount | int32_t | Numero di pagine da estrarre. |

## Vedi anche

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::ExtractPages(const System::String\&, const System::String\&, int32_t, int32_t) method


Estrae un intervallo specificato di pagine da un file documento e salva le pagine estratte in un nuovo file. Il formato del file di output è determinato dall'estensione del nome del file di output.

```cpp
static void Aspose::Words::LowCode::Splitter::ExtractPages(const System::String &inputFileName, const System::String &outputFileName, int32_t startPageIndex, int32_t pageCount)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | const System::String\& | Il nome del file di input. |
| outputFileName | const System::String\& | Il nome del file di output. |
| startPageIndex | int32_t | L'indice basato su zero della prima pagina da estrarre. |
| pageCount | int32_t | Numero di pagine da estrarre. |

## Vedi anche

* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
