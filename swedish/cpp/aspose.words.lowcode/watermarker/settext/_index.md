---
title: "Aspose::Words::LowCode::Watermarker::SetText metod"
linktitle: "SetText"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::LowCode::Watermarker::SetText metod. Lägger till en textvattenstämpel i dokumentet från strömmar med alternativ i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.lowcode/watermarker/settext/
---
## Watermarker::SetText(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&) method


Lägger till en textvattenstämpel i dokumentet från strömmar med alternativ.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetText(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::String &watermarkText)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Inmatningsströmmen. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Utdataflödet. |
| saveFormat | Aspose::Words::SaveFormat | Sparformatet. |
| watermarkText | const System::String\& | Text som visas som en vattenstämpel. |
## Anmärkningar


Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas endast den första sidan av utdata till den angivna strömmen.

Om utdataformatet är TIFF sparas utdata som en enda flerbilds‑TIFF till den angivna strömmen.

## Se även

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetText(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) method


Lägger till en textvattenstämpel i dokumentet från strömmar med alternativ.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetText(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::String &watermarkText, const System::SharedPtr<Aspose::Words::TextWatermarkOptions> &options)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Inmatningsströmmen. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Utdataflödet. |
| saveFormat | Aspose::Words::SaveFormat | Sparformatet. |
| watermarkText | const System::String\& | Text som visas som en vattenstämpel. |
| options | const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\& | Definierar ytterligare alternativ för textvattenstämpeln. |
## Anmärkningar


Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas endast den första sidan av utdata till den angivna strömmen.

Om utdataformatet är TIFF sparas utdata som en enda flerbilds‑TIFF till den angivna strömmen.

## Se även

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetText(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&) method


Lägger till en textvattenstämpel i dokumentet från strömmar med alternativ.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetText(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &watermarkText)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Inmatningsströmmen. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Utdataflödet. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Sparalternativen. |
| watermarkText | const System::String\& | Text som visas som en vattenstämpel. |
## Anmärkningar


Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas endast den första sidan av utdata till den angivna strömmen.

Om utdataformatet är TIFF sparas utdata som en enda flerbilds‑TIFF till den angivna strömmen.

## Se även

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetText(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) method


Lägger till en textvattenstämpel i dokumentet från strömmar med alternativ.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetText(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &watermarkText, const System::SharedPtr<Aspose::Words::TextWatermarkOptions> &options)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Inmatningsströmmen. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Utdataflödet. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Sparalternativen. |
| watermarkText | const System::String\& | Text som visas som en vattenstämpel. |
| options | const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\& | Definierar ytterligare alternativ för textvattenstämpeln. |
## Anmärkningar


Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas endast den första sidan av utdata till den angivna strömmen.

Om utdataformatet är TIFF sparas utdata som en enda flerbilds‑TIFF till den angivna strömmen.

## Se även

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetText(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&) method


Lägger till en textvattenstämpel i dokumentet med alternativ och specificerat sparformat.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetText(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::String &watermarkText)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputFileName | const System::String\& | Inmatningsfilnamnet. |
| outputFileName | const System::String\& | Utdatans filnamn. |
| saveFormat | Aspose::Words::SaveFormat | Sparformatet. |
| watermarkText | const System::String\& | Text som visas som en vattenstämpel. |
## Anmärkningar


Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas varje sida av utdata som en separat fil. Det angivna utdatafilnamnet kommer att användas för att generera filnamn för varje del enligt regeln: outputFile_partIndex.extension.

Om utdataformatet är TIFF sparas utdata som en enda flerbilds‑TIFF‑fil.

## Se även

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetText(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) method


Lägger till en textvattenstämpel i dokumentet med alternativ och specificerat sparformat.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetText(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::String &watermarkText, const System::SharedPtr<Aspose::Words::TextWatermarkOptions> &options)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputFileName | const System::String\& | Inmatningsfilnamnet. |
| outputFileName | const System::String\& | Utdatans filnamn. |
| saveFormat | Aspose::Words::SaveFormat | Sparformatet. |
| watermarkText | const System::String\& | Text som visas som en vattenstämpel. |
| options | const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\& | Definierar ytterligare alternativ för textvattenstämpeln. |
## Anmärkningar


Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas varje sida av utdata som en separat fil. Det angivna utdatafilnamnet kommer att användas för att generera filnamn för varje del enligt regeln: outputFile_partIndex.extension.

Om utdataformatet är TIFF sparas utdata som en enda flerbilds‑TIFF‑fil.

## Se även

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetText(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&) method


Lägger till en textvattenstämpel i dokumentet med alternativ och specificerat sparformat.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetText(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &watermarkText)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputFileName | const System::String\& | Inmatningsfilnamnet. |
| outputFileName | const System::String\& | Utdatans filnamn. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Sparalternativen. |
| watermarkText | const System::String\& | Text som visas som en vattenstämpel. |
## Anmärkningar


Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas varje sida av utdata som en separat fil. Det angivna utdatafilnamnet kommer att användas för att generera filnamn för varje del enligt regeln: outputFile_partIndex.extension.

Om utdataformatet är TIFF sparas utdata som en enda flerbilds‑TIFF‑fil.

## Se även

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetText(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) method


Lägger till en textvattenstämpel i dokumentet med alternativ och specificerat sparformat.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetText(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &watermarkText, const System::SharedPtr<Aspose::Words::TextWatermarkOptions> &options)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputFileName | const System::String\& | Inmatningsfilnamnet. |
| outputFileName | const System::String\& | Utdatans filnamn. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Sparalternativen. |
| watermarkText | const System::String\& | Text som visas som en vattenstämpel. |
| options | const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\& | Definierar ytterligare alternativ för textvattenstämpeln. |
## Anmärkningar


Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas varje sida av utdata som en separat fil. Det angivna utdatafilnamnet kommer att användas för att generera filnamn för varje del enligt regeln: outputFile_partIndex.extension.

Om utdataformatet är TIFF sparas utdata som en enda flerbilds‑TIFF‑fil.

## Se även

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetText(const System::String\&, const System::String\&, const System::String\&) method


Lägger till en textvattenstämpel i dokumentet.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetText(const System::String &inputFileName, const System::String &outputFileName, const System::String &watermarkText)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputFileName | const System::String\& | Inmatningsfilnamnet. |
| outputFileName | const System::String\& | Utdatans filnamn. |
| watermarkText | const System::String\& | Text som visas som en vattenstämpel. |
## Anmärkningar


Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas varje sida av utdata som en separat fil. Det angivna utdatafilnamnet kommer att användas för att generera filnamn för varje del enligt regeln: outputFile_partIndex.extension.

Om utdataformatet är TIFF sparas utdata som en enda flerbilds‑TIFF‑fil.

## Se även

* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetText(const System::String\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) method


Lägger till en textvattenstämpel i dokumentet med alternativ.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetText(const System::String &inputFileName, const System::String &outputFileName, const System::String &watermarkText, const System::SharedPtr<Aspose::Words::TextWatermarkOptions> &options)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputFileName | const System::String\& | Inmatningsfilnamnet. |
| outputFileName | const System::String\& | Utdatans filnamn. |
| watermarkText | const System::String\& | Text som visas som en vattenstämpel. |
| options | const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\& | Definierar ytterligare alternativ för textvattenstämpeln. |
## Anmärkningar


Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas varje sida av utdata som en separat fil. Det angivna utdatafilnamnet kommer att användas för att generera filnamn för varje del enligt regeln: outputFile_partIndex.extension.

Om utdataformatet är TIFF sparas utdata som en enda flerbilds‑TIFF‑fil.

## Se även

* Class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
