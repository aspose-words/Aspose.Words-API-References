---
title: "Aspose::Words::LowCode::Watermarker::SetImage metod"
linktitle: "SetImage"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::LowCode::Watermarker::SetImage metod. Lägger till en bildvattenstämpel i dokumentet från strömmar med alternativ i C++."
type: docs
weight: 1000
url: /sv/cpp/aspose.words.lowcode/watermarker/setimage/
---
## Watermarker::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Drawing::Image\>\&) method


Lägger till en bildvattenstämpel i dokumentet från strömmar med alternativ.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<System::Drawing::Image> &watermarkImage)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Inmatningsströmmen. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Utdataflödet. |
| saveFormat | Aspose::Words::SaveFormat | Sparformatet. |
| watermarkImage | const System::SharedPtr\<System::Drawing::Image\>\& | Bild som visas som en vattenstämpel. |
## Anmärkningar


Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas endast den första sidan av utdata till den angivna strömmen.

Om utdataformatet är TIFF sparas utdata som en enda flerbilds‑TIFF till den angivna strömmen.

## Se även

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Drawing::Image\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Lägger till en bildvattenstämpel i dokumentet från strömmar med alternativ.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<System::Drawing::Image> &watermarkImage, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Inmatningsströmmen. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Utdataflödet. |
| saveFormat | Aspose::Words::SaveFormat | Sparformatet. |
| watermarkImage | const System::SharedPtr\<System::Drawing::Image\>\& | Bild som visas som en vattenstämpel. |
| options | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Definierar ytterligare alternativ för bildvattenstämpeln. |
## Anmärkningar


Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas endast den första sidan av utdata till den angivna strömmen.

Om utdataformatet är TIFF sparas utdata som en enda flerbilds‑TIFF till den angivna strömmen.

## Se även

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::IO::Stream\>\&) method


Lägger till en bildvattenstämpel i dokumentet från strömmar med alternativ.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<System::IO::Stream> &watermarkImageStream)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Inmatningsströmmen. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Utdataflödet. |
| saveFormat | Aspose::Words::SaveFormat | Sparformatet. |
| watermarkImageStream | const System::SharedPtr\<System::IO::Stream\>\& | Bildström som visas som en vattenstämpel. |
## Anmärkningar


Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas endast den första sidan av utdata till den angivna strömmen.

Om utdataformatet är TIFF sparas utdata som en enda flerbilds‑TIFF till den angivna strömmen.

## Se även

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Lägger till en bildvattenstämpel i dokumentet från strömmar med alternativ.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<System::IO::Stream> &watermarkImageStream, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Inmatningsströmmen. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Utdataflödet. |
| saveFormat | Aspose::Words::SaveFormat | Sparformatet. |
| watermarkImageStream | const System::SharedPtr\<System::IO::Stream\>\& | Bildström som visas som en vattenstämpel. |
| options | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Definierar ytterligare alternativ för bildvattenstämpeln. |
## Anmärkningar


Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas endast den första sidan av utdata till den angivna strömmen.

Om utdataformatet är TIFF sparas utdata som en enda flerbilds‑TIFF till den angivna strömmen.

## Se även

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Drawing::Image\>\&) method


Lägger till en bildvattenstämpel i dokumentet från strömmar med alternativ.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<System::Drawing::Image> &watermarkImage)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Inmatningsströmmen. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Utdataflödet. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Sparalternativen. |
| watermarkImage | const System::SharedPtr\<System::Drawing::Image\>\& | Bild som visas som en vattenstämpel. |
## Anmärkningar


Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas endast den första sidan av utdata till den angivna strömmen.

Om utdataformatet är TIFF sparas utdata som en enda flerbilds‑TIFF till den angivna strömmen.

## Se även

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Drawing::Image\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Lägger till en bildvattenstämpel i dokumentet från strömmar med alternativ.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<System::Drawing::Image> &watermarkImage, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Inmatningsströmmen. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Utdataflödet. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Sparalternativen. |
| watermarkImage | const System::SharedPtr\<System::Drawing::Image\>\& | Bild som visas som en vattenstämpel. |
| options | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Definierar ytterligare alternativ för bildvattenstämpeln. |
## Anmärkningar


Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas endast den första sidan av utdata till den angivna strömmen.

Om utdataformatet är TIFF sparas utdata som en enda flerbilds‑TIFF till den angivna strömmen.

## Se även

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::IO::Stream\>\&) method


Lägger till en bildvattenstämpel i dokumentet från strömmar med alternativ.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<System::IO::Stream> &watermarkImageStream)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Inmatningsströmmen. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Utdataflödet. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Sparalternativen. |
| watermarkImageStream | const System::SharedPtr\<System::IO::Stream\>\& | Bildström som visas som en vattenstämpel. |
## Anmärkningar


Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas endast den första sidan av utdata till den angivna strömmen.

Om utdataformatet är TIFF sparas utdata som en enda flerbilds‑TIFF till den angivna strömmen.

## Se även

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Lägger till en bildvattenstämpel i dokumentet från strömmar med alternativ.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<System::IO::Stream> &watermarkImageStream, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Inmatningsströmmen. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Utdataflödet. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Sparalternativen. |
| watermarkImageStream | const System::SharedPtr\<System::IO::Stream\>\& | Bildström som visas som en vattenstämpel. |
| options | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Definierar ytterligare alternativ för bildvattenstämpeln. |
## Anmärkningar


Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas endast den första sidan av utdata till den angivna strömmen.

Om utdataformatet är TIFF sparas utdata som en enda flerbilds‑TIFF till den angivna strömmen.

## Se även

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&) method


Lägger till en bildvattenstämpel i dokumentet med alternativ och specificerat sparformat.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::String &watermarkImageFileName)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputFileName | const System::String\& | Inmatningsfilnamnet. |
| outputFileName | const System::String\& | Utdatans filnamn. |
| saveFormat | Aspose::Words::SaveFormat | Sparformatet. |
| watermarkImageFileName | const System::String\& | Bild som visas som en vattenstämpel. |
## Anmärkningar


Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas varje sida av utdata som en separat fil. Det angivna utdatafilnamnet kommer att användas för att generera filnamn för varje del enligt regeln: outputFile_partIndex.extension.

Om utdataformatet är TIFF sparas utdata som en enda flerbilds‑TIFF‑fil.

## Se även

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Lägger till en bildvattenstämpel i dokumentet med alternativ och specificerat sparformat.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::String &watermarkImageFileName, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputFileName | const System::String\& | Inmatningsfilnamnet. |
| outputFileName | const System::String\& | Utdatans filnamn. |
| saveFormat | Aspose::Words::SaveFormat | Sparformatet. |
| watermarkImageFileName | const System::String\& | Bild som visas som en vattenstämpel. |
| options | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Definierar ytterligare alternativ för bildvattenstämpeln. |
## Anmärkningar


Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas varje sida av utdata som en separat fil. Det angivna utdatafilnamnet kommer att användas för att generera filnamn för varje del enligt regeln: outputFile_partIndex.extension.

Om utdataformatet är TIFF sparas utdata som en enda flerbilds‑TIFF‑fil.

## Se även

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&) method


Lägger till en bildvattenstämpel i dokumentet med alternativ och specificerat sparformat.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &watermarkImageFileName)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputFileName | const System::String\& | Inmatningsfilnamnet. |
| outputFileName | const System::String\& | Utdatans filnamn. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Sparalternativen. |
| watermarkImageFileName | const System::String\& | Bild som visas som en vattenstämpel. |
## Anmärkningar


Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas varje sida av utdata som en separat fil. Det angivna utdatafilnamnet kommer att användas för att generera filnamn för varje del enligt regeln: outputFile_partIndex.extension.

Om utdataformatet är TIFF sparas utdata som en enda flerbilds‑TIFF‑fil.

## Se även

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Lägger till en bildvattenstämpel i dokumentet med alternativ och specificerat sparformat.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &watermarkImageFileName, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputFileName | const System::String\& | Inmatningsfilnamnet. |
| outputFileName | const System::String\& | Utdatans filnamn. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Sparalternativen. |
| watermarkImageFileName | const System::String\& | Bild som visas som en vattenstämpel. |
| options | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Definierar ytterligare alternativ för bildvattenstämpeln. |
## Anmärkningar


Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas varje sida av utdata som en separat fil. Det angivna utdatafilnamnet kommer att användas för att generera filnamn för varje del enligt regeln: outputFile_partIndex.extension.

Om utdataformatet är TIFF sparas utdata som en enda flerbilds‑TIFF‑fil.

## Se även

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::String\&, const System::String\&, const System::String\&) method


Lägger till en bildvattenstämpel i dokumentet.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::String &inputFileName, const System::String &outputFileName, const System::String &watermarkImageFileName)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputFileName | const System::String\& | Inmatningsfilnamnet. |
| outputFileName | const System::String\& | Utdatans filnamn. |
| watermarkImageFileName | const System::String\& | Bild som visas som en vattenstämpel. |
## Anmärkningar


Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas varje sida av utdata som en separat fil. Det angivna utdatafilnamnet kommer att användas för att generera filnamn för varje del enligt regeln: outputFile_partIndex.extension.

Om utdataformatet är TIFF sparas utdata som en enda flerbilds‑TIFF‑fil.

## Se även

* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::String\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Lägger till en bildvattenstämpel i dokumentet med alternativ.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::String &inputFileName, const System::String &outputFileName, const System::String &watermarkImageFileName, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputFileName | const System::String\& | Inmatningsfilnamnet. |
| outputFileName | const System::String\& | Utdatans filnamn. |
| watermarkImageFileName | const System::String\& | Bild som visas som en vattenstämpel. |
| options | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Definierar ytterligare alternativ för bildvattenstämpeln. |
## Anmärkningar


Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas varje sida av utdata som en separat fil. Det angivna utdatafilnamnet kommer att användas för att generera filnamn för varje del enligt regeln: outputFile_partIndex.extension.

Om utdataformatet är TIFF sparas utdata som en enda flerbilds‑TIFF‑fil.

## Se även

* Class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
