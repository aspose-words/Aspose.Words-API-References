---
title: "Aspose::Words::LowCode::Converter::Convert Methode"
linktitle: "Convert"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::LowCode::Converter::Convert Methode. Konvertiert das angegebene Eingabedokument in ein einzelnes Ausgabedokument unter Verwendung der angegebenen Eingabe‑ und Ausgabeströme in C++."
type: docs
weight: 1000
url: /de/cpp/aspose.words.lowcode/converter/convert/
---
## Converter::Convert(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) method


Konvertiert das angegebene Eingabedokument in ein einzelnes Ausgabedokument unter Verwendung der angegebenen Eingabe- und Ausgabeströme.

```cpp
static void Aspose::Words::LowCode::Converter::Convert(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Die Eingabeströme. |
| loadOptions | const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\& | Die Ladeoptionen des Eingabedokuments. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Der Ausgabestream. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Die Speicheroptionen. |
## Hinweise


Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird nur die erste Seite der Ausgabe in den angegebenen Stream gespeichert.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als ein einzelnes Multi‑Frame‑TIFF in den angegebenen Stream gespeichert.

## Siehe auch

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::Convert(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) method


Konvertiert das angegebene Eingabedokument in ein einzelnes Ausgabedokument unter Verwendung der angegebenen Eingabe- und Ausgabeströme.

```cpp
static void Aspose::Words::LowCode::Converter::Convert(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Der Eingabestream. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Der Ausgabestream. |
| saveFormat | Aspose::Words::SaveFormat | Das Speicherformat. |
## Hinweise


Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird nur die erste Seite der Ausgabe in den angegebenen Stream gespeichert.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als ein einzelnes Multi‑Frame‑TIFF in den angegebenen Stream gespeichert.

## Siehe auch

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::Convert(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) method


Konvertiert das angegebene Eingabedokument in ein einzelnes Ausgabedokument unter Verwendung der angegebenen Eingabe- und Ausgabeströme.

```cpp
static void Aspose::Words::LowCode::Converter::Convert(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Die Eingabeströme. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Der Ausgabestream. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Die Speicheroptionen. |
## Hinweise


Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird nur die erste Seite der Ausgabe in den angegebenen Stream gespeichert.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als ein einzelnes Multi‑Frame‑TIFF in den angegebenen Stream gespeichert.

## Siehe auch

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::Convert(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) method


Konvertiert das angegebene Eingabedokument in das Ausgabedokument unter Verwendung der angegebenen Eingabe- und Ausgabedateinamen sowie seiner Lade-/Speicheroptionen.

```cpp
static void Aspose::Words::LowCode::Converter::Convert(const System::String &inputFile, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions, const System::String &outputFile, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFile | const System::String\& | Der Eingabedateiname. |
| loadOptions | const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\& | Die Ladeoptionen des Eingabedokuments. |
| outputFile | const System::String\& | Der Name der Ausgabedatei. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Die Speicheroptionen. |
## Hinweise


Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jeden Teil nach der Regel: outputFile_partIndex.extension zu erzeugen.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als eine einzelne Multi‑Frame‑TIFF‑Datei gespeichert.

## Siehe auch

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::Convert(const System::String\&, const System::String\&) method


Konvertiert das angegebene Eingabedokument in das Ausgabedokument unter Verwendung der angegebenen Eingabe- und Ausgabedateinamen sowie deren Erweiterungen.

```cpp
static void Aspose::Words::LowCode::Converter::Convert(const System::String &inputFile, const System::String &outputFile)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFile | const System::String\& | Der Eingabedateiname. |
| outputFile | const System::String\& | Der Name der Ausgabedatei. |
## Hinweise


Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jeden Teil nach der Regel: outputFile_partIndex.extension zu erzeugen.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als eine einzelne Multi‑Frame‑TIFF‑Datei gespeichert.

## Siehe auch

* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::Convert(const System::String\&, const System::String\&, Aspose::Words::SaveFormat) method


Konvertiert das angegebene Eingabedokument in das Ausgabedokument unter Verwendung der angegebenen Eingabe- und Ausgabedateinamen und des endgültigen Dokumentformats.

```cpp
static void Aspose::Words::LowCode::Converter::Convert(const System::String &inputFile, const System::String &outputFile, Aspose::Words::SaveFormat saveFormat)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFile | const System::String\& | Der Eingabedateiname. |
| outputFile | const System::String\& | Der Name der Ausgabedatei. |
| saveFormat | Aspose::Words::SaveFormat | Das Speicherformat. |
## Hinweise


Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jeden Teil nach der Regel: outputFile_partIndex.extension zu erzeugen.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als eine einzelne Multi‑Frame‑TIFF‑Datei gespeichert.

## Siehe auch

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::Convert(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) method


Konvertiert das angegebene Eingabedokument in das Ausgabedokument unter Verwendung der angegebenen Eingabe- und Ausgabedateinamen sowie der Speicheroptionen.

```cpp
static void Aspose::Words::LowCode::Converter::Convert(const System::String &inputFile, const System::String &outputFile, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFile | const System::String\& | Der Eingabedateiname. |
| outputFile | const System::String\& | Der Name der Ausgabedatei. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Die Speicheroptionen. |
## Hinweise


Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jeden Teil nach der Regel: outputFile_partIndex.extension zu erzeugen.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als eine einzelne Multi‑Frame‑TIFF‑Datei gespeichert.

## Siehe auch

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
