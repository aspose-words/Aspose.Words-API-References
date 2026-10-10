---
title: "Aspose::Words::LowCode::Splitter::Split metodo"
linktitle: "Dividi"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::LowCode::Splitter::Split metodo. Divide un documento da un flusso di input in più parti in base alle opzioni di divisione specificate e restituisce le parti risultanti come un array di flussi nel formato di salvataggio specificato in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.lowcode/splitter/split/
---
## Splitter::Split(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) method


Divide un documento da un flusso di input in più parti in base alle opzioni di divisione specificate e restituisce le parti risultanti come un array di flussi nel formato di salvataggio specificato.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Splitter::Split(const System::SharedPtr<System::IO::Stream> &inputStream, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<Aspose::Words::LowCode::SplitOptions> &options)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Il flusso di input. |
| saveFormat | Aspose::Words::SaveFormat | Il formato di salvataggio. |
| options | const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\& | [Document](../../../aspose.words/document/) opzioni di divisione. |

## Vedi anche

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [SplitOptions](../../splitoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::Split(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) method


Divide un documento da un flusso di input in più parti in base alle opzioni di divisione specificate e restituisce le parti risultanti come un array di flussi nel formato di salvataggio specificato.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Splitter::Split(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<Aspose::Words::LowCode::SplitOptions> &options)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Il flusso di input. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Le opzioni di salvataggio. |
| options | const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\& | [Document](../../../aspose.words/document/) opzioni di divisione. |

## Vedi anche

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [SplitOptions](../../splitoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::Split(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) method


Divide un documento in più parti in base alle opzioni di divisione specificate e salva le parti risultanti in file nel formato di salvataggio specificato.

```cpp
static void Aspose::Words::LowCode::Splitter::Split(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<Aspose::Words::LowCode::SplitOptions> &options)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | const System::String\& | Il nome del file di input. |
| outputFileName | const System::String\& | Il nome file di output utilizzato per generare il nome file per le parti del documento usando la regola "outputFile_partIndex.extension" |
| saveFormat | Aspose::Words::SaveFormat | Il formato di salvataggio. |
| options | const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\& | [Document](../../../aspose.words/document/) opzioni di divisione. |

## Vedi anche

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [SplitOptions](../../splitoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::Split(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) method


Divide un documento in più parti in base alle opzioni di divisione specificate e salva le parti risultanti in file. Il formato del file di output è determinato dall'estensione del nome del file di output.

```cpp
static void Aspose::Words::LowCode::Splitter::Split(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::LowCode::SplitOptions> &options)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | const System::String\& | Il nome del file di input. |
| outputFileName | const System::String\& | Il nome file di output utilizzato per generare il nome file per le parti del documento usando la regola "outputFile_partIndex.extension" |
| options | const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\& | [Document](../../../aspose.words/document/) opzioni di divisione. |

## Vedi anche

* Class [SplitOptions](../../splitoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::Split(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) method


Divide un documento in più parti in base alle opzioni di divisione specificate e salva le parti risultanti in file nel formato di salvataggio specificato.

```cpp
static void Aspose::Words::LowCode::Splitter::Split(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<Aspose::Words::LowCode::SplitOptions> &options)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | const System::String\& | Il nome del file di input. |
| outputFileName | const System::String\& | Il nome file di output utilizzato per generare il nome file per le parti del documento usando la regola "outputFile_partIndex.extension" |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Le opzioni di salvataggio. |
| options | const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\& | [Document](../../../aspose.words/document/) opzioni di divisione. |

## Vedi anche

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [SplitOptions](../../splitoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
