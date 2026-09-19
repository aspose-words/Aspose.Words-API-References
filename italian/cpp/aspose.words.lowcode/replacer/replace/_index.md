---
title: "Aspose::Words::LowCode::Replacer::Replace metodo"
linktitle: "Sostituisci"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::LowCode::Replacer::Replace metodo. Sostituisce tutte le occorrenze di un modello di stringa di caratteri specificato con una stringa di sostituzione nel flusso di input usando un'espressione regolare, con il formato di salvataggio specificato e opzioni aggiuntive in C++."
type: docs
weight: 1000
url: /it/cpp/aspose.words.lowcode/replacer/replace/
---
## Replacer::Replace(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) method


Sostituisce tutte le occorrenze di un modello di stringa di caratteri specificato con una stringa di sostituzione nello stream di input utilizzando un'espressione regolare, con il formato di salvataggio specificato e opzioni aggiuntive.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Il flusso di input. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Lo stream di output. |
| saveFormat | Aspose::Words::SaveFormat | Il formato di salvataggio. |
| modello | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Un modello di espressione regolare usato per trovare corrispondenze. |
| sostituzione | const System::String\& | Una stringa per sostituire tutte le occorrenze del modello. |

### ReturnValue

Il numero di sostituzioni effettuate.
## Note


Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo la prima pagina dell'output verrà salvata nello stream specificato.

Se il formato di output è TIFF, l'output verrà salvato come un singolo TIFF multi-frame nello stream specificato.

## Vedi anche

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Sostituisce tutte le occorrenze di un modello di stringa di caratteri specificato con una stringa di sostituzione nello stream di input utilizzando un'espressione regolare, con il formato di salvataggio specificato e opzioni aggiuntive.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Il flusso di input. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Lo stream di output. |
| saveFormat | Aspose::Words::SaveFormat | Il formato di salvataggio. |
| modello | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Un modello di espressione regolare usato per trovare corrispondenze. |
| sostituzione | const System::String\& | Una stringa per sostituire tutte le occorrenze del modello. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | Oggetto [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) per specificare opzioni aggiuntive. |

### ReturnValue

Il numero di sostituzioni effettuate.
## Note


Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo la prima pagina dell'output verrà salvata nello stream specificato.

Se il formato di output è TIFF, l'output verrà salvato come un singolo TIFF multi-frame nello stream specificato.

## Vedi anche

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, const System::String\&) method


Sostituisce tutte le occorrenze di un modello di stringa di caratteri specificato con una stringa di sostituzione nello stream di input, con il formato di salvataggio specificato e opzioni aggiuntive.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::String &pattern, const System::String &replacement)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Il flusso di input. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Lo stream di output. |
| saveFormat | Aspose::Words::SaveFormat | Il formato di salvataggio. |
| modello | const System::String\& | Una stringa da sostituire. |
| sostituzione | const System::String\& | Una stringa per sostituire tutte le occorrenze del modello. |

### ReturnValue

Il numero di sostituzioni effettuate.
## Note


Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo la prima pagina dell'output verrà salvata nello stream specificato.

Se il formato di output è TIFF, l'output verrà salvato come un singolo TIFF multi-frame nello stream specificato.

## Vedi anche

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Sostituisce tutte le occorrenze di un modello di stringa di caratteri specificato con una stringa di sostituzione nello stream di input, con il formato di salvataggio specificato e opzioni aggiuntive.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::String &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Il flusso di input. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Lo stream di output. |
| saveFormat | Aspose::Words::SaveFormat | Il formato di salvataggio. |
| modello | const System::String\& | Una stringa da sostituire. |
| sostituzione | const System::String\& | Una stringa per sostituire tutte le occorrenze del modello. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | Oggetto [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) per specificare opzioni aggiuntive. |

### ReturnValue

Il numero di sostituzioni effettuate.
## Note


Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo la prima pagina dell'output verrà salvata nello stream specificato.

Se il formato di output è TIFF, l'output verrà salvato come un singolo TIFF multi-frame nello stream specificato.

## Vedi anche

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) method


Sostituisce tutte le occorrenze di un modello di stringa di caratteri specificato con una stringa di sostituzione nello stream di input utilizzando un'espressione regolare, con il formato di salvataggio specificato e opzioni aggiuntive.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Il flusso di input. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Lo stream di output. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Le opzioni di salvataggio. |
| modello | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Un modello di espressione regolare usato per trovare corrispondenze. |
| sostituzione | const System::String\& | Una stringa per sostituire tutte le occorrenze del modello. |

### ReturnValue

Il numero di sostituzioni effettuate.
## Note


Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo la prima pagina dell'output verrà salvata nello stream specificato.

Se il formato di output è TIFF, l'output verrà salvato come un singolo TIFF multi-frame nello stream specificato.

## Vedi anche

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Sostituisce tutte le occorrenze di un modello di stringa di caratteri specificato con una stringa di sostituzione nello stream di input utilizzando un'espressione regolare, con il formato di salvataggio specificato e opzioni aggiuntive.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Il flusso di input. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Lo stream di output. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Le opzioni di salvataggio. |
| modello | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Un modello di espressione regolare usato per trovare corrispondenze. |
| sostituzione | const System::String\& | Una stringa per sostituire tutte le occorrenze del modello. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | Oggetto [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) per specificare opzioni aggiuntive. |

### ReturnValue

Il numero di sostituzioni effettuate.
## Note


Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo la prima pagina dell'output verrà salvata nello stream specificato.

Se il formato di output è TIFF, l'output verrà salvato come un singolo TIFF multi-frame nello stream specificato.

## Vedi anche

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::String\&) method


Sostituisce tutte le occorrenze di un modello di stringa di caratteri specificato con una stringa di sostituzione nello stream di input, con il formato di salvataggio specificato e opzioni aggiuntive.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &pattern, const System::String &replacement)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Il flusso di input. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Lo stream di output. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Le opzioni di salvataggio. |
| modello | const System::String\& | Una stringa da sostituire. |
| sostituzione | const System::String\& | Una stringa per sostituire tutte le occorrenze del modello. |

### ReturnValue

Il numero di sostituzioni effettuate.
## Note


Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo la prima pagina dell'output verrà salvata nello stream specificato.

Se il formato di output è TIFF, l'output verrà salvato come un singolo TIFF multi-frame nello stream specificato.

## Vedi anche

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Sostituisce tutte le occorrenze di un modello di stringa di caratteri specificato con una stringa di sostituzione nello stream di input, con il formato di salvataggio specificato e opzioni aggiuntive.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Il flusso di input. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Lo stream di output. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Le opzioni di salvataggio. |
| modello | const System::String\& | Una stringa da sostituire. |
| sostituzione | const System::String\& | Una stringa per sostituire tutte le occorrenze del modello. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | Oggetto [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) per specificare opzioni aggiuntive. |

### ReturnValue

Il numero di sostituzioni effettuate.
## Note


Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo la prima pagina dell'output verrà salvata nello stream specificato.

Se il formato di output è TIFF, l'output verrà salvato come un singolo TIFF multi-frame nello stream specificato.

## Vedi anche

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) method


Sostituisce tutte le occorrenze di un modello di stringa di caratteri specificato con una stringa di sostituzione nel file di input utilizzando un'espressione regolare, con il formato di salvataggio specificato e opzioni aggiuntive.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | const System::String\& | Il nome del file di input. |
| outputFileName | const System::String\& | Il nome del file di output. |
| saveFormat | Aspose::Words::SaveFormat | Il formato di salvataggio. |
| modello | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Un modello di espressione regolare usato per trovare corrispondenze. |
| sostituzione | const System::String\& | Una stringa per sostituire tutte le occorrenze del modello. |

### ReturnValue

Il numero di sostituzioni effettuate.
## Note


Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), ogni pagina dell'output verrà salvata come file separato. Il nome del file di output specificato verrà usato per generare i nomi dei file per ogni parte secondo la regola: outputFile_partIndex.extension.

Se il formato di output è TIFF, l'output verrà salvato come un unico file TIFF multi-frame.

## Vedi anche

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Sostituisce tutte le occorrenze di un modello di stringa di caratteri specificato con una stringa di sostituzione nel file di input utilizzando un'espressione regolare, con il formato di salvataggio specificato e opzioni aggiuntive.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | const System::String\& | Il nome del file di input. |
| outputFileName | const System::String\& | Il nome del file di output. |
| saveFormat | Aspose::Words::SaveFormat | Il formato di salvataggio. |
| modello | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Un modello di espressione regolare usato per trovare corrispondenze. |
| sostituzione | const System::String\& | Una stringa per sostituire tutte le occorrenze del modello. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | Oggetto [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) per specificare opzioni aggiuntive. |

### ReturnValue

Il numero di sostituzioni effettuate.
## Note


Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), ogni pagina dell'output verrà salvata come file separato. Il nome del file di output specificato verrà usato per generare i nomi dei file per ogni parte secondo la regola: outputFile_partIndex.extension.

Se il formato di output è TIFF, l'output verrà salvato come un unico file TIFF multi-frame.

## Vedi anche

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, const System::String\&) method


Sostituisce tutte le occorrenze di un modello di stringa di caratteri specificato con una stringa di sostituzione nel file di input, con il formato di salvataggio specificato e opzioni aggiuntive.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::String &pattern, const System::String &replacement)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | const System::String\& | Il nome del file di input. |
| outputFileName | const System::String\& | Il nome del file di output. |
| saveFormat | Aspose::Words::SaveFormat | Il formato di salvataggio. |
| modello | const System::String\& | Una stringa da sostituire. |
| sostituzione | const System::String\& | Una stringa per sostituire tutte le occorrenze del modello. |

### ReturnValue

Il numero di sostituzioni effettuate.
## Note


Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), ogni pagina dell'output verrà salvata come file separato. Il nome del file di output specificato verrà usato per generare i nomi dei file per ogni parte secondo la regola: outputFile_partIndex.extension.

Se il formato di output è TIFF, l'output verrà salvato come un unico file TIFF multi-frame.

## Vedi anche

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Sostituisce tutte le occorrenze di un modello di stringa di caratteri specificato con una stringa di sostituzione nel file di input, con il formato di salvataggio specificato e opzioni aggiuntive.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::String &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | const System::String\& | Il nome del file di input. |
| outputFileName | const System::String\& | Il nome del file di output. |
| saveFormat | Aspose::Words::SaveFormat | Il formato di salvataggio. |
| modello | const System::String\& | Una stringa da sostituire. |
| sostituzione | const System::String\& | Una stringa per sostituire tutte le occorrenze del modello. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | Oggetto [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) per specificare opzioni aggiuntive. |

### ReturnValue

Il numero di sostituzioni effettuate.
## Note


Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), ogni pagina dell'output verrà salvata come file separato. Il nome del file di output specificato verrà usato per generare i nomi dei file per ogni parte secondo la regola: outputFile_partIndex.extension.

Se il formato di output è TIFF, l'output verrà salvato come un unico file TIFF multi-frame.

## Vedi anche

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) method


Sostituisce tutte le occorrenze di un modello di stringa di caratteri specificato con una stringa di sostituzione nel file di input utilizzando un'espressione regolare, con il formato di salvataggio specificato e opzioni aggiuntive.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | const System::String\& | Il nome del file di input. |
| outputFileName | const System::String\& | Il nome del file di output. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Le opzioni di salvataggio. |
| modello | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Un modello di espressione regolare usato per trovare corrispondenze. |
| sostituzione | const System::String\& | Una stringa per sostituire tutte le occorrenze del modello. |

### ReturnValue

Il numero di sostituzioni effettuate.
## Note


Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), ogni pagina dell'output verrà salvata come file separato. Il nome del file di output specificato verrà usato per generare i nomi dei file per ogni parte secondo la regola: outputFile_partIndex.extension.

Se il formato di output è TIFF, l'output verrà salvato come un unico file TIFF multi-frame.

## Vedi anche

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Sostituisce tutte le occorrenze di un modello di stringa di caratteri specificato con una stringa di sostituzione nel file di input utilizzando un'espressione regolare, con il formato di salvataggio specificato e opzioni aggiuntive.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | const System::String\& | Il nome del file di input. |
| outputFileName | const System::String\& | Il nome del file di output. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Le opzioni di salvataggio. |
| modello | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Un modello di espressione regolare usato per trovare corrispondenze. |
| sostituzione | const System::String\& | Una stringa per sostituire tutte le occorrenze del modello. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | Oggetto [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) per specificare opzioni aggiuntive. |

### ReturnValue

Il numero di sostituzioni effettuate.
## Note


Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), ogni pagina dell'output verrà salvata come file separato. Il nome del file di output specificato verrà usato per generare i nomi dei file per ogni parte secondo la regola: outputFile_partIndex.extension.

Se il formato di output è TIFF, l'output verrà salvato come un unico file TIFF multi-frame.

## Vedi anche

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::String\&) method


Sostituisce tutte le occorrenze di un modello di stringa di caratteri specificato con una stringa di sostituzione nel file di input, con il formato di salvataggio specificato e opzioni aggiuntive.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &pattern, const System::String &replacement)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | const System::String\& | Il nome del file di input. |
| outputFileName | const System::String\& | Il nome del file di output. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Le opzioni di salvataggio. |
| modello | const System::String\& | Una stringa da sostituire. |
| sostituzione | const System::String\& | Una stringa per sostituire tutte le occorrenze del modello. |

### ReturnValue

Il numero di sostituzioni effettuate.
## Note


Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), ogni pagina dell'output verrà salvata come file separato. Il nome del file di output specificato verrà usato per generare i nomi dei file per ogni parte secondo la regola: outputFile_partIndex.extension.

Se il formato di output è TIFF, l'output verrà salvato come un unico file TIFF multi-frame.

## Vedi anche

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Sostituisce tutte le occorrenze di un modello di stringa di caratteri specificato con una stringa di sostituzione nel file di input, con il formato di salvataggio specificato e opzioni aggiuntive.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | const System::String\& | Il nome del file di input. |
| outputFileName | const System::String\& | Il nome del file di output. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Le opzioni di salvataggio. |
| modello | const System::String\& | Una stringa da sostituire. |
| sostituzione | const System::String\& | Una stringa per sostituire tutte le occorrenze del modello. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | Oggetto [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) per specificare opzioni aggiuntive. |

### ReturnValue

Il numero di sostituzioni effettuate.
## Note


Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), ogni pagina dell'output verrà salvata come file separato. Il nome del file di output specificato verrà usato per generare i nomi dei file per ogni parte secondo la regola: outputFile_partIndex.extension.

Se il formato di output è TIFF, l'output verrà salvato come un unico file TIFF multi-frame.

## Vedi anche

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) method


Sostituisce tutte le occorrenze di un modello di stringa di caratteri specificato con una stringa di sostituzione nel file di input usando un'espressione regolare.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | const System::String\& | Il nome del file di input. |
| outputFileName | const System::String\& | Il nome del file di output. |
| modello | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Un modello di espressione regolare usato per trovare corrispondenze. |
| sostituzione | const System::String\& | Una stringa per sostituire tutte le occorrenze del modello. |

### ReturnValue

Il numero di sostituzioni effettuate.
## Note


Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), ogni pagina dell'output verrà salvata come file separato. Il nome del file di output specificato verrà usato per generare i nomi dei file per ogni parte secondo la regola: outputFile_partIndex.extension.

Se il formato di output è TIFF, l'output verrà salvato come un unico file TIFF multi-frame.

## Vedi anche

* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, const System::String\&, const System::String\&) method


Sostituisce tutte le occorrenze di un modello di stringa di caratteri specificato con una stringa di sostituzione nel file di input.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, const System::String &pattern, const System::String &replacement)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | const System::String\& | Il nome del file di input. |
| outputFileName | const System::String\& | Il nome del file di output. |
| modello | const System::String\& | Una stringa da sostituire. |
| sostituzione | const System::String\& | Una stringa per sostituire tutte le occorrenze del modello. |

### ReturnValue

Il numero di sostituzioni effettuate.
## Note


Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), ogni pagina dell'output verrà salvata come file separato. Il nome del file di output specificato verrà usato per generare i nomi dei file per ogni parte secondo la regola: outputFile_partIndex.extension.

Se il formato di output è TIFF, l'output verrà salvato come un unico file TIFF multi-frame.

## Vedi anche

* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
