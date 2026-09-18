---
title: "Aspose::Words::LowCode::Comparer::Compare‑Methode"
linktitle: "Compare"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::LowCode::Comparer::Compare‑Methode. Vergleicht zwei aus Streams geladene Dokumente mit zusätzlichen Optionen und speichert die Unterschiede in den bereitgestellten Ausgabestream im angegebenen Speicherformat, wobei Änderungen als eine Reihe von Bearbeitungs‑ und Formatierungsrevisionen in C++ erzeugt werden."
type: docs
weight: 1000
url: /de/cpp/aspose.words.lowcode/comparer/compare/
---
## Comparer::Compare(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime) method


Vergleicht zwei Dokumente, die aus Streams geladen wurden, mit zusätzlichen Optionen und speichert die Unterschiede in den bereitgestellten Ausgabestream im angegebenen Speicherformat, wobei Änderungen als eine Reihe von Bearbeitungs- und Formatierungsrevisionen erzeugt werden.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::SharedPtr<System::IO::Stream> &v1, const System::SharedPtr<System::IO::Stream> &v2, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::String &author, System::DateTime dateTime)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| v1 | const System::SharedPtr\<System::IO::Stream\>\& | Das Originaldokument. |
| v2 | const System::SharedPtr\<System::IO::Stream\>\& | Das geänderte Dokument. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Der Ausgabestream. |
| saveFormat | Aspose::Words::SaveFormat | Das Speicherformat der Ausgabe. |
| Autor | const System::String\& | Initialen des Autors, die für Revisionen verwendet werden. |
| dateTime | System::DateTime | Das Datum und die Uhrzeit, die für Revisionen verwendet werden sollen. |
## Hinweise


Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird nur die erste Seite der Ausgabe in den angegebenen Stream gespeichert.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als ein einzelnes Multi‑Frame‑TIFF in den angegebenen Stream gespeichert.

## Siehe auch

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) method


Vergleicht zwei Dokumente, die aus Streams geladen wurden, mit zusätzlichen Optionen und speichert die Unterschiede in den bereitgestellten Ausgabestream im angegebenen Speicherformat, wobei Änderungen als eine Reihe von Bearbeitungs- und Formatierungsrevisionen erzeugt werden.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::SharedPtr<System::IO::Stream> &v1, const System::SharedPtr<System::IO::Stream> &v2, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::String &author, System::DateTime dateTime, const System::SharedPtr<Aspose::Words::Comparing::CompareOptions> &compareOptions)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| v1 | const System::SharedPtr\<System::IO::Stream\>\& | Das Originaldokument. |
| v2 | const System::SharedPtr\<System::IO::Stream\>\& | Das geänderte Dokument. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Der Ausgabestream. |
| saveFormat | Aspose::Words::SaveFormat | Das Speicherformat der Ausgabe. |
| Autor | const System::String\& | Initialen des Autors, die für Revisionen verwendet werden. |
| dateTime | System::DateTime | Das Datum und die Uhrzeit, die für Revisionen verwendet werden sollen. |
| compareOptions | const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\& | Vergleichsoptionen für [Document](../../../aspose.words/document/). |
## Hinweise


Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird nur die erste Seite der Ausgabe in den angegebenen Stream gespeichert.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als ein einzelnes Multi‑Frame‑TIFF in den angegebenen Stream gespeichert.

## Siehe auch

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime) method


Vergleicht zwei Dokumente, die aus Streams geladen wurden, mit zusätzlichen Optionen und speichert die Unterschiede in den bereitgestellten Ausgabestream im angegebenen Speicherformat, wobei Änderungen als eine Reihe von Bearbeitungs- und Formatierungsrevisionen erzeugt werden.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::SharedPtr<System::IO::Stream> &v1, const System::SharedPtr<System::IO::Stream> &v2, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &author, System::DateTime dateTime)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| v1 | const System::SharedPtr\<System::IO::Stream\>\& | Das Originaldokument. |
| v2 | const System::SharedPtr\<System::IO::Stream\>\& | Das geänderte Dokument. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Der Ausgabestream. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Die Speicheroptionen der Ausgabe. |
| Autor | const System::String\& | Initialen des Autors, die für Revisionen verwendet werden. |
| dateTime | System::DateTime | Das Datum und die Uhrzeit, die für Revisionen verwendet werden sollen. |
## Hinweise


Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird nur die erste Seite der Ausgabe in den angegebenen Stream gespeichert.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als ein einzelnes Multi‑Frame‑TIFF in den angegebenen Stream gespeichert.

## Siehe auch

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) method


Vergleicht zwei Dokumente, die aus Streams geladen wurden, mit zusätzlichen Optionen und speichert die Unterschiede in den bereitgestellten Ausgabestream im angegebenen Speicherformat, wobei Änderungen als eine Reihe von Bearbeitungs- und Formatierungsrevisionen erzeugt werden.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::SharedPtr<System::IO::Stream> &v1, const System::SharedPtr<System::IO::Stream> &v2, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &author, System::DateTime dateTime, const System::SharedPtr<Aspose::Words::Comparing::CompareOptions> &compareOptions)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| v1 | const System::SharedPtr\<System::IO::Stream\>\& | Das Originaldokument. |
| v2 | const System::SharedPtr\<System::IO::Stream\>\& | Das geänderte Dokument. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Der Ausgabestream. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Die Speicheroptionen der Ausgabe. |
| Autor | const System::String\& | Initialen des Autors, die für Revisionen verwendet werden. |
| dateTime | System::DateTime | Das Datum und die Uhrzeit, die für Revisionen verwendet werden sollen. |
| compareOptions | const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\& | Vergleichsoptionen für [Document](../../../aspose.words/document/). |
## Hinweise


Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird nur die erste Seite der Ausgabe in den angegebenen Stream gespeichert.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als ein einzelnes Multi‑Frame‑TIFF in den angegebenen Stream gespeichert.

## Siehe auch

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::String\&, const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime) method


Vergleicht zwei Dokumente mit zusätzlichen Optionen und speichert die Unterschiede in die angegebene Ausgabedatei im angegebenen Speicherformat, wobei Änderungen als eine Reihe von Bearbeitungs- und Formatierungsrevisionen erzeugt werden.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::String &v1, const System::String &v2, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::String &author, System::DateTime dateTime)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| v1 | const System::String\& | Das Originaldokument. |
| v2 | const System::String\& | Das geänderte Dokument. |
| outputFileName | const System::String\& | Der Name der Ausgabedatei. |
| saveFormat | Aspose::Words::SaveFormat | Das Speicherformat der Ausgabe. |
| Autor | const System::String\& | Initialen des Autors, die für Revisionen verwendet werden. |
| dateTime | System::DateTime | Das Datum und die Uhrzeit, die für Revisionen verwendet werden sollen. |
## Hinweise


Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jeden Teil nach der Regel: outputFile_partIndex.extension zu erzeugen.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als eine einzelne Multi‑Frame‑TIFF‑Datei gespeichert.

## Siehe auch

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::String\&, const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) method


Vergleicht zwei Dokumente mit zusätzlichen Optionen und speichert die Unterschiede in die angegebene Ausgabedatei im angegebenen Speicherformat, wobei Änderungen als eine Reihe von Bearbeitungs- und Formatierungsrevisionen erzeugt werden.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::String &v1, const System::String &v2, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::String &author, System::DateTime dateTime, const System::SharedPtr<Aspose::Words::Comparing::CompareOptions> &compareOptions)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| v1 | const System::String\& | Das Originaldokument. |
| v2 | const System::String\& | Das geänderte Dokument. |
| outputFileName | const System::String\& | Der Name der Ausgabedatei. |
| saveFormat | Aspose::Words::SaveFormat | Das Speicherformat der Ausgabe. |
| Autor | const System::String\& | Initialen des Autors, die für Revisionen verwendet werden. |
| dateTime | System::DateTime | Das Datum und die Uhrzeit, die für Revisionen verwendet werden sollen. |
| compareOptions | const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\& | Vergleichsoptionen für [Document](../../../aspose.words/document/). |
## Hinweise


Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jeden Teil nach der Regel: outputFile_partIndex.extension zu erzeugen.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als eine einzelne Multi‑Frame‑TIFF‑Datei gespeichert.

## Siehe auch

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::String\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime) method


Vergleicht zwei Dokumente mit zusätzlichen Optionen und speichert die Unterschiede in die angegebene Ausgabedatei im angegebenen Speicherformat, wobei Änderungen als eine Reihe von Bearbeitungs- und Formatierungsrevisionen erzeugt werden.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::String &v1, const System::String &v2, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &author, System::DateTime dateTime)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| v1 | const System::String\& | Das Originaldokument. |
| v2 | const System::String\& | Das geänderte Dokument. |
| outputFileName | const System::String\& | Der Name der Ausgabedatei. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Die Speicheroptionen der Ausgabe. |
| Autor | const System::String\& | Initialen des Autors, die für Revisionen verwendet werden. |
| dateTime | System::DateTime | Das Datum und die Uhrzeit, die für Revisionen verwendet werden sollen. |
## Hinweise


Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jeden Teil nach der Regel: outputFile_partIndex.extension zu erzeugen.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als eine einzelne Multi‑Frame‑TIFF‑Datei gespeichert.

## Siehe auch

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::String\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) method


Vergleicht zwei Dokumente mit zusätzlichen Optionen und speichert die Unterschiede in die angegebene Ausgabedatei im angegebenen Speicherformat, wobei Änderungen als eine Reihe von Bearbeitungs- und Formatierungsrevisionen erzeugt werden.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::String &v1, const System::String &v2, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &author, System::DateTime dateTime, const System::SharedPtr<Aspose::Words::Comparing::CompareOptions> &compareOptions)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| v1 | const System::String\& | Das Originaldokument. |
| v2 | const System::String\& | Das geänderte Dokument. |
| outputFileName | const System::String\& | Der Name der Ausgabedatei. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Die Speicheroptionen der Ausgabe. |
| Autor | const System::String\& | Initialen des Autors, die für Revisionen verwendet werden. |
| dateTime | System::DateTime | Das Datum und die Uhrzeit, die für Revisionen verwendet werden sollen. |
| compareOptions | const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\& | Vergleichsoptionen für [Document](../../../aspose.words/document/). |
## Hinweise


Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jeden Teil nach der Regel: outputFile_partIndex.extension zu erzeugen.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als eine einzelne Multi‑Frame‑TIFF‑Datei gespeichert.

## Siehe auch

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::String\&, const System::String\&, const System::String\&, const System::String\&, System::DateTime) method


Vergleicht zwei Dokumente mit zusätzlichen Optionen und speichert die Unterschiede in die angegebene Ausgabedatei, wobei Änderungen als eine Reihe von Bearbeitungs- und Formatierungsrevisionen erzeugt werden.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::String &v1, const System::String &v2, const System::String &outputFileName, const System::String &author, System::DateTime dateTime)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| v1 | const System::String\& | Das Originaldokument. |
| v2 | const System::String\& | Das geänderte Dokument. |
| outputFileName | const System::String\& | Der Name der Ausgabedatei. |
| Autor | const System::String\& | Initialen des Autors, die für Revisionen verwendet werden. |
| dateTime | System::DateTime | Das Datum und die Uhrzeit, die für Revisionen verwendet werden sollen. |
## Hinweise


Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jeden Teil nach der Regel: outputFile_partIndex.extension zu erzeugen.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als eine einzelne Multi‑Frame‑TIFF‑Datei gespeichert.

## Siehe auch

* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::String\&, const System::String\&, const System::String\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) method


Vergleicht zwei Dokumente mit zusätzlichen Optionen und speichert die Unterschiede in die angegebene Ausgabedatei, wobei Änderungen als eine Reihe von Bearbeitungs- und Formatierungsrevisionen erzeugt werden.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::String &v1, const System::String &v2, const System::String &outputFileName, const System::String &author, System::DateTime dateTime, const System::SharedPtr<Aspose::Words::Comparing::CompareOptions> &compareOptions)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| v1 | const System::String\& | Das Originaldokument. |
| v2 | const System::String\& | Das geänderte Dokument. |
| outputFileName | const System::String\& | Der Name der Ausgabedatei. |
| Autor | const System::String\& | Initialen des Autors, die für Revisionen verwendet werden. |
| dateTime | System::DateTime | Das Datum und die Uhrzeit, die für Revisionen verwendet werden sollen. |
| compareOptions | const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\& | Vergleichsoptionen für [Document](../../../aspose.words/document/). |
## Hinweise


Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jeden Teil nach der Regel: outputFile_partIndex.extension zu erzeugen.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als eine einzelne Multi‑Frame‑TIFF‑Datei gespeichert.

## Siehe auch

* Class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
