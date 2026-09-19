---
title: "Aspose::Words::LowCode::Watermarker::SetText metodo"
linktitle: "SetText"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::LowCode::Watermarker::SetText metodo. Aggiunge una filigrana di testo al documento da flussi con opzioni in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.lowcode/watermarker/settext/
---
## Watermarker::SetText(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&) method


Aggiunge una filigrana di testo al documento da flussi con opzioni.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetText(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::String &watermarkText)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Il flusso di input. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Lo stream di output. |
| saveFormat | Aspose::Words::SaveFormat | Il formato di salvataggio. |
| watermarkText | const System::String\& | Testo visualizzato come filigrana. |
## Note


Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo la prima pagina dell'output verrà salvata nello stream specificato.

Se il formato di output è TIFF, l'output verrà salvato come un singolo TIFF multi-frame nello stream specificato.

## Vedi anche

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetText(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) method


Aggiunge una filigrana di testo al documento da flussi con opzioni.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetText(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::String &watermarkText, const System::SharedPtr<Aspose::Words::TextWatermarkOptions> &options)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Il flusso di input. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Lo stream di output. |
| saveFormat | Aspose::Words::SaveFormat | Il formato di salvataggio. |
| watermarkText | const System::String\& | Testo visualizzato come filigrana. |
| opzioni | const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\& | Definisce opzioni aggiuntive per la filigrana di testo. |
## Note


Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo la prima pagina dell'output verrà salvata nello stream specificato.

Se il formato di output è TIFF, l'output verrà salvato come un singolo TIFF multi-frame nello stream specificato.

## Vedi anche

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetText(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&) method


Aggiunge una filigrana di testo al documento da flussi con opzioni.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetText(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &watermarkText)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Il flusso di input. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Lo stream di output. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Le opzioni di salvataggio. |
| watermarkText | const System::String\& | Testo visualizzato come filigrana. |
## Note


Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo la prima pagina dell'output verrà salvata nello stream specificato.

Se il formato di output è TIFF, l'output verrà salvato come un singolo TIFF multi-frame nello stream specificato.

## Vedi anche

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetText(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) method


Aggiunge una filigrana di testo al documento da flussi con opzioni.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetText(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &watermarkText, const System::SharedPtr<Aspose::Words::TextWatermarkOptions> &options)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Il flusso di input. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Lo stream di output. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Le opzioni di salvataggio. |
| watermarkText | const System::String\& | Testo visualizzato come filigrana. |
| opzioni | const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\& | Definisce opzioni aggiuntive per la filigrana di testo. |
## Note


Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo la prima pagina dell'output verrà salvata nello stream specificato.

Se il formato di output è TIFF, l'output verrà salvato come un singolo TIFF multi-frame nello stream specificato.

## Vedi anche

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetText(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&) method


Aggiunge una filigrana di testo al documento con opzioni e formato di salvataggio specificato.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetText(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::String &watermarkText)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | const System::String\& | Il nome del file di input. |
| outputFileName | const System::String\& | Il nome del file di output. |
| saveFormat | Aspose::Words::SaveFormat | Il formato di salvataggio. |
| watermarkText | const System::String\& | Testo visualizzato come filigrana. |
## Note


Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), ogni pagina dell'output verrà salvata come file separato. Il nome del file di output specificato verrà usato per generare i nomi dei file per ogni parte secondo la regola: outputFile_partIndex.extension.

Se il formato di output è TIFF, l'output verrà salvato come un unico file TIFF multi-frame.

## Vedi anche

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetText(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) method


Aggiunge una filigrana di testo al documento con opzioni e formato di salvataggio specificato.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetText(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::String &watermarkText, const System::SharedPtr<Aspose::Words::TextWatermarkOptions> &options)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | const System::String\& | Il nome del file di input. |
| outputFileName | const System::String\& | Il nome del file di output. |
| saveFormat | Aspose::Words::SaveFormat | Il formato di salvataggio. |
| watermarkText | const System::String\& | Testo visualizzato come filigrana. |
| opzioni | const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\& | Definisce opzioni aggiuntive per la filigrana di testo. |
## Note


Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), ogni pagina dell'output verrà salvata come file separato. Il nome del file di output specificato verrà usato per generare i nomi dei file per ogni parte secondo la regola: outputFile_partIndex.extension.

Se il formato di output è TIFF, l'output verrà salvato come un unico file TIFF multi-frame.

## Vedi anche

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetText(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&) method


Aggiunge una filigrana di testo al documento con opzioni e formato di salvataggio specificato.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetText(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &watermarkText)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | const System::String\& | Il nome del file di input. |
| outputFileName | const System::String\& | Il nome del file di output. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Le opzioni di salvataggio. |
| watermarkText | const System::String\& | Testo visualizzato come filigrana. |
## Note


Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), ogni pagina dell'output verrà salvata come file separato. Il nome del file di output specificato verrà usato per generare i nomi dei file per ogni parte secondo la regola: outputFile_partIndex.extension.

Se il formato di output è TIFF, l'output verrà salvato come un unico file TIFF multi-frame.

## Vedi anche

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetText(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) method


Aggiunge una filigrana di testo al documento con opzioni e formato di salvataggio specificato.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetText(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &watermarkText, const System::SharedPtr<Aspose::Words::TextWatermarkOptions> &options)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | const System::String\& | Il nome del file di input. |
| outputFileName | const System::String\& | Il nome del file di output. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Le opzioni di salvataggio. |
| watermarkText | const System::String\& | Testo visualizzato come filigrana. |
| opzioni | const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\& | Definisce opzioni aggiuntive per la filigrana di testo. |
## Note


Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), ogni pagina dell'output verrà salvata come file separato. Il nome del file di output specificato verrà usato per generare i nomi dei file per ogni parte secondo la regola: outputFile_partIndex.extension.

Se il formato di output è TIFF, l'output verrà salvato come un unico file TIFF multi-frame.

## Vedi anche

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetText(const System::String\&, const System::String\&, const System::String\&) method


Aggiunge una filigrana di testo al documento.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetText(const System::String &inputFileName, const System::String &outputFileName, const System::String &watermarkText)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | const System::String\& | Il nome del file di input. |
| outputFileName | const System::String\& | Il nome del file di output. |
| watermarkText | const System::String\& | Testo visualizzato come filigrana. |
## Note


Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), ogni pagina dell'output verrà salvata come file separato. Il nome del file di output specificato verrà usato per generare i nomi dei file per ogni parte secondo la regola: outputFile_partIndex.extension.

Se il formato di output è TIFF, l'output verrà salvato come un unico file TIFF multi-frame.

## Vedi anche

* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetText(const System::String\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) method


Aggiunge una filigrana di testo al documento con opzioni.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetText(const System::String &inputFileName, const System::String &outputFileName, const System::String &watermarkText, const System::SharedPtr<Aspose::Words::TextWatermarkOptions> &options)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | const System::String\& | Il nome del file di input. |
| outputFileName | const System::String\& | Il nome del file di output. |
| watermarkText | const System::String\& | Testo visualizzato come filigrana. |
| opzioni | const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\& | Definisce opzioni aggiuntive per la filigrana di testo. |
## Note


Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), ogni pagina dell'output verrà salvata come file separato. Il nome del file di output specificato verrà usato per generare i nomi dei file per ogni parte secondo la regola: outputFile_partIndex.extension.

Se il formato di output è TIFF, l'output verrà salvato come un unico file TIFF multi-frame.

## Vedi anche

* Class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
