---
title: "Aspose::Words::LowCode::Replacer::Replace‑metod"
linktitle: "Ersätt"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::LowCode::Replacer::Replace‑metod. Ersätter alla förekomster av ett angivet teckensträngsmönster med en ersättningssträng i indataströmmen med hjälp av ett reguljärt uttryck, med det angivna sparformatet och ytterligare alternativ i C++."
type: docs
weight: 1000
url: /sv/cpp/aspose.words.lowcode/replacer/replace/
---
## Replacer::Replace(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) method


Ersätter alla förekomster av ett angivet teckensträngsmönster med en ersättningssträng i indataströmmen med hjälp av ett reguljärt uttryck, med det angivna sparformatet och ytterligare alternativ.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Inmatningsströmmen. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Utdataflödet. |
| saveFormat | Aspose::Words::SaveFormat | Sparformatet. |
| mönster | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Ett reguljärt uttrycksmönster som används för att hitta matchningar. |
| ersättning | const System::String\& | En sträng för att ersätta alla förekomster av mönster. |

### ReturnValue

Antalet utförda ersättningar.
## Anmärkningar


Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas endast den första sidan av utdata till den angivna strömmen.

Om utdataformatet är TIFF sparas utdata som en enda flerbilds‑TIFF till den angivna strömmen.

## Se även

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Ersätter alla förekomster av ett angivet teckensträngsmönster med en ersättningssträng i indataströmmen med hjälp av ett reguljärt uttryck, med det angivna sparformatet och ytterligare alternativ.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Inmatningsströmmen. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Utdataflödet. |
| saveFormat | Aspose::Words::SaveFormat | Sparformatet. |
| mönster | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Ett reguljärt uttrycksmönster som används för att hitta matchningar. |
| ersättning | const System::String\& | En sträng för att ersätta alla förekomster av mönster. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) objekt för att specificera ytterligare alternativ. |

### ReturnValue

Antalet utförda ersättningar.
## Anmärkningar


Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas endast den första sidan av utdata till den angivna strömmen.

Om utdataformatet är TIFF sparas utdata som en enda flerbilds‑TIFF till den angivna strömmen.

## Se även

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, const System::String\&) method


Ersätter alla förekomster av ett angivet teckensträngsmönster med en ersättningssträng i indataströmmen, med det angivna sparformatet och ytterligare alternativ.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::String &pattern, const System::String &replacement)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Inmatningsströmmen. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Utdataflödet. |
| saveFormat | Aspose::Words::SaveFormat | Sparformatet. |
| mönster | const System::String\& | En sträng som ska ersättas. |
| ersättning | const System::String\& | En sträng för att ersätta alla förekomster av mönster. |

### ReturnValue

Antalet utförda ersättningar.
## Anmärkningar


Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas endast den första sidan av utdata till den angivna strömmen.

Om utdataformatet är TIFF sparas utdata som en enda flerbilds‑TIFF till den angivna strömmen.

## Se även

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Ersätter alla förekomster av ett angivet teckensträngsmönster med en ersättningssträng i indataströmmen, med det angivna sparformatet och ytterligare alternativ.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::String &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Inmatningsströmmen. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Utdataflödet. |
| saveFormat | Aspose::Words::SaveFormat | Sparformatet. |
| mönster | const System::String\& | En sträng som ska ersättas. |
| ersättning | const System::String\& | En sträng för att ersätta alla förekomster av mönster. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) objekt för att specificera ytterligare alternativ. |

### ReturnValue

Antalet utförda ersättningar.
## Anmärkningar


Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas endast den första sidan av utdata till den angivna strömmen.

Om utdataformatet är TIFF sparas utdata som en enda flerbilds‑TIFF till den angivna strömmen.

## Se även

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) method


Ersätter alla förekomster av ett angivet teckensträngsmönster med en ersättningssträng i indataströmmen med hjälp av ett reguljärt uttryck, med det angivna sparformatet och ytterligare alternativ.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Inmatningsströmmen. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Utdataflödet. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Sparalternativen. |
| mönster | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Ett reguljärt uttrycksmönster som används för att hitta matchningar. |
| ersättning | const System::String\& | En sträng för att ersätta alla förekomster av mönster. |

### ReturnValue

Antalet utförda ersättningar.
## Anmärkningar


Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas endast den första sidan av utdata till den angivna strömmen.

Om utdataformatet är TIFF sparas utdata som en enda flerbilds‑TIFF till den angivna strömmen.

## Se även

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Ersätter alla förekomster av ett angivet teckensträngsmönster med en ersättningssträng i indataströmmen med hjälp av ett reguljärt uttryck, med det angivna sparformatet och ytterligare alternativ.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Inmatningsströmmen. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Utdataflödet. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Sparalternativen. |
| mönster | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Ett reguljärt uttrycksmönster som används för att hitta matchningar. |
| ersättning | const System::String\& | En sträng för att ersätta alla förekomster av mönster. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) objekt för att specificera ytterligare alternativ. |

### ReturnValue

Antalet utförda ersättningar.
## Anmärkningar


Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas endast den första sidan av utdata till den angivna strömmen.

Om utdataformatet är TIFF sparas utdata som en enda flerbilds‑TIFF till den angivna strömmen.

## Se även

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::String\&) method


Ersätter alla förekomster av ett angivet teckensträngsmönster med en ersättningssträng i indataströmmen, med det angivna sparformatet och ytterligare alternativ.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &pattern, const System::String &replacement)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Inmatningsströmmen. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Utdataflödet. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Sparalternativen. |
| mönster | const System::String\& | En sträng som ska ersättas. |
| ersättning | const System::String\& | En sträng för att ersätta alla förekomster av mönster. |

### ReturnValue

Antalet utförda ersättningar.
## Anmärkningar


Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas endast den första sidan av utdata till den angivna strömmen.

Om utdataformatet är TIFF sparas utdata som en enda flerbilds‑TIFF till den angivna strömmen.

## Se även

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Ersätter alla förekomster av ett angivet teckensträngsmönster med en ersättningssträng i indataströmmen, med det angivna sparformatet och ytterligare alternativ.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Inmatningsströmmen. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Utdataflödet. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Sparalternativen. |
| mönster | const System::String\& | En sträng som ska ersättas. |
| ersättning | const System::String\& | En sträng för att ersätta alla förekomster av mönster. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) objekt för att specificera ytterligare alternativ. |

### ReturnValue

Antalet utförda ersättningar.
## Anmärkningar


Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas endast den första sidan av utdata till den angivna strömmen.

Om utdataformatet är TIFF sparas utdata som en enda flerbilds‑TIFF till den angivna strömmen.

## Se även

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) method


Ersätter alla förekomster av ett angivet teckensträngsmönster med en ersättningssträng i indatafilen med hjälp av ett reguljärt uttryck, med det angivna sparformatet och ytterligare alternativ.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputFileName | const System::String\& | Inmatningsfilnamnet. |
| outputFileName | const System::String\& | Utdatans filnamn. |
| saveFormat | Aspose::Words::SaveFormat | Sparformatet. |
| mönster | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Ett reguljärt uttrycksmönster som används för att hitta matchningar. |
| ersättning | const System::String\& | En sträng för att ersätta alla förekomster av mönster. |

### ReturnValue

Antalet utförda ersättningar.
## Anmärkningar


Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas varje sida av utdata som en separat fil. Det angivna utdatafilnamnet kommer att användas för att generera filnamn för varje del enligt regeln: outputFile_partIndex.extension.

Om utdataformatet är TIFF sparas utdata som en enda flerbilds‑TIFF‑fil.

## Se även

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Ersätter alla förekomster av ett angivet teckensträngsmönster med en ersättningssträng i indatafilen med hjälp av ett reguljärt uttryck, med det angivna sparformatet och ytterligare alternativ.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputFileName | const System::String\& | Inmatningsfilnamnet. |
| outputFileName | const System::String\& | Utdatans filnamn. |
| saveFormat | Aspose::Words::SaveFormat | Sparformatet. |
| mönster | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Ett reguljärt uttrycksmönster som används för att hitta matchningar. |
| ersättning | const System::String\& | En sträng för att ersätta alla förekomster av mönster. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) objekt för att specificera ytterligare alternativ. |

### ReturnValue

Antalet utförda ersättningar.
## Anmärkningar


Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas varje sida av utdata som en separat fil. Det angivna utdatafilnamnet kommer att användas för att generera filnamn för varje del enligt regeln: outputFile_partIndex.extension.

Om utdataformatet är TIFF sparas utdata som en enda flerbilds‑TIFF‑fil.

## Se även

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, const System::String\&) method


Ersätter alla förekomster av ett angivet teckensträngsmönster med en ersättningssträng i indatafilen, med det angivna sparformatet och ytterligare alternativ.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::String &pattern, const System::String &replacement)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputFileName | const System::String\& | Inmatningsfilnamnet. |
| outputFileName | const System::String\& | Utdatans filnamn. |
| saveFormat | Aspose::Words::SaveFormat | Sparformatet. |
| mönster | const System::String\& | En sträng som ska ersättas. |
| ersättning | const System::String\& | En sträng för att ersätta alla förekomster av mönster. |

### ReturnValue

Antalet utförda ersättningar.
## Anmärkningar


Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas varje sida av utdata som en separat fil. Det angivna utdatafilnamnet kommer att användas för att generera filnamn för varje del enligt regeln: outputFile_partIndex.extension.

Om utdataformatet är TIFF sparas utdata som en enda flerbilds‑TIFF‑fil.

## Se även

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Ersätter alla förekomster av ett angivet teckensträngsmönster med en ersättningssträng i indatafilen, med det angivna sparformatet och ytterligare alternativ.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::String &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputFileName | const System::String\& | Inmatningsfilnamnet. |
| outputFileName | const System::String\& | Utdatans filnamn. |
| saveFormat | Aspose::Words::SaveFormat | Sparformatet. |
| mönster | const System::String\& | En sträng som ska ersättas. |
| ersättning | const System::String\& | En sträng för att ersätta alla förekomster av mönster. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) objekt för att specificera ytterligare alternativ. |

### ReturnValue

Antalet utförda ersättningar.
## Anmärkningar


Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas varje sida av utdata som en separat fil. Det angivna utdatafilnamnet kommer att användas för att generera filnamn för varje del enligt regeln: outputFile_partIndex.extension.

Om utdataformatet är TIFF sparas utdata som en enda flerbilds‑TIFF‑fil.

## Se även

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) method


Ersätter alla förekomster av ett angivet teckensträngsmönster med en ersättningssträng i indatafilen med hjälp av ett reguljärt uttryck, med det angivna sparformatet och ytterligare alternativ.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputFileName | const System::String\& | Inmatningsfilnamnet. |
| outputFileName | const System::String\& | Utdatans filnamn. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Sparalternativen. |
| mönster | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Ett reguljärt uttrycksmönster som används för att hitta matchningar. |
| ersättning | const System::String\& | En sträng för att ersätta alla förekomster av mönster. |

### ReturnValue

Antalet utförda ersättningar.
## Anmärkningar


Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas varje sida av utdata som en separat fil. Det angivna utdatafilnamnet kommer att användas för att generera filnamn för varje del enligt regeln: outputFile_partIndex.extension.

Om utdataformatet är TIFF sparas utdata som en enda flerbilds‑TIFF‑fil.

## Se även

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Ersätter alla förekomster av ett angivet teckensträngsmönster med en ersättningssträng i indatafilen med hjälp av ett reguljärt uttryck, med det angivna sparformatet och ytterligare alternativ.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputFileName | const System::String\& | Inmatningsfilnamnet. |
| outputFileName | const System::String\& | Utdatans filnamn. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Sparalternativen. |
| mönster | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Ett reguljärt uttrycksmönster som används för att hitta matchningar. |
| ersättning | const System::String\& | En sträng för att ersätta alla förekomster av mönster. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) objekt för att specificera ytterligare alternativ. |

### ReturnValue

Antalet utförda ersättningar.
## Anmärkningar


Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas varje sida av utdata som en separat fil. Det angivna utdatafilnamnet kommer att användas för att generera filnamn för varje del enligt regeln: outputFile_partIndex.extension.

Om utdataformatet är TIFF sparas utdata som en enda flerbilds‑TIFF‑fil.

## Se även

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::String\&) method


Ersätter alla förekomster av ett angivet teckensträngsmönster med en ersättningssträng i indatafilen, med det angivna sparformatet och ytterligare alternativ.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &pattern, const System::String &replacement)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputFileName | const System::String\& | Inmatningsfilnamnet. |
| outputFileName | const System::String\& | Utdatans filnamn. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Sparalternativen. |
| mönster | const System::String\& | En sträng som ska ersättas. |
| ersättning | const System::String\& | En sträng för att ersätta alla förekomster av mönster. |

### ReturnValue

Antalet utförda ersättningar.
## Anmärkningar


Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas varje sida av utdata som en separat fil. Det angivna utdatafilnamnet kommer att användas för att generera filnamn för varje del enligt regeln: outputFile_partIndex.extension.

Om utdataformatet är TIFF sparas utdata som en enda flerbilds‑TIFF‑fil.

## Se även

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Ersätter alla förekomster av ett angivet teckensträngsmönster med en ersättningssträng i indatafilen, med det angivna sparformatet och ytterligare alternativ.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputFileName | const System::String\& | Inmatningsfilnamnet. |
| outputFileName | const System::String\& | Utdatans filnamn. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Sparalternativen. |
| mönster | const System::String\& | En sträng som ska ersättas. |
| ersättning | const System::String\& | En sträng för att ersätta alla förekomster av mönster. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) objekt för att specificera ytterligare alternativ. |

### ReturnValue

Antalet utförda ersättningar.
## Anmärkningar


Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas varje sida av utdata som en separat fil. Det angivna utdatafilnamnet kommer att användas för att generera filnamn för varje del enligt regeln: outputFile_partIndex.extension.

Om utdataformatet är TIFF sparas utdata som en enda flerbilds‑TIFF‑fil.

## Se även

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) method


Ersätter alla förekomster av ett angivet teckensträngsmönster med en ersättningssträng i indatafilen med hjälp av ett reguljärt uttryck.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputFileName | const System::String\& | Inmatningsfilnamnet. |
| outputFileName | const System::String\& | Utdatans filnamn. |
| mönster | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Ett reguljärt uttrycksmönster som används för att hitta matchningar. |
| ersättning | const System::String\& | En sträng för att ersätta alla förekomster av mönster. |

### ReturnValue

Antalet utförda ersättningar.
## Anmärkningar


Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas varje sida av utdata som en separat fil. Det angivna utdatafilnamnet kommer att användas för att generera filnamn för varje del enligt regeln: outputFile_partIndex.extension.

Om utdataformatet är TIFF sparas utdata som en enda flerbilds‑TIFF‑fil.

## Se även

* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, const System::String\&, const System::String\&) method


Ersätter alla förekomster av ett angivet teckensträngsmönster med en ersättningssträng i indatafilen.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, const System::String &pattern, const System::String &replacement)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputFileName | const System::String\& | Inmatningsfilnamnet. |
| outputFileName | const System::String\& | Utdatans filnamn. |
| mönster | const System::String\& | En sträng som ska ersättas. |
| ersättning | const System::String\& | En sträng för att ersätta alla förekomster av mönster. |

### ReturnValue

Antalet utförda ersättningar.
## Anmärkningar


Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas varje sida av utdata som en separat fil. Det angivna utdatafilnamnet kommer att användas för att generera filnamn för varje del enligt regeln: outputFile_partIndex.extension.

Om utdataformatet är TIFF sparas utdata som en enda flerbilds‑TIFF‑fil.

## Se även

* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
