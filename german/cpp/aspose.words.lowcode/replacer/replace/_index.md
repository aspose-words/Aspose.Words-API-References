---
title: "Aspose::Words::LowCode::Replacer::Replace Methode"
linktitle: "Ersetzen"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::LowCode::Replacer::Replace Methode. Ersetzt alle Vorkommen eines angegebenen Zeichenkettenmusters durch einen Ersetzungsstring im Eingabestream unter Verwendung eines regulären Ausdrucks, mit dem angegebenen Speicherformat und zusätzlichen Optionen in C++."
type: docs
weight: 1000
url: /de/cpp/aspose.words.lowcode/replacer/replace/
---
## Replacer::Replace(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) method


Ersetzt alle Vorkommen eines angegebenen Zeichenkettenmusters durch einen Ersetzungsstring im Eingabestream mithilfe eines regulären Ausdrucks, mit dem angegebenen Speicherformat und zusätzlichen Optionen.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Der Eingabestream. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Der Ausgabestream. |
| saveFormat | Aspose::Words::SaveFormat | Das Speicherformat. |
| Muster | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Ein reguläres Ausdrucksmuster, das zum Finden von Übereinstimmungen verwendet wird. |
| Ersetzung | const System::String\& | Ein String, um alle Vorkommen des Musters zu ersetzen. |

### ReturnValue

Die Anzahl der vorgenommenen Ersetzungen.
## Hinweise


Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird nur die erste Seite der Ausgabe in den angegebenen Stream gespeichert.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als ein einzelnes Multi‑Frame‑TIFF in den angegebenen Stream gespeichert.

## Siehe auch

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Ersetzt alle Vorkommen eines angegebenen Zeichenkettenmusters durch einen Ersetzungsstring im Eingabestream mithilfe eines regulären Ausdrucks, mit dem angegebenen Speicherformat und zusätzlichen Optionen.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Der Eingabestream. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Der Ausgabestream. |
| saveFormat | Aspose::Words::SaveFormat | Das Speicherformat. |
| Muster | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Ein reguläres Ausdrucksmuster, das zum Finden von Übereinstimmungen verwendet wird. |
| Ersetzung | const System::String\& | Ein String, um alle Vorkommen des Musters zu ersetzen. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)-Objekt, um zusätzliche Optionen anzugeben. |

### ReturnValue

Die Anzahl der vorgenommenen Ersetzungen.
## Hinweise


Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird nur die erste Seite der Ausgabe in den angegebenen Stream gespeichert.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als ein einzelnes Multi‑Frame‑TIFF in den angegebenen Stream gespeichert.

## Siehe auch

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, const System::String\&) method


Ersetzt alle Vorkommen eines angegebenen Zeichenkettenmusters durch einen Ersetzungsstring im Eingabestream, mit dem angegebenen Speicherformat und zusätzlichen Optionen.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::String &pattern, const System::String &replacement)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Der Eingabestream. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Der Ausgabestream. |
| saveFormat | Aspose::Words::SaveFormat | Das Speicherformat. |
| Muster | const System::String\& | Ein zu ersetzender String. |
| Ersetzung | const System::String\& | Ein String, um alle Vorkommen des Musters zu ersetzen. |

### ReturnValue

Die Anzahl der vorgenommenen Ersetzungen.
## Hinweise


Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird nur die erste Seite der Ausgabe in den angegebenen Stream gespeichert.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als ein einzelnes Multi‑Frame‑TIFF in den angegebenen Stream gespeichert.

## Siehe auch

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Ersetzt alle Vorkommen eines angegebenen Zeichenkettenmusters durch einen Ersetzungsstring im Eingabestream, mit dem angegebenen Speicherformat und zusätzlichen Optionen.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::String &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Der Eingabestream. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Der Ausgabestream. |
| saveFormat | Aspose::Words::SaveFormat | Das Speicherformat. |
| Muster | const System::String\& | Ein zu ersetzender String. |
| Ersetzung | const System::String\& | Ein String, um alle Vorkommen des Musters zu ersetzen. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)-Objekt, um zusätzliche Optionen anzugeben. |

### ReturnValue

Die Anzahl der vorgenommenen Ersetzungen.
## Hinweise


Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird nur die erste Seite der Ausgabe in den angegebenen Stream gespeichert.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als ein einzelnes Multi‑Frame‑TIFF in den angegebenen Stream gespeichert.

## Siehe auch

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) method


Ersetzt alle Vorkommen eines angegebenen Zeichenkettenmusters durch einen Ersetzungsstring im Eingabestream mithilfe eines regulären Ausdrucks, mit dem angegebenen Speicherformat und zusätzlichen Optionen.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Der Eingabestream. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Der Ausgabestream. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Die Speicheroptionen. |
| Muster | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Ein reguläres Ausdrucksmuster, das zum Finden von Übereinstimmungen verwendet wird. |
| Ersetzung | const System::String\& | Ein String, um alle Vorkommen des Musters zu ersetzen. |

### ReturnValue

Die Anzahl der vorgenommenen Ersetzungen.
## Hinweise


Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird nur die erste Seite der Ausgabe in den angegebenen Stream gespeichert.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als ein einzelnes Multi‑Frame‑TIFF in den angegebenen Stream gespeichert.

## Siehe auch

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Ersetzt alle Vorkommen eines angegebenen Zeichenkettenmusters durch einen Ersetzungsstring im Eingabestream mithilfe eines regulären Ausdrucks, mit dem angegebenen Speicherformat und zusätzlichen Optionen.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Der Eingabestream. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Der Ausgabestream. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Die Speicheroptionen. |
| Muster | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Ein reguläres Ausdrucksmuster, das zum Finden von Übereinstimmungen verwendet wird. |
| Ersetzung | const System::String\& | Ein String, um alle Vorkommen des Musters zu ersetzen. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)-Objekt, um zusätzliche Optionen anzugeben. |

### ReturnValue

Die Anzahl der vorgenommenen Ersetzungen.
## Hinweise


Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird nur die erste Seite der Ausgabe in den angegebenen Stream gespeichert.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als ein einzelnes Multi‑Frame‑TIFF in den angegebenen Stream gespeichert.

## Siehe auch

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::String\&) method


Ersetzt alle Vorkommen eines angegebenen Zeichenkettenmusters durch einen Ersetzungsstring im Eingabestream, mit dem angegebenen Speicherformat und zusätzlichen Optionen.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &pattern, const System::String &replacement)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Der Eingabestream. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Der Ausgabestream. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Die Speicheroptionen. |
| Muster | const System::String\& | Ein zu ersetzender String. |
| Ersetzung | const System::String\& | Ein String, um alle Vorkommen des Musters zu ersetzen. |

### ReturnValue

Die Anzahl der vorgenommenen Ersetzungen.
## Hinweise


Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird nur die erste Seite der Ausgabe in den angegebenen Stream gespeichert.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als ein einzelnes Multi‑Frame‑TIFF in den angegebenen Stream gespeichert.

## Siehe auch

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Ersetzt alle Vorkommen eines angegebenen Zeichenkettenmusters durch einen Ersetzungsstring im Eingabestream, mit dem angegebenen Speicherformat und zusätzlichen Optionen.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Der Eingabestream. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Der Ausgabestream. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Die Speicheroptionen. |
| Muster | const System::String\& | Ein zu ersetzender String. |
| Ersetzung | const System::String\& | Ein String, um alle Vorkommen des Musters zu ersetzen. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)-Objekt, um zusätzliche Optionen anzugeben. |

### ReturnValue

Die Anzahl der vorgenommenen Ersetzungen.
## Hinweise


Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird nur die erste Seite der Ausgabe in den angegebenen Stream gespeichert.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als ein einzelnes Multi‑Frame‑TIFF in den angegebenen Stream gespeichert.

## Siehe auch

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) method


Ersetzt alle Vorkommen eines angegebenen Zeichenkettenmusters durch einen Ersetzungsstring in der Eingabedatei mithilfe eines regulären Ausdrucks, mit dem angegebenen Speicherformat und zusätzlichen Optionen.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | const System::String\& | Der Eingabedateiname. |
| outputFileName | const System::String\& | Der Name der Ausgabedatei. |
| saveFormat | Aspose::Words::SaveFormat | Das Speicherformat. |
| Muster | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Ein reguläres Ausdrucksmuster, das zum Finden von Übereinstimmungen verwendet wird. |
| Ersetzung | const System::String\& | Ein String, um alle Vorkommen des Musters zu ersetzen. |

### ReturnValue

Die Anzahl der vorgenommenen Ersetzungen.
## Hinweise


Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jeden Teil nach der Regel: outputFile_partIndex.extension zu erzeugen.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als eine einzelne Multi‑Frame‑TIFF‑Datei gespeichert.

## Siehe auch

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Ersetzt alle Vorkommen eines angegebenen Zeichenkettenmusters durch einen Ersetzungsstring in der Eingabedatei mithilfe eines regulären Ausdrucks, mit dem angegebenen Speicherformat und zusätzlichen Optionen.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | const System::String\& | Der Eingabedateiname. |
| outputFileName | const System::String\& | Der Name der Ausgabedatei. |
| saveFormat | Aspose::Words::SaveFormat | Das Speicherformat. |
| Muster | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Ein reguläres Ausdrucksmuster, das zum Finden von Übereinstimmungen verwendet wird. |
| Ersetzung | const System::String\& | Ein String, um alle Vorkommen des Musters zu ersetzen. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)-Objekt, um zusätzliche Optionen anzugeben. |

### ReturnValue

Die Anzahl der vorgenommenen Ersetzungen.
## Hinweise


Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jeden Teil nach der Regel: outputFile_partIndex.extension zu erzeugen.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als eine einzelne Multi‑Frame‑TIFF‑Datei gespeichert.

## Siehe auch

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, const System::String\&) method


Ersetzt alle Vorkommen eines angegebenen Zeichenkettenmusters durch einen Ersetzungsstring in der Eingabedatei, mit dem angegebenen Speicherformat und zusätzlichen Optionen.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::String &pattern, const System::String &replacement)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | const System::String\& | Der Eingabedateiname. |
| outputFileName | const System::String\& | Der Name der Ausgabedatei. |
| saveFormat | Aspose::Words::SaveFormat | Das Speicherformat. |
| Muster | const System::String\& | Ein zu ersetzender String. |
| Ersetzung | const System::String\& | Ein String, um alle Vorkommen des Musters zu ersetzen. |

### ReturnValue

Die Anzahl der vorgenommenen Ersetzungen.
## Hinweise


Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jeden Teil nach der Regel: outputFile_partIndex.extension zu erzeugen.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als eine einzelne Multi‑Frame‑TIFF‑Datei gespeichert.

## Siehe auch

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Ersetzt alle Vorkommen eines angegebenen Zeichenkettenmusters durch einen Ersetzungsstring in der Eingabedatei, mit dem angegebenen Speicherformat und zusätzlichen Optionen.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::String &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | const System::String\& | Der Eingabedateiname. |
| outputFileName | const System::String\& | Der Name der Ausgabedatei. |
| saveFormat | Aspose::Words::SaveFormat | Das Speicherformat. |
| Muster | const System::String\& | Ein zu ersetzender String. |
| Ersetzung | const System::String\& | Ein String, um alle Vorkommen des Musters zu ersetzen. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)-Objekt, um zusätzliche Optionen anzugeben. |

### ReturnValue

Die Anzahl der vorgenommenen Ersetzungen.
## Hinweise


Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jeden Teil nach der Regel: outputFile_partIndex.extension zu erzeugen.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als eine einzelne Multi‑Frame‑TIFF‑Datei gespeichert.

## Siehe auch

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) method


Ersetzt alle Vorkommen eines angegebenen Zeichenkettenmusters durch einen Ersetzungsstring in der Eingabedatei mithilfe eines regulären Ausdrucks, mit dem angegebenen Speicherformat und zusätzlichen Optionen.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | const System::String\& | Der Eingabedateiname. |
| outputFileName | const System::String\& | Der Name der Ausgabedatei. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Die Speicheroptionen. |
| Muster | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Ein reguläres Ausdrucksmuster, das zum Finden von Übereinstimmungen verwendet wird. |
| Ersetzung | const System::String\& | Ein String, um alle Vorkommen des Musters zu ersetzen. |

### ReturnValue

Die Anzahl der vorgenommenen Ersetzungen.
## Hinweise


Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jeden Teil nach der Regel: outputFile_partIndex.extension zu erzeugen.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als eine einzelne Multi‑Frame‑TIFF‑Datei gespeichert.

## Siehe auch

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Ersetzt alle Vorkommen eines angegebenen Zeichenkettenmusters durch einen Ersetzungsstring in der Eingabedatei mithilfe eines regulären Ausdrucks, mit dem angegebenen Speicherformat und zusätzlichen Optionen.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | const System::String\& | Der Eingabedateiname. |
| outputFileName | const System::String\& | Der Name der Ausgabedatei. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Die Speicheroptionen. |
| Muster | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Ein reguläres Ausdrucksmuster, das zum Finden von Übereinstimmungen verwendet wird. |
| Ersetzung | const System::String\& | Ein String, um alle Vorkommen des Musters zu ersetzen. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)-Objekt, um zusätzliche Optionen anzugeben. |

### ReturnValue

Die Anzahl der vorgenommenen Ersetzungen.
## Hinweise


Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jeden Teil nach der Regel: outputFile_partIndex.extension zu erzeugen.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als eine einzelne Multi‑Frame‑TIFF‑Datei gespeichert.

## Siehe auch

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::String\&) method


Ersetzt alle Vorkommen eines angegebenen Zeichenkettenmusters durch einen Ersetzungsstring in der Eingabedatei, mit dem angegebenen Speicherformat und zusätzlichen Optionen.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &pattern, const System::String &replacement)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | const System::String\& | Der Eingabedateiname. |
| outputFileName | const System::String\& | Der Name der Ausgabedatei. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Die Speicheroptionen. |
| Muster | const System::String\& | Ein zu ersetzender String. |
| Ersetzung | const System::String\& | Ein String, um alle Vorkommen des Musters zu ersetzen. |

### ReturnValue

Die Anzahl der vorgenommenen Ersetzungen.
## Hinweise


Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jeden Teil nach der Regel: outputFile_partIndex.extension zu erzeugen.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als eine einzelne Multi‑Frame‑TIFF‑Datei gespeichert.

## Siehe auch

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Ersetzt alle Vorkommen eines angegebenen Zeichenkettenmusters durch einen Ersetzungsstring in der Eingabedatei, mit dem angegebenen Speicherformat und zusätzlichen Optionen.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | const System::String\& | Der Eingabedateiname. |
| outputFileName | const System::String\& | Der Name der Ausgabedatei. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Die Speicheroptionen. |
| Muster | const System::String\& | Ein zu ersetzender String. |
| Ersetzung | const System::String\& | Ein String, um alle Vorkommen des Musters zu ersetzen. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)-Objekt, um zusätzliche Optionen anzugeben. |

### ReturnValue

Die Anzahl der vorgenommenen Ersetzungen.
## Hinweise


Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jeden Teil nach der Regel: outputFile_partIndex.extension zu erzeugen.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als eine einzelne Multi‑Frame‑TIFF‑Datei gespeichert.

## Siehe auch

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) method


Ersetzt alle Vorkommen eines angegebenen Zeichenkettenmusters durch einen Ersetzungsstring in der Eingabedatei mithilfe eines regulären Ausdrucks.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | const System::String\& | Der Eingabedateiname. |
| outputFileName | const System::String\& | Der Name der Ausgabedatei. |
| Muster | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Ein reguläres Ausdrucksmuster, das zum Finden von Übereinstimmungen verwendet wird. |
| Ersetzung | const System::String\& | Ein String, um alle Vorkommen des Musters zu ersetzen. |

### ReturnValue

Die Anzahl der vorgenommenen Ersetzungen.
## Hinweise


Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jeden Teil nach der Regel: outputFile_partIndex.extension zu erzeugen.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als eine einzelne Multi‑Frame‑TIFF‑Datei gespeichert.

## Siehe auch

* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, const System::String\&, const System::String\&) method


Ersetzt alle Vorkommen eines angegebenen Zeichenkettenmusters durch einen Ersetzungsstring in der Eingabedatei.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, const System::String &pattern, const System::String &replacement)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | const System::String\& | Der Eingabedateiname. |
| outputFileName | const System::String\& | Der Name der Ausgabedatei. |
| Muster | const System::String\& | Ein zu ersetzender String. |
| Ersetzung | const System::String\& | Ein String, um alle Vorkommen des Musters zu ersetzen. |

### ReturnValue

Die Anzahl der vorgenommenen Ersetzungen.
## Hinweise


Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jeden Teil nach der Regel: outputFile_partIndex.extension zu erzeugen.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als eine einzelne Multi‑Frame‑TIFF‑Datei gespeichert.

## Siehe auch

* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
