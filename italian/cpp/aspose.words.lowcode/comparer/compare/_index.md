---
title: "Aspose::Words::LowCode::Comparer::Compare method"
linktitle: "Compare"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::LowCode::Comparer::Compare method. Confronta due documenti caricati da stream con opzioni aggiuntive e salva le differenze nello stream di output fornito nel formato di salvataggio specificato, producendo modifiche sotto forma di un numero di revisioni di modifica e di formato in C++."
type: docs
weight: 1000
url: /it/cpp/aspose.words.lowcode/comparer/compare/
---
## Comparer::Compare(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime) method


Confronta due documenti caricati da flussi con opzioni aggiuntive e salva le differenze nel flusso di output fornito nel formato di salvataggio specificato, producendo modifiche come un numero di revisioni di modifica e formattazione.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::SharedPtr<System::IO::Stream> &v1, const System::SharedPtr<System::IO::Stream> &v2, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::String &author, System::DateTime dateTime)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| v1 | const System::SharedPtr\<System::IO::Stream\>\& | Il documento originale. |
| v2 | const System::SharedPtr\<System::IO::Stream\>\& | Il documento modificato. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Lo stream di output. |
| saveFormat | Aspose::Words::SaveFormat | Il formato di salvataggio dell'output. |
| autore | const System::String\& | Iniziali dell'autore da utilizzare per le revisioni. |
| dateTime | System::DateTime | La data e l'ora da utilizzare per le revisioni. |
## Note


Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo la prima pagina dell'output verrà salvata nello stream specificato.

Se il formato di output è TIFF, l'output verrà salvato come un singolo TIFF multi-frame nello stream specificato.

## Vedi anche

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) method


Confronta due documenti caricati da flussi con opzioni aggiuntive e salva le differenze nel flusso di output fornito nel formato di salvataggio specificato, producendo modifiche come un numero di revisioni di modifica e formattazione.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::SharedPtr<System::IO::Stream> &v1, const System::SharedPtr<System::IO::Stream> &v2, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::String &author, System::DateTime dateTime, const System::SharedPtr<Aspose::Words::Comparing::CompareOptions> &compareOptions)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| v1 | const System::SharedPtr\<System::IO::Stream\>\& | Il documento originale. |
| v2 | const System::SharedPtr\<System::IO::Stream\>\& | Il documento modificato. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Lo stream di output. |
| saveFormat | Aspose::Words::SaveFormat | Il formato di salvataggio dell'output. |
| autore | const System::String\& | Iniziali dell'autore da utilizzare per le revisioni. |
| dateTime | System::DateTime | La data e l'ora da utilizzare per le revisioni. |
| compareOptions | const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\& | opzioni di confronto del [Document](../../../aspose.words/document/). |
## Note


Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo la prima pagina dell'output verrà salvata nello stream specificato.

Se il formato di output è TIFF, l'output verrà salvato come un singolo TIFF multi-frame nello stream specificato.

## Vedi anche

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime) method


Confronta due documenti caricati da flussi con opzioni aggiuntive e salva le differenze nel flusso di output fornito nel formato di salvataggio specificato, producendo modifiche come un numero di revisioni di modifica e formattazione.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::SharedPtr<System::IO::Stream> &v1, const System::SharedPtr<System::IO::Stream> &v2, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &author, System::DateTime dateTime)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| v1 | const System::SharedPtr\<System::IO::Stream\>\& | Il documento originale. |
| v2 | const System::SharedPtr\<System::IO::Stream\>\& | Il documento modificato. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Lo stream di output. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Le opzioni di salvataggio dell'output. |
| autore | const System::String\& | Iniziali dell'autore da utilizzare per le revisioni. |
| dateTime | System::DateTime | La data e l'ora da utilizzare per le revisioni. |
## Note


Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo la prima pagina dell'output verrà salvata nello stream specificato.

Se il formato di output è TIFF, l'output verrà salvato come un singolo TIFF multi-frame nello stream specificato.

## Vedi anche

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) method


Confronta due documenti caricati da flussi con opzioni aggiuntive e salva le differenze nel flusso di output fornito nel formato di salvataggio specificato, producendo modifiche come un numero di revisioni di modifica e formattazione.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::SharedPtr<System::IO::Stream> &v1, const System::SharedPtr<System::IO::Stream> &v2, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &author, System::DateTime dateTime, const System::SharedPtr<Aspose::Words::Comparing::CompareOptions> &compareOptions)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| v1 | const System::SharedPtr\<System::IO::Stream\>\& | Il documento originale. |
| v2 | const System::SharedPtr\<System::IO::Stream\>\& | Il documento modificato. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Lo stream di output. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Le opzioni di salvataggio dell'output. |
| autore | const System::String\& | Iniziali dell'autore da utilizzare per le revisioni. |
| dateTime | System::DateTime | La data e l'ora da utilizzare per le revisioni. |
| compareOptions | const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\& | opzioni di confronto del [Document](../../../aspose.words/document/). |
## Note


Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo la prima pagina dell'output verrà salvata nello stream specificato.

Se il formato di output è TIFF, l'output verrà salvato come un singolo TIFF multi-frame nello stream specificato.

## Vedi anche

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::String\&, const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime) method


Confronta due documenti con opzioni aggiuntive e salva le differenze nel file di output specificato nel formato di salvataggio fornito, producendo modifiche come un numero di revisioni di modifica e formattazione.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::String &v1, const System::String &v2, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::String &author, System::DateTime dateTime)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| v1 | const System::String\& | Il documento originale. |
| v2 | const System::String\& | Il documento modificato. |
| outputFileName | const System::String\& | Il nome del file di output. |
| saveFormat | Aspose::Words::SaveFormat | Il formato di salvataggio dell'output. |
| autore | const System::String\& | Iniziali dell'autore da utilizzare per le revisioni. |
| dateTime | System::DateTime | La data e l'ora da utilizzare per le revisioni. |
## Note


Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), ogni pagina dell'output verrà salvata come file separato. Il nome del file di output specificato verrà usato per generare i nomi dei file per ogni parte secondo la regola: outputFile_partIndex.extension.

Se il formato di output è TIFF, l'output verrà salvato come un unico file TIFF multi-frame.

## Vedi anche

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::String\&, const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) method


Confronta due documenti con opzioni aggiuntive e salva le differenze nel file di output specificato nel formato di salvataggio fornito, producendo modifiche come un numero di revisioni di modifica e formattazione.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::String &v1, const System::String &v2, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::String &author, System::DateTime dateTime, const System::SharedPtr<Aspose::Words::Comparing::CompareOptions> &compareOptions)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| v1 | const System::String\& | Il documento originale. |
| v2 | const System::String\& | Il documento modificato. |
| outputFileName | const System::String\& | Il nome del file di output. |
| saveFormat | Aspose::Words::SaveFormat | Il formato di salvataggio dell'output. |
| autore | const System::String\& | Iniziali dell'autore da utilizzare per le revisioni. |
| dateTime | System::DateTime | La data e l'ora da utilizzare per le revisioni. |
| compareOptions | const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\& | opzioni di confronto del [Document](../../../aspose.words/document/). |
## Note


Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), ogni pagina dell'output verrà salvata come file separato. Il nome del file di output specificato verrà usato per generare i nomi dei file per ogni parte secondo la regola: outputFile_partIndex.extension.

Se il formato di output è TIFF, l'output verrà salvato come un unico file TIFF multi-frame.

## Vedi anche

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::String\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime) method


Confronta due documenti con opzioni aggiuntive e salva le differenze nel file di output specificato nel formato di salvataggio fornito, producendo modifiche come un numero di revisioni di modifica e formattazione.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::String &v1, const System::String &v2, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &author, System::DateTime dateTime)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| v1 | const System::String\& | Il documento originale. |
| v2 | const System::String\& | Il documento modificato. |
| outputFileName | const System::String\& | Il nome del file di output. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Le opzioni di salvataggio dell'output. |
| autore | const System::String\& | Iniziali dell'autore da utilizzare per le revisioni. |
| dateTime | System::DateTime | La data e l'ora da utilizzare per le revisioni. |
## Note


Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), ogni pagina dell'output verrà salvata come file separato. Il nome del file di output specificato verrà usato per generare i nomi dei file per ogni parte secondo la regola: outputFile_partIndex.extension.

Se il formato di output è TIFF, l'output verrà salvato come un unico file TIFF multi-frame.

## Vedi anche

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::String\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) method


Confronta due documenti con opzioni aggiuntive e salva le differenze nel file di output specificato nel formato di salvataggio fornito, producendo modifiche come un numero di revisioni di modifica e formattazione.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::String &v1, const System::String &v2, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &author, System::DateTime dateTime, const System::SharedPtr<Aspose::Words::Comparing::CompareOptions> &compareOptions)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| v1 | const System::String\& | Il documento originale. |
| v2 | const System::String\& | Il documento modificato. |
| outputFileName | const System::String\& | Il nome del file di output. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Le opzioni di salvataggio dell'output. |
| autore | const System::String\& | Iniziali dell'autore da utilizzare per le revisioni. |
| dateTime | System::DateTime | La data e l'ora da utilizzare per le revisioni. |
| compareOptions | const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\& | opzioni di confronto del [Document](../../../aspose.words/document/). |
## Note


Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), ogni pagina dell'output verrà salvata come file separato. Il nome del file di output specificato verrà usato per generare i nomi dei file per ogni parte secondo la regola: outputFile_partIndex.extension.

Se il formato di output è TIFF, l'output verrà salvato come un unico file TIFF multi-frame.

## Vedi anche

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::String\&, const System::String\&, const System::String\&, const System::String\&, System::DateTime) method


Confronta due documenti con opzioni aggiuntive e salva le differenze nel file di output specificato, producendo modifiche come un numero di revisioni di modifica e formattazione.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::String &v1, const System::String &v2, const System::String &outputFileName, const System::String &author, System::DateTime dateTime)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| v1 | const System::String\& | Il documento originale. |
| v2 | const System::String\& | Il documento modificato. |
| outputFileName | const System::String\& | Il nome del file di output. |
| autore | const System::String\& | Iniziali dell'autore da utilizzare per le revisioni. |
| dateTime | System::DateTime | La data e l'ora da utilizzare per le revisioni. |
## Note


Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), ogni pagina dell'output verrà salvata come file separato. Il nome del file di output specificato verrà usato per generare i nomi dei file per ogni parte secondo la regola: outputFile_partIndex.extension.

Se il formato di output è TIFF, l'output verrà salvato come un unico file TIFF multi-frame.

## Vedi anche

* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::String\&, const System::String\&, const System::String\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) method


Confronta due documenti con opzioni aggiuntive e salva le differenze nel file di output specificato, producendo modifiche come un numero di revisioni di modifica e formattazione.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::String &v1, const System::String &v2, const System::String &outputFileName, const System::String &author, System::DateTime dateTime, const System::SharedPtr<Aspose::Words::Comparing::CompareOptions> &compareOptions)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| v1 | const System::String\& | Il documento originale. |
| v2 | const System::String\& | Il documento modificato. |
| outputFileName | const System::String\& | Il nome del file di output. |
| autore | const System::String\& | Iniziali dell'autore da utilizzare per le revisioni. |
| dateTime | System::DateTime | La data e l'ora da utilizzare per le revisioni. |
| compareOptions | const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\& | opzioni di confronto del [Document](../../../aspose.words/document/). |
## Note


Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), ogni pagina dell'output verrà salvata come file separato. Il nome del file di output specificato verrà usato per generare i nomi dei file per ogni parte secondo la regola: outputFile_partIndex.extension.

Se il formato di output è TIFF, l'output verrà salvato come un unico file TIFF multi-frame.

## Vedi anche

* Class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
