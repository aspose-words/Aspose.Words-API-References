---
title: "Aspose::Words::LowCode::Converter::ConvertToImages Methode"
linktitle: "ConvertToImages"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::LowCode::Converter::ConvertToImages Methode. Konvertiert die Seiten des angegebenen Dokuments in Bilder im angegebenen Format und gibt ein Array von Strömen zurück, die die Bilder in C++ enthalten."
type: docs
weight: 2000
url: /de/cpp/aspose.words.lowcode/converter/converttoimages/
---
## Converter::ConvertToImages(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::SaveFormat) method


Konvertiert die Seiten des angegebenen Dokuments in Bilder im angegebenen Format und gibt ein Array von Streams zurück, das die Bilder enthält.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Converter::ConvertToImages(const System::SharedPtr<Aspose::Words::Document> &doc, Aspose::Words::SaveFormat saveFormat)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::Document\>\& | Das Eingabedokument. |
| saveFormat | Aspose::Words::SaveFormat | Speicherformat. Nur Bildspeicherformate sind erlaubt. |

### ReturnValue

Gibt ein Array von Bild-Streams zurück. Die Streams sollten vom Endbenutzer freigegeben werden.

## Siehe auch

* Class [Document](../../../aspose.words/document/)
* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::SharedPtr\<Aspose::Words::Document\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) method


Konvertiert die Seiten des angegebenen Dokuments in Bilder unter Verwendung der angegebenen Speicheroptionen und gibt ein Array von Streams zurück, das die Bilder enthält.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Converter::ConvertToImages(const System::SharedPtr<Aspose::Words::Document> &doc, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::Document\>\& | Das Eingabedokument. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Optionen zum Bildspeichern. |

### ReturnValue

Gibt ein Array von Bild-Streams zurück. Die Streams sollten vom Endbenutzer freigegeben werden.

## Siehe auch

* Class [Document](../../../aspose.words/document/)
* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) method


Konvertiert die Seiten des angegebenen Eingabestreams in Bilder im angegebenen Format und gibt ein Array von Streams zurück, das die Bilder enthält.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Converter::ConvertToImages(const System::SharedPtr<System::IO::Stream> &inputStream, Aspose::Words::SaveFormat saveFormat)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Der Eingabestream. |
| saveFormat | Aspose::Words::SaveFormat | Speicherformat. Nur Bildspeicherformate sind erlaubt. |

### ReturnValue

Gibt ein Array von Bild-Streams zurück. Die Streams sollten vom Endbenutzer freigegeben werden.

## Siehe auch

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) method


Konvertiert die Seiten des angegebenen Eingabestreams in Bilder unter Verwendung der bereitgestellten Lade- und Speicheroptionen und gibt ein Array von Streams zurück, das die Bilder enthält.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Converter::ConvertToImages(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Der Eingabestream. |
| loadOptions | const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\& | Die Ladeoptionen des Eingabedokuments. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Optionen zum Bildspeichern. |

### ReturnValue

Gibt ein Array von Bild-Streams zurück. Die Streams sollten vom Endbenutzer freigegeben werden.

## Siehe auch

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) method


Konvertiert die Seiten des angegebenen Eingabestreams in Bilder unter Verwendung der angegebenen Speicheroptionen und gibt ein Array von Streams zurück, das die Bilder enthält.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Converter::ConvertToImages(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Der Eingabestream. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Optionen zum Bildspeichern. |

### ReturnValue

Gibt ein Array von Bild-Streams zurück. Die Streams sollten vom Endbenutzer freigegeben werden.

## Siehe auch

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::String\&, Aspose::Words::SaveFormat) method


Konvertiert die Seiten der angegebenen Eingabedatei in Bilder im angegebenen Format und gibt ein Array von Streams zurück, das die Bilder enthält.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Converter::ConvertToImages(const System::String &inputFile, Aspose::Words::SaveFormat saveFormat)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFile | const System::String\& | Der Eingabedateiname. |
| saveFormat | Aspose::Words::SaveFormat | Speicherformat. Nur Bildspeicherformate sind erlaubt. |

### ReturnValue

Gibt ein Array von Bild-Streams zurück. Die Streams sollten vom Endbenutzer freigegeben werden.

## Siehe auch

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) method


Konvertiert die Seiten der angegebenen Eingabedatei in Bilddateien unter Verwendung der bereitgestellten Lade- und Speicheroptionen.

```cpp
static void Aspose::Words::LowCode::Converter::ConvertToImages(const System::String &inputFile, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions, const System::String &outputFile, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFile | const System::String\& | Der Eingabedateiname. |
| loadOptions | const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\& | Die Ladeoptionen des Eingabedokuments. |
| outputFile | const System::String\& | Der Ausgabedateiname, der verwendet wird, um Dateinamen für Seitenbilder nach der Regel "outputFile_pageIndex.extension" zu erzeugen. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Optionen zum Bildspeichern. |

## Siehe auch

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) method


Konvertiert die Seiten der angegebenen Eingabedatei in Bilder unter Verwendung der angegebenen Speicheroptionen und gibt ein Array von Streams zurück, das die Bilder enthält.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Converter::ConvertToImages(const System::String &inputFile, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFile | const System::String\& | Der Eingabedateiname. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Optionen zum Bildspeichern. |

### ReturnValue

Gibt ein Array von Bild-Streams zurück. Die Streams sollten vom Endbenutzer freigegeben werden.

## Siehe auch

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::String\&, const System::String\&) method


Konvertiert die Seiten der angegebenen Eingabedatei in Bilddateien.

```cpp
static void Aspose::Words::LowCode::Converter::ConvertToImages(const System::String &inputFile, const System::String &outputFile)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFile | const System::String\& | Der Eingabedateiname. |
| outputFile | const System::String\& | Der Ausgabedateiname, der verwendet wird, um Dateinamen für Seitenbilder nach der Regel "outputFile_pageIndex.extension" zu erzeugen. |

## Siehe auch

* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::String\&, const System::String\&, Aspose::Words::SaveFormat) method


Konvertiert die Seiten der angegebenen Eingabedatei in Bilddateien im angegebenen Format.

```cpp
static void Aspose::Words::LowCode::Converter::ConvertToImages(const System::String &inputFile, const System::String &outputFile, Aspose::Words::SaveFormat saveFormat)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFile | const System::String\& | Der Eingabedateiname. |
| outputFile | const System::String\& | Der Ausgabedateiname, der verwendet wird, um Dateinamen für Seitenbilder nach der Regel "outputFile_pageIndex.extension" zu erzeugen. |
| saveFormat | Aspose::Words::SaveFormat | Speicherformat. Nur Bildspeicherformate sind erlaubt. |

## Siehe auch

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) method


Konvertiert die Seiten der angegebenen Eingabedatei in Bilddateien unter Verwendung der angegebenen Speicheroptionen.

```cpp
static void Aspose::Words::LowCode::Converter::ConvertToImages(const System::String &inputFile, const System::String &outputFile, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFile | const System::String\& | Der Eingabedateiname. |
| outputFile | const System::String\& | Der Ausgabedateiname, der verwendet wird, um Dateinamen für Seitenbilder nach der Regel "outputFile_pageIndex.extension" zu erzeugen. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Optionen zum Bildspeichern. |

## Siehe auch

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
