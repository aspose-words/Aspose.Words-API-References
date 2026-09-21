---
title: "Aspose::Words::LowCode::Comparer::Compare metod"
linktitle: "Jämför"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::LowCode::Comparer::Compare metod. Jämför två dokument som lästs in från strömmar med ytterligare alternativ och sparar skillnaderna till den angivna utdataströmmen i det specificerade sparformatet, vilket producerar förändringar som ett antal redigerings- och formatrevisioner i C++."
type: docs
weight: 1000
url: /sv/cpp/aspose.words.lowcode/comparer/compare/
---
## Comparer::Compare(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime) method


Jämför två dokument som lästs in från strömmar med ytterligare alternativ och sparar skillnaderna till den angivna utdataströmmen i det specificerade sparformatet, vilket skapar förändringar som ett antal redigerings- och formatrevisioner.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::SharedPtr<System::IO::Stream> &v1, const System::SharedPtr<System::IO::Stream> &v2, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::String &author, System::DateTime dateTime)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| v1 | const System::SharedPtr\<System::IO::Stream\>\& | Det ursprungliga dokumentet. |
| v2 | const System::SharedPtr\<System::IO::Stream\>\& | Det modifierade dokumentet. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Utdataflödet. |
| saveFormat | Aspose::Words::SaveFormat | Sparformatet för utdata. |
| författare | const System::String\& | Initialer för författaren att använda för revisioner. |
| dateTime | System::DateTime | Datumet och tiden att använda för revisioner. |
## Anmärkningar


Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas endast den första sidan av utdata till den angivna strömmen.

Om utdataformatet är TIFF sparas utdata som en enda flerbilds‑TIFF till den angivna strömmen.

## Se även

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) method


Jämför två dokument som lästs in från strömmar med ytterligare alternativ och sparar skillnaderna till den angivna utdataströmmen i det specificerade sparformatet, vilket skapar förändringar som ett antal redigerings- och formatrevisioner.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::SharedPtr<System::IO::Stream> &v1, const System::SharedPtr<System::IO::Stream> &v2, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::String &author, System::DateTime dateTime, const System::SharedPtr<Aspose::Words::Comparing::CompareOptions> &compareOptions)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| v1 | const System::SharedPtr\<System::IO::Stream\>\& | Det ursprungliga dokumentet. |
| v2 | const System::SharedPtr\<System::IO::Stream\>\& | Det modifierade dokumentet. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Utdataflödet. |
| saveFormat | Aspose::Words::SaveFormat | Sparformatet för utdata. |
| författare | const System::String\& | Initialer för författaren att använda för revisioner. |
| dateTime | System::DateTime | Datumet och tiden att använda för revisioner. |
| compareOptions | const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\& | [Document](../../../aspose.words/document/) jämförelsealternativ. |
## Anmärkningar


Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas endast den första sidan av utdata till den angivna strömmen.

Om utdataformatet är TIFF sparas utdata som en enda flerbilds‑TIFF till den angivna strömmen.

## Se även

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime) method


Jämför två dokument som lästs in från strömmar med ytterligare alternativ och sparar skillnaderna till den angivna utdataströmmen i det specificerade sparformatet, vilket skapar förändringar som ett antal redigerings- och formatrevisioner.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::SharedPtr<System::IO::Stream> &v1, const System::SharedPtr<System::IO::Stream> &v2, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &author, System::DateTime dateTime)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| v1 | const System::SharedPtr\<System::IO::Stream\>\& | Det ursprungliga dokumentet. |
| v2 | const System::SharedPtr\<System::IO::Stream\>\& | Det modifierade dokumentet. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Utdataflödet. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Sparalternativen för utdata. |
| författare | const System::String\& | Initialer för författaren att använda för revisioner. |
| dateTime | System::DateTime | Datumet och tiden att använda för revisioner. |
## Anmärkningar


Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas endast den första sidan av utdata till den angivna strömmen.

Om utdataformatet är TIFF sparas utdata som en enda flerbilds‑TIFF till den angivna strömmen.

## Se även

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) method


Jämför två dokument som lästs in från strömmar med ytterligare alternativ och sparar skillnaderna till den angivna utdataströmmen i det specificerade sparformatet, vilket skapar förändringar som ett antal redigerings- och formatrevisioner.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::SharedPtr<System::IO::Stream> &v1, const System::SharedPtr<System::IO::Stream> &v2, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &author, System::DateTime dateTime, const System::SharedPtr<Aspose::Words::Comparing::CompareOptions> &compareOptions)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| v1 | const System::SharedPtr\<System::IO::Stream\>\& | Det ursprungliga dokumentet. |
| v2 | const System::SharedPtr\<System::IO::Stream\>\& | Det modifierade dokumentet. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Utdataflödet. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Sparalternativen för utdata. |
| författare | const System::String\& | Initialer för författaren att använda för revisioner. |
| dateTime | System::DateTime | Datumet och tiden att använda för revisioner. |
| compareOptions | const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\& | [Document](../../../aspose.words/document/) jämförelsealternativ. |
## Anmärkningar


Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas endast den första sidan av utdata till den angivna strömmen.

Om utdataformatet är TIFF sparas utdata som en enda flerbilds‑TIFF till den angivna strömmen.

## Se även

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::String\&, const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime) method


Jämför två dokument med ytterligare alternativ och sparar skillnaderna till den angivna utdatafilen i det angivna sparformatet, vilket skapar förändringar som ett antal redigerings- och formatrevisioner.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::String &v1, const System::String &v2, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::String &author, System::DateTime dateTime)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| v1 | const System::String\& | Det ursprungliga dokumentet. |
| v2 | const System::String\& | Det modifierade dokumentet. |
| outputFileName | const System::String\& | Utdatans filnamn. |
| saveFormat | Aspose::Words::SaveFormat | Sparformatet för utdata. |
| författare | const System::String\& | Initialer för författaren att använda för revisioner. |
| dateTime | System::DateTime | Datumet och tiden att använda för revisioner. |
## Anmärkningar


Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas varje sida av utdata som en separat fil. Det angivna utdatafilnamnet kommer att användas för att generera filnamn för varje del enligt regeln: outputFile_partIndex.extension.

Om utdataformatet är TIFF sparas utdata som en enda flerbilds‑TIFF‑fil.

## Se även

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::String\&, const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) method


Jämför två dokument med ytterligare alternativ och sparar skillnaderna till den angivna utdatafilen i det angivna sparformatet, vilket skapar förändringar som ett antal redigerings- och formatrevisioner.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::String &v1, const System::String &v2, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::String &author, System::DateTime dateTime, const System::SharedPtr<Aspose::Words::Comparing::CompareOptions> &compareOptions)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| v1 | const System::String\& | Det ursprungliga dokumentet. |
| v2 | const System::String\& | Det modifierade dokumentet. |
| outputFileName | const System::String\& | Utdatans filnamn. |
| saveFormat | Aspose::Words::SaveFormat | Sparformatet för utdata. |
| författare | const System::String\& | Initialer för författaren att använda för revisioner. |
| dateTime | System::DateTime | Datumet och tiden att använda för revisioner. |
| compareOptions | const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\& | [Document](../../../aspose.words/document/) jämförelsealternativ. |
## Anmärkningar


Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas varje sida av utdata som en separat fil. Det angivna utdatafilnamnet kommer att användas för att generera filnamn för varje del enligt regeln: outputFile_partIndex.extension.

Om utdataformatet är TIFF sparas utdata som en enda flerbilds‑TIFF‑fil.

## Se även

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::String\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime) method


Jämför två dokument med ytterligare alternativ och sparar skillnaderna till den angivna utdatafilen i det angivna sparformatet, vilket skapar förändringar som ett antal redigerings- och formatrevisioner.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::String &v1, const System::String &v2, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &author, System::DateTime dateTime)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| v1 | const System::String\& | Det ursprungliga dokumentet. |
| v2 | const System::String\& | Det modifierade dokumentet. |
| outputFileName | const System::String\& | Utdatans filnamn. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Sparalternativen för utdata. |
| författare | const System::String\& | Initialer för författaren att använda för revisioner. |
| dateTime | System::DateTime | Datumet och tiden att använda för revisioner. |
## Anmärkningar


Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas varje sida av utdata som en separat fil. Det angivna utdatafilnamnet kommer att användas för att generera filnamn för varje del enligt regeln: outputFile_partIndex.extension.

Om utdataformatet är TIFF sparas utdata som en enda flerbilds‑TIFF‑fil.

## Se även

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::String\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) method


Jämför två dokument med ytterligare alternativ och sparar skillnaderna till den angivna utdatafilen i det angivna sparformatet, vilket skapar förändringar som ett antal redigerings- och formatrevisioner.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::String &v1, const System::String &v2, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &author, System::DateTime dateTime, const System::SharedPtr<Aspose::Words::Comparing::CompareOptions> &compareOptions)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| v1 | const System::String\& | Det ursprungliga dokumentet. |
| v2 | const System::String\& | Det modifierade dokumentet. |
| outputFileName | const System::String\& | Utdatans filnamn. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Sparalternativen för utdata. |
| författare | const System::String\& | Initialer för författaren att använda för revisioner. |
| dateTime | System::DateTime | Datumet och tiden att använda för revisioner. |
| compareOptions | const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\& | [Document](../../../aspose.words/document/) jämförelsealternativ. |
## Anmärkningar


Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas varje sida av utdata som en separat fil. Det angivna utdatafilnamnet kommer att användas för att generera filnamn för varje del enligt regeln: outputFile_partIndex.extension.

Om utdataformatet är TIFF sparas utdata som en enda flerbilds‑TIFF‑fil.

## Se även

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::String\&, const System::String\&, const System::String\&, const System::String\&, System::DateTime) method


Jämför två dokument med ytterligare alternativ och sparar skillnaderna till den angivna utdatafilen, vilket skapar förändringar som ett antal redigerings- och formatrevisioner.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::String &v1, const System::String &v2, const System::String &outputFileName, const System::String &author, System::DateTime dateTime)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| v1 | const System::String\& | Det ursprungliga dokumentet. |
| v2 | const System::String\& | Det modifierade dokumentet. |
| outputFileName | const System::String\& | Utdatans filnamn. |
| författare | const System::String\& | Initialer för författaren att använda för revisioner. |
| dateTime | System::DateTime | Datumet och tiden att använda för revisioner. |
## Anmärkningar


Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas varje sida av utdata som en separat fil. Det angivna utdatafilnamnet kommer att användas för att generera filnamn för varje del enligt regeln: outputFile_partIndex.extension.

Om utdataformatet är TIFF sparas utdata som en enda flerbilds‑TIFF‑fil.

## Se även

* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::String\&, const System::String\&, const System::String\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) method


Jämför två dokument med ytterligare alternativ och sparar skillnaderna till den angivna utdatafilen, vilket skapar förändringar som ett antal redigerings- och formatrevisioner.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::String &v1, const System::String &v2, const System::String &outputFileName, const System::String &author, System::DateTime dateTime, const System::SharedPtr<Aspose::Words::Comparing::CompareOptions> &compareOptions)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| v1 | const System::String\& | Det ursprungliga dokumentet. |
| v2 | const System::String\& | Det modifierade dokumentet. |
| outputFileName | const System::String\& | Utdatans filnamn. |
| författare | const System::String\& | Initialer för författaren att använda för revisioner. |
| dateTime | System::DateTime | Datumet och tiden att använda för revisioner. |
| compareOptions | const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\& | [Document](../../../aspose.words/document/) jämförelsealternativ. |
## Anmärkningar


Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas varje sida av utdata som en separat fil. Det angivna utdatafilnamnet kommer att användas för att generera filnamn för varje del enligt regeln: outputFile_partIndex.extension.

Om utdataformatet är TIFF sparas utdata som en enda flerbilds‑TIFF‑fil.

## Se även

* Class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
