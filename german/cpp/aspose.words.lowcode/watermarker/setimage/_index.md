---
title: "Aspose::Words::LowCode::Watermarker::SetImage Methode"
linktitle: "SetImage"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::LowCode::Watermarker::SetImage Methode. Fügt dem Dokument ein Bildwasserzeichen aus Streams mit Optionen in C++ hinzu."
type: docs
weight: 1000
url: /de/cpp/aspose.words.lowcode/watermarker/setimage/
---
## Watermarker::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Drawing::Image\>\&) method


Fügt dem Dokument ein Bildwasserzeichen aus Streams mit Optionen hinzu.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<System::Drawing::Image> &watermarkImage)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Der Eingabestream. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Der Ausgabestream. |
| saveFormat | Aspose::Words::SaveFormat | Das Speicherformat. |
| watermarkImage | const System::SharedPtr\<System::Drawing::Image\>\& | Bild, das als Wasserzeichen angezeigt wird. |
## Hinweise


Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird nur die erste Seite der Ausgabe in den angegebenen Stream gespeichert.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als ein einzelnes Multi‑Frame‑TIFF in den angegebenen Stream gespeichert.

## Siehe auch

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Drawing::Image\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Fügt dem Dokument ein Bildwasserzeichen aus Streams mit Optionen hinzu.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<System::Drawing::Image> &watermarkImage, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Der Eingabestream. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Der Ausgabestream. |
| saveFormat | Aspose::Words::SaveFormat | Das Speicherformat. |
| watermarkImage | const System::SharedPtr\<System::Drawing::Image\>\& | Bild, das als Wasserzeichen angezeigt wird. |
| options | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Definiert zusätzliche Optionen für das Bildwasserzeichen. |
## Hinweise


Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird nur die erste Seite der Ausgabe in den angegebenen Stream gespeichert.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als ein einzelnes Multi‑Frame‑TIFF in den angegebenen Stream gespeichert.

## Siehe auch

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::IO::Stream\>\&) method


Fügt dem Dokument ein Bildwasserzeichen aus Streams mit Optionen hinzu.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<System::IO::Stream> &watermarkImageStream)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Der Eingabestream. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Der Ausgabestream. |
| saveFormat | Aspose::Words::SaveFormat | Das Speicherformat. |
| watermarkImageStream | const System::SharedPtr\<System::IO::Stream\>\& | Bildstrom, der als Wasserzeichen angezeigt wird. |
## Hinweise


Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird nur die erste Seite der Ausgabe in den angegebenen Stream gespeichert.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als ein einzelnes Multi‑Frame‑TIFF in den angegebenen Stream gespeichert.

## Siehe auch

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Fügt dem Dokument ein Bildwasserzeichen aus Streams mit Optionen hinzu.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<System::IO::Stream> &watermarkImageStream, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Der Eingabestream. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Der Ausgabestream. |
| saveFormat | Aspose::Words::SaveFormat | Das Speicherformat. |
| watermarkImageStream | const System::SharedPtr\<System::IO::Stream\>\& | Bildstrom, der als Wasserzeichen angezeigt wird. |
| options | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Definiert zusätzliche Optionen für das Bildwasserzeichen. |
## Hinweise


Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird nur die erste Seite der Ausgabe in den angegebenen Stream gespeichert.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als ein einzelnes Multi‑Frame‑TIFF in den angegebenen Stream gespeichert.

## Siehe auch

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Drawing::Image\>\&) method


Fügt dem Dokument ein Bildwasserzeichen aus Streams mit Optionen hinzu.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<System::Drawing::Image> &watermarkImage)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Der Eingabestream. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Der Ausgabestream. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Die Speicheroptionen. |
| watermarkImage | const System::SharedPtr\<System::Drawing::Image\>\& | Bild, das als Wasserzeichen angezeigt wird. |
## Hinweise


Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird nur die erste Seite der Ausgabe in den angegebenen Stream gespeichert.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als ein einzelnes Multi‑Frame‑TIFF in den angegebenen Stream gespeichert.

## Siehe auch

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Drawing::Image\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Fügt dem Dokument ein Bildwasserzeichen aus Streams mit Optionen hinzu.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<System::Drawing::Image> &watermarkImage, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Der Eingabestream. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Der Ausgabestream. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Die Speicheroptionen. |
| watermarkImage | const System::SharedPtr\<System::Drawing::Image\>\& | Bild, das als Wasserzeichen angezeigt wird. |
| options | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Definiert zusätzliche Optionen für das Bildwasserzeichen. |
## Hinweise


Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird nur die erste Seite der Ausgabe in den angegebenen Stream gespeichert.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als ein einzelnes Multi‑Frame‑TIFF in den angegebenen Stream gespeichert.

## Siehe auch

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::IO::Stream\>\&) method


Fügt dem Dokument ein Bildwasserzeichen aus Streams mit Optionen hinzu.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<System::IO::Stream> &watermarkImageStream)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Der Eingabestream. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Der Ausgabestream. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Die Speicheroptionen. |
| watermarkImageStream | const System::SharedPtr\<System::IO::Stream\>\& | Bildstrom, der als Wasserzeichen angezeigt wird. |
## Hinweise


Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird nur die erste Seite der Ausgabe in den angegebenen Stream gespeichert.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als ein einzelnes Multi‑Frame‑TIFF in den angegebenen Stream gespeichert.

## Siehe auch

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Fügt dem Dokument ein Bildwasserzeichen aus Streams mit Optionen hinzu.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<System::IO::Stream> &watermarkImageStream, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Der Eingabestream. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Der Ausgabestream. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Die Speicheroptionen. |
| watermarkImageStream | const System::SharedPtr\<System::IO::Stream\>\& | Bildstrom, der als Wasserzeichen angezeigt wird. |
| options | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Definiert zusätzliche Optionen für das Bildwasserzeichen. |
## Hinweise


Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird nur die erste Seite der Ausgabe in den angegebenen Stream gespeichert.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als ein einzelnes Multi‑Frame‑TIFF in den angegebenen Stream gespeichert.

## Siehe auch

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&) method


Fügt dem Dokument ein Bildwasserzeichen mit Optionen und angegebenem Speicherformat hinzu.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::String &watermarkImageFileName)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | const System::String\& | Der Eingabedateiname. |
| outputFileName | const System::String\& | Der Name der Ausgabedatei. |
| saveFormat | Aspose::Words::SaveFormat | Das Speicherformat. |
| watermarkImageFileName | const System::String\& | Bild, das als Wasserzeichen angezeigt wird. |
## Hinweise


Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jeden Teil nach der Regel: outputFile_partIndex.extension zu erzeugen.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als eine einzelne Multi‑Frame‑TIFF‑Datei gespeichert.

## Siehe auch

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Fügt dem Dokument ein Bildwasserzeichen mit Optionen und angegebenem Speicherformat hinzu.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::String &watermarkImageFileName, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | const System::String\& | Der Eingabedateiname. |
| outputFileName | const System::String\& | Der Name der Ausgabedatei. |
| saveFormat | Aspose::Words::SaveFormat | Das Speicherformat. |
| watermarkImageFileName | const System::String\& | Bild, das als Wasserzeichen angezeigt wird. |
| options | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Definiert zusätzliche Optionen für das Bildwasserzeichen. |
## Hinweise


Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jeden Teil nach der Regel: outputFile_partIndex.extension zu erzeugen.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als eine einzelne Multi‑Frame‑TIFF‑Datei gespeichert.

## Siehe auch

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&) method


Fügt dem Dokument ein Bildwasserzeichen mit Optionen und angegebenem Speicherformat hinzu.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &watermarkImageFileName)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | const System::String\& | Der Eingabedateiname. |
| outputFileName | const System::String\& | Der Name der Ausgabedatei. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Die Speicheroptionen. |
| watermarkImageFileName | const System::String\& | Bild, das als Wasserzeichen angezeigt wird. |
## Hinweise


Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jeden Teil nach der Regel: outputFile_partIndex.extension zu erzeugen.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als eine einzelne Multi‑Frame‑TIFF‑Datei gespeichert.

## Siehe auch

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Fügt dem Dokument ein Bildwasserzeichen mit Optionen und angegebenem Speicherformat hinzu.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &watermarkImageFileName, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | const System::String\& | Der Eingabedateiname. |
| outputFileName | const System::String\& | Der Name der Ausgabedatei. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Die Speicheroptionen. |
| watermarkImageFileName | const System::String\& | Bild, das als Wasserzeichen angezeigt wird. |
| options | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Definiert zusätzliche Optionen für das Bildwasserzeichen. |
## Hinweise


Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jeden Teil nach der Regel: outputFile_partIndex.extension zu erzeugen.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als eine einzelne Multi‑Frame‑TIFF‑Datei gespeichert.

## Siehe auch

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::String\&, const System::String\&, const System::String\&) method


Fügt dem Dokument ein Bildwasserzeichen hinzu.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::String &inputFileName, const System::String &outputFileName, const System::String &watermarkImageFileName)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | const System::String\& | Der Eingabedateiname. |
| outputFileName | const System::String\& | Der Name der Ausgabedatei. |
| watermarkImageFileName | const System::String\& | Bild, das als Wasserzeichen angezeigt wird. |
## Hinweise


Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jeden Teil nach der Regel: outputFile_partIndex.extension zu erzeugen.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als eine einzelne Multi‑Frame‑TIFF‑Datei gespeichert.

## Siehe auch

* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::String\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Fügt dem Dokument ein Bildwasserzeichen mit Optionen hinzu.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::String &inputFileName, const System::String &outputFileName, const System::String &watermarkImageFileName, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | const System::String\& | Der Eingabedateiname. |
| outputFileName | const System::String\& | Der Name der Ausgabedatei. |
| watermarkImageFileName | const System::String\& | Bild, das als Wasserzeichen angezeigt wird. |
| options | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Definiert zusätzliche Optionen für das Bildwasserzeichen. |
## Hinweise


Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jeden Teil nach der Regel: outputFile_partIndex.extension zu erzeugen.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als eine einzelne Multi‑Frame‑TIFF‑Datei gespeichert.

## Siehe auch

* Class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
