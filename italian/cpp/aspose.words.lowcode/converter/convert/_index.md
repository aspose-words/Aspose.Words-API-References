---
title: "Aspose::Words::LowCode::Converter::Convert metodo"
linktitle: "Converti"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::LowCode::Converter::Convert metodo. Converte il documento di input fornito in un unico documento di output utilizzando i flussi di input e output specificati in C++."
type: docs
weight: 1000
url: /it/cpp/aspose.words.lowcode/converter/convert/
---
## Converter::Convert(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) method


Converte il documento di input fornito in un unico documento di output utilizzando i flussi di input e output specificati.

```cpp
static void Aspose::Words::LowCode::Converter::Convert(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | I flussi di input. |
| loadOptions | const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\& | Le opzioni di caricamento del documento di input. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Lo stream di output. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Le opzioni di salvataggio. |
## Note


Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo la prima pagina dell'output verrà salvata nello stream specificato.

Se il formato di output è TIFF, l'output verrà salvato come un singolo TIFF multi-frame nello stream specificato.

## Vedi anche

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::Convert(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) method


Converte il documento di input fornito in un unico documento di output utilizzando i flussi di input e output specificati.

```cpp
static void Aspose::Words::LowCode::Converter::Convert(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Il flusso di input. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Lo stream di output. |
| saveFormat | Aspose::Words::SaveFormat | Il formato di salvataggio. |
## Note


Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo la prima pagina dell'output verrà salvata nello stream specificato.

Se il formato di output è TIFF, l'output verrà salvato come un singolo TIFF multi-frame nello stream specificato.

## Vedi anche

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::Convert(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) method


Converte il documento di input fornito in un unico documento di output utilizzando i flussi di input e output specificati.

```cpp
static void Aspose::Words::LowCode::Converter::Convert(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | I flussi di input. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Lo stream di output. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Le opzioni di salvataggio. |
## Note


Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo la prima pagina dell'output verrà salvata nello stream specificato.

Se il formato di output è TIFF, l'output verrà salvato come un singolo TIFF multi-frame nello stream specificato.

## Vedi anche

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::Convert(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) method


Converte il documento di input fornito nel documento di output utilizzando i nomi di file di input e output specificati e le sue opzioni di caricamento/salvataggio.

```cpp
static void Aspose::Words::LowCode::Converter::Convert(const System::String &inputFile, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions, const System::String &outputFile, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFile | const System::String\& | Il nome del file di input. |
| loadOptions | const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\& | Le opzioni di caricamento del documento di input. |
| outputFile | const System::String\& | Il nome del file di output. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Le opzioni di salvataggio. |
## Note


Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), ogni pagina dell'output verrà salvata come file separato. Il nome del file di output specificato verrà usato per generare i nomi dei file per ogni parte secondo la regola: outputFile_partIndex.extension.

Se il formato di output è TIFF, l'output verrà salvato come un unico file TIFF multi-frame.

## Vedi anche

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::Convert(const System::String\&, const System::String\&) method


Converte il documento di input fornito nel documento di output utilizzando i nomi dei file di input e output specificati e le relative estensioni.

```cpp
static void Aspose::Words::LowCode::Converter::Convert(const System::String &inputFile, const System::String &outputFile)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFile | const System::String\& | Il nome del file di input. |
| outputFile | const System::String\& | Il nome del file di output. |
## Note


Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), ogni pagina dell'output verrà salvata come file separato. Il nome del file di output specificato verrà usato per generare i nomi dei file per ogni parte secondo la regola: outputFile_partIndex.extension.

Se il formato di output è TIFF, l'output verrà salvato come un unico file TIFF multi-frame.

## Vedi anche

* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::Convert(const System::String\&, const System::String\&, Aspose::Words::SaveFormat) method


Converte il documento di input fornito nel documento di output utilizzando i nomi di file di input e output specificati e il formato finale del documento.

```cpp
static void Aspose::Words::LowCode::Converter::Convert(const System::String &inputFile, const System::String &outputFile, Aspose::Words::SaveFormat saveFormat)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFile | const System::String\& | Il nome del file di input. |
| outputFile | const System::String\& | Il nome del file di output. |
| saveFormat | Aspose::Words::SaveFormat | Il formato di salvataggio. |
## Note


Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), ogni pagina dell'output verrà salvata come file separato. Il nome del file di output specificato verrà usato per generare i nomi dei file per ogni parte secondo la regola: outputFile_partIndex.extension.

Se il formato di output è TIFF, l'output verrà salvato come un unico file TIFF multi-frame.

## Vedi anche

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::Convert(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) method


Converte il documento di input fornito nel documento di output utilizzando i nomi di file di input e output specificati e le opzioni di salvataggio.

```cpp
static void Aspose::Words::LowCode::Converter::Convert(const System::String &inputFile, const System::String &outputFile, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFile | const System::String\& | Il nome del file di input. |
| outputFile | const System::String\& | Il nome del file di output. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Le opzioni di salvataggio. |
## Note


Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), ogni pagina dell'output verrà salvata come file separato. Il nome del file di output specificato verrà usato per generare i nomi dei file per ogni parte secondo la regola: outputFile_partIndex.extension.

Se il formato di output è TIFF, l'output verrà salvato come un unico file TIFF multi-frame.

## Vedi anche

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
