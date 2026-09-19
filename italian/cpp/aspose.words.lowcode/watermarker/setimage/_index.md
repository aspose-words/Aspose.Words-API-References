---
title: "Aspose::Words::LowCode::Watermarker::SetImage metodo"
linktitle: "SetImage"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::LowCode::Watermarker::SetImage metodo. Aggiunge una filigrana immagine al documento da flussi con opzioni in C++."
type: docs
weight: 1000
url: /it/cpp/aspose.words.lowcode/watermarker/setimage/
---
## Watermarker::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Drawing::Image\>\&) method


Aggiunge una filigrana immagine al documento da flussi con opzioni.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<System::Drawing::Image> &watermarkImage)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Il flusso di input. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Lo stream di output. |
| saveFormat | Aspose::Words::SaveFormat | Il formato di salvataggio. |
| watermarkImage | const System::SharedPtr\<System::Drawing::Image\>\& | Immagine visualizzata come filigrana. |
## Note


Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo la prima pagina dell'output verrà salvata nello stream specificato.

Se il formato di output è TIFF, l'output verrà salvato come un singolo TIFF multi-frame nello stream specificato.

## Vedi anche

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Drawing::Image\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Aggiunge una filigrana immagine al documento da flussi con opzioni.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<System::Drawing::Image> &watermarkImage, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Il flusso di input. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Lo stream di output. |
| saveFormat | Aspose::Words::SaveFormat | Il formato di salvataggio. |
| watermarkImage | const System::SharedPtr\<System::Drawing::Image\>\& | Immagine visualizzata come filigrana. |
| opzioni | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Definisce opzioni aggiuntive per la filigrana immagine. |
## Note


Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo la prima pagina dell'output verrà salvata nello stream specificato.

Se il formato di output è TIFF, l'output verrà salvato come un singolo TIFF multi-frame nello stream specificato.

## Vedi anche

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::IO::Stream\>\&) method


Aggiunge una filigrana immagine al documento da flussi con opzioni.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<System::IO::Stream> &watermarkImageStream)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Il flusso di input. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Lo stream di output. |
| saveFormat | Aspose::Words::SaveFormat | Il formato di salvataggio. |
| watermarkImageStream | const System::SharedPtr\<System::IO::Stream\>\& | Stream immagine visualizzato come filigrana. |
## Note


Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo la prima pagina dell'output verrà salvata nello stream specificato.

Se il formato di output è TIFF, l'output verrà salvato come un singolo TIFF multi-frame nello stream specificato.

## Vedi anche

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Aggiunge una filigrana immagine al documento da flussi con opzioni.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<System::IO::Stream> &watermarkImageStream, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Il flusso di input. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Lo stream di output. |
| saveFormat | Aspose::Words::SaveFormat | Il formato di salvataggio. |
| watermarkImageStream | const System::SharedPtr\<System::IO::Stream\>\& | Stream immagine visualizzato come filigrana. |
| opzioni | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Definisce opzioni aggiuntive per la filigrana immagine. |
## Note


Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo la prima pagina dell'output verrà salvata nello stream specificato.

Se il formato di output è TIFF, l'output verrà salvato come un singolo TIFF multi-frame nello stream specificato.

## Vedi anche

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Drawing::Image\>\&) method


Aggiunge una filigrana immagine al documento da flussi con opzioni.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<System::Drawing::Image> &watermarkImage)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Il flusso di input. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Lo stream di output. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Le opzioni di salvataggio. |
| watermarkImage | const System::SharedPtr\<System::Drawing::Image\>\& | Immagine visualizzata come filigrana. |
## Note


Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo la prima pagina dell'output verrà salvata nello stream specificato.

Se il formato di output è TIFF, l'output verrà salvato come un singolo TIFF multi-frame nello stream specificato.

## Vedi anche

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Drawing::Image\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Aggiunge una filigrana immagine al documento da flussi con opzioni.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<System::Drawing::Image> &watermarkImage, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Il flusso di input. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Lo stream di output. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Le opzioni di salvataggio. |
| watermarkImage | const System::SharedPtr\<System::Drawing::Image\>\& | Immagine visualizzata come filigrana. |
| opzioni | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Definisce opzioni aggiuntive per la filigrana immagine. |
## Note


Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo la prima pagina dell'output verrà salvata nello stream specificato.

Se il formato di output è TIFF, l'output verrà salvato come un singolo TIFF multi-frame nello stream specificato.

## Vedi anche

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::IO::Stream\>\&) method


Aggiunge una filigrana immagine al documento da flussi con opzioni.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<System::IO::Stream> &watermarkImageStream)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Il flusso di input. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Lo stream di output. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Le opzioni di salvataggio. |
| watermarkImageStream | const System::SharedPtr\<System::IO::Stream\>\& | Stream immagine visualizzato come filigrana. |
## Note


Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo la prima pagina dell'output verrà salvata nello stream specificato.

Se il formato di output è TIFF, l'output verrà salvato come un singolo TIFF multi-frame nello stream specificato.

## Vedi anche

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Aggiunge una filigrana immagine al documento da flussi con opzioni.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<System::IO::Stream> &watermarkImageStream, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Il flusso di input. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Lo stream di output. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Le opzioni di salvataggio. |
| watermarkImageStream | const System::SharedPtr\<System::IO::Stream\>\& | Stream immagine visualizzato come filigrana. |
| opzioni | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Definisce opzioni aggiuntive per la filigrana immagine. |
## Note


Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo la prima pagina dell'output verrà salvata nello stream specificato.

Se il formato di output è TIFF, l'output verrà salvato come un singolo TIFF multi-frame nello stream specificato.

## Vedi anche

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&) method


Aggiunge una filigrana immagine al documento con opzioni e formato di salvataggio specificato.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::String &watermarkImageFileName)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | const System::String\& | Il nome del file di input. |
| outputFileName | const System::String\& | Il nome del file di output. |
| saveFormat | Aspose::Words::SaveFormat | Il formato di salvataggio. |
| watermarkImageFileName | const System::String\& | Immagine visualizzata come filigrana. |
## Note


Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), ogni pagina dell'output verrà salvata come file separato. Il nome del file di output specificato verrà usato per generare i nomi dei file per ogni parte secondo la regola: outputFile_partIndex.extension.

Se il formato di output è TIFF, l'output verrà salvato come un unico file TIFF multi-frame.

## Vedi anche

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Aggiunge una filigrana immagine al documento con opzioni e formato di salvataggio specificato.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::String &watermarkImageFileName, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | const System::String\& | Il nome del file di input. |
| outputFileName | const System::String\& | Il nome del file di output. |
| saveFormat | Aspose::Words::SaveFormat | Il formato di salvataggio. |
| watermarkImageFileName | const System::String\& | Immagine visualizzata come filigrana. |
| opzioni | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Definisce opzioni aggiuntive per la filigrana immagine. |
## Note


Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), ogni pagina dell'output verrà salvata come file separato. Il nome del file di output specificato verrà usato per generare i nomi dei file per ogni parte secondo la regola: outputFile_partIndex.extension.

Se il formato di output è TIFF, l'output verrà salvato come un unico file TIFF multi-frame.

## Vedi anche

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&) method


Aggiunge una filigrana immagine al documento con opzioni e formato di salvataggio specificato.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &watermarkImageFileName)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | const System::String\& | Il nome del file di input. |
| outputFileName | const System::String\& | Il nome del file di output. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Le opzioni di salvataggio. |
| watermarkImageFileName | const System::String\& | Immagine visualizzata come filigrana. |
## Note


Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), ogni pagina dell'output verrà salvata come file separato. Il nome del file di output specificato verrà usato per generare i nomi dei file per ogni parte secondo la regola: outputFile_partIndex.extension.

Se il formato di output è TIFF, l'output verrà salvato come un unico file TIFF multi-frame.

## Vedi anche

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Aggiunge una filigrana immagine al documento con opzioni e formato di salvataggio specificato.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &watermarkImageFileName, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | const System::String\& | Il nome del file di input. |
| outputFileName | const System::String\& | Il nome del file di output. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Le opzioni di salvataggio. |
| watermarkImageFileName | const System::String\& | Immagine visualizzata come filigrana. |
| opzioni | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Definisce opzioni aggiuntive per la filigrana immagine. |
## Note


Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), ogni pagina dell'output verrà salvata come file separato. Il nome del file di output specificato verrà usato per generare i nomi dei file per ogni parte secondo la regola: outputFile_partIndex.extension.

Se il formato di output è TIFF, l'output verrà salvato come un unico file TIFF multi-frame.

## Vedi anche

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::String\&, const System::String\&, const System::String\&) method


Aggiunge una filigrana immagine al documento.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::String &inputFileName, const System::String &outputFileName, const System::String &watermarkImageFileName)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | const System::String\& | Il nome del file di input. |
| outputFileName | const System::String\& | Il nome del file di output. |
| watermarkImageFileName | const System::String\& | Immagine visualizzata come filigrana. |
## Note


Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), ogni pagina dell'output verrà salvata come file separato. Il nome del file di output specificato verrà usato per generare i nomi dei file per ogni parte secondo la regola: outputFile_partIndex.extension.

Se il formato di output è TIFF, l'output verrà salvato come un unico file TIFF multi-frame.

## Vedi anche

* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::String\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Aggiunge una filigrana immagine al documento con opzioni.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::String &inputFileName, const System::String &outputFileName, const System::String &watermarkImageFileName, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | const System::String\& | Il nome del file di input. |
| outputFileName | const System::String\& | Il nome del file di output. |
| watermarkImageFileName | const System::String\& | Immagine visualizzata come filigrana. |
| opzioni | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Definisce opzioni aggiuntive per la filigrana immagine. |
## Note


Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), ogni pagina dell'output verrà salvata come file separato. Il nome del file di output specificato verrà usato per generare i nomi dei file per ogni parte secondo la regola: outputFile_partIndex.extension.

Se il formato di output è TIFF, l'output verrà salvato come un unico file TIFF multi-frame.

## Vedi anche

* Class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
