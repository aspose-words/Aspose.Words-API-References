---
title: "Aspose::Words::LowCode::Converter::ConvertToImages metodo"
linktitle: "ConvertToImages"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::LowCode::Converter::ConvertToImages metodo. Converte le pagine del documento specificato in immagini nel formato specificato e restituisce un array di stream contenenti le immagini in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.lowcode/converter/converttoimages/
---
## Converter::ConvertToImages(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::SaveFormat) method


Converte le pagine del documento specificato in immagini nel formato specificato e restituisce un array di flussi contenenti le immagini.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Converter::ConvertToImages(const System::SharedPtr<Aspose::Words::Document> &doc, Aspose::Words::SaveFormat saveFormat)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::Document\>\& | Il documento di input. |
| saveFormat | Aspose::Words::SaveFormat | Formato di salvataggio. Sono consentiti solo formati di salvataggio immagine. |

### ReturnValue

Restituisce un array di stream di immagini. Gli stream devono essere rilasciati dall'utente finale.

## Vedi anche

* Class [Document](../../../aspose.words/document/)
* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::SharedPtr\<Aspose::Words::Document\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) method


Converte le pagine del documento specificato in immagini utilizzando le opzioni di salvataggio specificate e restituisce un array di flussi contenenti le immagini.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Converter::ConvertToImages(const System::SharedPtr<Aspose::Words::Document> &doc, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::Document\>\& | Il documento di input. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Opzioni di salvataggio dell'immagine. |

### ReturnValue

Restituisce un array di stream di immagini. Gli stream devono essere rilasciati dall'utente finale.

## Vedi anche

* Class [Document](../../../aspose.words/document/)
* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) method


Converte le pagine del flusso di input specificato in immagini nel formato specificato e restituisce un array di flussi contenenti le immagini.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Converter::ConvertToImages(const System::SharedPtr<System::IO::Stream> &inputStream, Aspose::Words::SaveFormat saveFormat)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Il flusso di input. |
| saveFormat | Aspose::Words::SaveFormat | Formato di salvataggio. Sono consentiti solo formati di salvataggio immagine. |

### ReturnValue

Restituisce un array di stream di immagini. Gli stream devono essere rilasciati dall'utente finale.

## Vedi anche

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) method


Converte le pagine del flusso di input specificato in immagini utilizzando le opzioni di caricamento e salvataggio fornite, e restituisce un array di flussi contenenti le immagini.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Converter::ConvertToImages(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Il flusso di input. |
| loadOptions | const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\& | Le opzioni di caricamento del documento di input. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Opzioni di salvataggio dell'immagine. |

### ReturnValue

Restituisce un array di stream di immagini. Gli stream devono essere rilasciati dall'utente finale.

## Vedi anche

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) method


Converte le pagine del flusso di input specificato in immagini utilizzando le opzioni di salvataggio specificate e restituisce un array di flussi contenenti le immagini.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Converter::ConvertToImages(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Il flusso di input. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Opzioni di salvataggio dell'immagine. |

### ReturnValue

Restituisce un array di stream di immagini. Gli stream devono essere rilasciati dall'utente finale.

## Vedi anche

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::String\&, Aspose::Words::SaveFormat) method


Converte le pagine del file di input specificato in immagini nel formato specificato e restituisce un array di flussi contenenti le immagini.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Converter::ConvertToImages(const System::String &inputFile, Aspose::Words::SaveFormat saveFormat)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFile | const System::String\& | Il nome del file di input. |
| saveFormat | Aspose::Words::SaveFormat | Formato di salvataggio. Sono consentiti solo formati di salvataggio immagine. |

### ReturnValue

Restituisce un array di stream di immagini. Gli stream devono essere rilasciati dall'utente finale.

## Vedi anche

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) method


Converte le pagine del file di input specificato in file immagine utilizzando le opzioni di caricamento e salvataggio fornite.

```cpp
static void Aspose::Words::LowCode::Converter::ConvertToImages(const System::String &inputFile, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions, const System::String &outputFile, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFile | const System::String\& | Il nome del file di input. |
| loadOptions | const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\& | Le opzioni di caricamento del documento di input. |
| outputFile | const System::String\& | Il nome file di output utilizzato per generare il nome file per le immagini delle pagine secondo la regola "outputFile_pageIndex.extension" |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Opzioni di salvataggio dell'immagine. |

## Vedi anche

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) method


Converte le pagine del file di input specificato in immagini utilizzando le opzioni di salvataggio specificate e restituisce un array di flussi contenenti le immagini.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Converter::ConvertToImages(const System::String &inputFile, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFile | const System::String\& | Il nome del file di input. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Opzioni di salvataggio dell'immagine. |

### ReturnValue

Restituisce un array di stream di immagini. Gli stream devono essere rilasciati dall'utente finale.

## Vedi anche

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::String\&, const System::String\&) method


Converte le pagine del file di input specificato in file immagine.

```cpp
static void Aspose::Words::LowCode::Converter::ConvertToImages(const System::String &inputFile, const System::String &outputFile)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFile | const System::String\& | Il nome del file di input. |
| outputFile | const System::String\& | Il nome file di output utilizzato per generare il nome file per le immagini delle pagine secondo la regola "outputFile_pageIndex.extension" |

## Vedi anche

* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::String\&, const System::String\&, Aspose::Words::SaveFormat) method


Converte le pagine del file di input specificato in file immagine nel formato specificato.

```cpp
static void Aspose::Words::LowCode::Converter::ConvertToImages(const System::String &inputFile, const System::String &outputFile, Aspose::Words::SaveFormat saveFormat)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFile | const System::String\& | Il nome del file di input. |
| outputFile | const System::String\& | Il nome file di output utilizzato per generare il nome file per le immagini delle pagine secondo la regola "outputFile_pageIndex.extension" |
| saveFormat | Aspose::Words::SaveFormat | Formato di salvataggio. Sono consentiti solo formati di salvataggio immagine. |

## Vedi anche

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) method


Converte le pagine del file di input specificato in file immagine utilizzando le opzioni di salvataggio specificate.

```cpp
static void Aspose::Words::LowCode::Converter::ConvertToImages(const System::String &inputFile, const System::String &outputFile, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFile | const System::String\& | Il nome del file di input. |
| outputFile | const System::String\& | Il nome file di output utilizzato per generare il nome file per le immagini delle pagine secondo la regola "outputFile_pageIndex.extension" |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Opzioni di salvataggio dell'immagine. |

## Vedi anche

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
