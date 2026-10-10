---
title: "Aspose::Words::LowCode::Splitter::RemoveBlankPages metodo"
linktitle: "RemoveBlankPages"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::LowCode::Splitter::RemoveBlankPages metodo. Rimuove le pagine vuote da un documento fornito in un flusso di input e salva il documento aggiornato in un flusso di output nel formato di salvataggio specificato. Restituisce un elenco di numeri di pagina che sono stati rimossi in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.lowcode/splitter/removeblankpages/
---
## Splitter::RemoveBlankPages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) method


Rimuove le pagine bianche da un documento fornito in un flusso di input e salva il documento aggiornato in un flusso di output nel formato di salvataggio specificato. Restituisce un elenco di numeri di pagina che sono stati rimossi.

```cpp
static System::SharedPtr<System::Collections::Generic::List<int32_t>> Aspose::Words::LowCode::Splitter::RemoveBlankPages(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Il flusso di input. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Lo stream di output. |
| saveFormat | Aspose::Words::SaveFormat | Il formato di salvataggio. |

### ReturnValue

L'elenco dei numeri di pagina è stato considerato vuoto e rimosso.

## Vedi anche

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::RemoveBlankPages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) method


Rimuove le pagine bianche da un documento fornito in un flusso di input e salva il documento aggiornato in un flusso di output nel formato di salvataggio specificato. Restituisce un elenco di numeri di pagina che sono stati rimossi.

```cpp
static System::SharedPtr<System::Collections::Generic::List<int32_t>> Aspose::Words::LowCode::Splitter::RemoveBlankPages(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Il flusso di input. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Lo stream di output. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Le opzioni di salvataggio. |

### ReturnValue

L'elenco dei numeri di pagina è stato considerato vuoto e rimosso.

## Vedi anche

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::RemoveBlankPages(const System::String\&, const System::String\&) method


Rimuove le pagine vuote dal documento e salva l'output. Restituisce un elenco di numeri di pagina che sono stati rimossi.

```cpp
static System::SharedPtr<System::Collections::Generic::List<int32_t>> Aspose::Words::LowCode::Splitter::RemoveBlankPages(const System::String &inputFileName, const System::String &outputFileName)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | const System::String\& | Il nome del file di input. |
| outputFileName | const System::String\& | Il nome del file di output. |

### ReturnValue

L'elenco dei numeri di pagina è stato considerato vuoto e rimosso.

## Vedi anche

* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::RemoveBlankPages(const System::String\&, const System::String\&, Aspose::Words::SaveFormat) method


Rimuove le pagine vuote dal documento e salva l'output nel formato specificato. Restituisce un elenco di numeri di pagina che sono stati rimossi.

```cpp
static System::SharedPtr<System::Collections::Generic::List<int32_t>> Aspose::Words::LowCode::Splitter::RemoveBlankPages(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | const System::String\& | Il nome del file di input. |
| outputFileName | const System::String\& | Il nome del file di output. |
| saveFormat | Aspose::Words::SaveFormat | Il formato di salvataggio. |

### ReturnValue

L'elenco dei numeri di pagina è stato considerato vuoto e rimosso.

## Vedi anche

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::RemoveBlankPages(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) method


Rimuove le pagine vuote dal documento e salva l'output nel formato specificato. Restituisce un elenco di numeri di pagina che sono stati rimossi.

```cpp
static System::SharedPtr<System::Collections::Generic::List<int32_t>> Aspose::Words::LowCode::Splitter::RemoveBlankPages(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | const System::String\& | Il nome del file di input. |
| outputFileName | const System::String\& | Il nome del file di output. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Le opzioni di salvataggio. |

### ReturnValue

L'elenco dei numeri di pagina è stato considerato vuoto e rimosso.

## Vedi anche

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
