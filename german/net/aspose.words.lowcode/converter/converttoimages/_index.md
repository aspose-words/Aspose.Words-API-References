---
title: Converter.ConvertToImages
linktitle: ConvertToImages
articleTitle: ConvertToImages
second_title: Aspose.Words für .NET
description: Transformieren Sie Ihre Dokumente mühelos mit ConvertToImages. Konvertieren Sie Seiten schnell und einfach in hochwertige Bilddateien für optimierte Freigabe und Speicherung.
type: docs
weight: 30
url: /de/net/aspose.words.lowcode/converter/converttoimages/
---
## ConvertToImages(*string, [SaveFormat](../../../aspose.words/saveformat/)*) {#converttoimages_5}

Konvertiert die Seiten der angegebenen Eingabedatei in Bilder im angegebenen Format und gibt ein Array von Streams zurück, die die Bilder enthalten.

```csharp
public static Stream[] ConvertToImages(string inputFile, SaveFormat saveFormat)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFile | String | Der Name der Eingabedatei. |
| saveFormat | SaveFormat | Speicherformat. Es sind nur Bildspeicherformate zulässig. |

### Rückgabewert

Gibt ein Array von Bildströmen zurück. Die Ströme sollten vom Endbenutzer entsorgt werden.

## Beispiele

Zeigt, wie ein Dokument in einen Bildstream konvertiert wird.

```csharp
string doc = MyDir + "Big document.docx";

Stream[] streams = Converter.ConvertToImages(doc, SaveFormat.Png);

ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.PageSet = new PageSet(1);
streams = Converter.ConvertToImages(doc, imageSaveOptions);

streams = Converter.ConvertToImages(new Document(doc), SaveFormat.Png);

streams = Converter.ConvertToImages(new Document(doc), imageSaveOptions);
```

### Siehe auch

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Converter](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## ConvertToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)*) {#converttoimages_6}

Konvertiert die Seiten der angegebenen Eingabedatei unter Verwendung der angegebenen Speicheroptionen in Bilder und gibt ein Array von Streams zurück, die die Bilder enthalten.

```csharp
public static Stream[] ConvertToImages(string inputFile, ImageSaveOptions saveOptions)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFile | String | Der Name der Eingabedatei. |
| saveOptions | ImageSaveOptions | Optionen zum Speichern von Bildern. |

### Rückgabewert

Gibt ein Array von Bildströmen zurück. Die Ströme sollten vom Endbenutzer entsorgt werden.

## Beispiele

Zeigt, wie ein Dokument in einen Bildstream konvertiert wird.

```csharp
string doc = MyDir + "Big document.docx";

Stream[] streams = Converter.ConvertToImages(doc, SaveFormat.Png);

ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.PageSet = new PageSet(1);
streams = Converter.ConvertToImages(doc, imageSaveOptions);

streams = Converter.ConvertToImages(new Document(doc), SaveFormat.Png);

streams = Converter.ConvertToImages(new Document(doc), imageSaveOptions);
```

### Siehe auch

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [Converter](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## ConvertToImages(*Stream, [SaveFormat](../../../aspose.words/saveformat/)*) {#converttoimages_3}

Konvertiert die Seiten des angegebenen Eingabestreams in Bilder im angegebenen Format und gibt ein Array von Streams zurück, die die Bilder enthalten.

```csharp
public static Stream[] ConvertToImages(Stream inputStream, SaveFormat saveFormat)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | Stream | Der Eingabestream. |
| saveFormat | SaveFormat | Speicherformat. Es sind nur Bildspeicherformate zulässig. |

### Rückgabewert

Gibt ein Array von Bildströmen zurück. Die Ströme sollten vom Endbenutzer entsorgt werden.

## Beispiele

Zeigt, wie Dokumente aus einem Stream in Bilder konvertiert werden.

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    Stream[] streams = Converter.ConvertToImages(streamIn, SaveFormat.Jpeg);

    ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
    imageSaveOptions.PageSet = new PageSet(1);
    streams = Converter.ConvertToImages(streamIn, imageSaveOptions);

    LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = false };
    Converter.ConvertToImages(streamIn, loadOptions, imageSaveOptions);
}
```

### Siehe auch

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Converter](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## ConvertToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)*) {#converttoimages_4}

Konvertiert die Seiten des angegebenen Eingabestreams unter Verwendung der angegebenen Speicheroptionen in Bilder und gibt ein Array von Streams zurück, die die Bilder enthalten.

```csharp
public static Stream[] ConvertToImages(Stream inputStream, ImageSaveOptions saveOptions)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | Stream | Der Eingabestream. |
| saveOptions | ImageSaveOptions | Optionen zum Speichern von Bildern. |

### Rückgabewert

Gibt ein Array von Bildströmen zurück. Die Ströme sollten vom Endbenutzer entsorgt werden.

## Beispiele

Zeigt, wie Dokumente aus einem Stream in Bilder konvertiert werden.

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    Stream[] streams = Converter.ConvertToImages(streamIn, SaveFormat.Jpeg);

    ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
    imageSaveOptions.PageSet = new PageSet(1);
    streams = Converter.ConvertToImages(streamIn, imageSaveOptions);

    LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = false };
    Converter.ConvertToImages(streamIn, loadOptions, imageSaveOptions);
}
```

### Siehe auch

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [Converter](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## ConvertToImages(*Stream, [LoadOptions](../../../aspose.words.loading/loadoptions/), [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)*) {#converttoimages_2}

Konvertiert die Seiten des angegebenen Eingabestreams mithilfe der bereitgestellten Lade- und Speicheroptionen in Bilder und gibt ein Array von Streams zurück, die die Bilder enthalten.

```csharp
public static Stream[] ConvertToImages(Stream inputStream, LoadOptions loadOptions, 
    ImageSaveOptions saveOptions)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | Stream | Der Eingabestream. |
| loadOptions | LoadOptions | Die Ladeoptionen für das Eingabedokument. |
| saveOptions | ImageSaveOptions | Optionen zum Speichern von Bildern. |

### Rückgabewert

Gibt ein Array von Bildströmen zurück. Die Ströme sollten vom Endbenutzer entsorgt werden.

## Beispiele

Zeigt, wie Dokumente aus einem Stream in Bilder konvertiert werden.

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    Stream[] streams = Converter.ConvertToImages(streamIn, SaveFormat.Jpeg);

    ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
    imageSaveOptions.PageSet = new PageSet(1);
    streams = Converter.ConvertToImages(streamIn, imageSaveOptions);

    LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = false };
    Converter.ConvertToImages(streamIn, loadOptions, imageSaveOptions);
}
```

### Siehe auch

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [Converter](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## ConvertToImages(*[Document](../../../aspose.words/document/), [SaveFormat](../../../aspose.words/saveformat/)*) {#converttoimages}

Konvertiert die Seiten des angegebenen Dokuments in Bilder im angegebenen Format und gibt ein Array von Streams zurück, die die Bilder enthalten.

```csharp
public static Stream[] ConvertToImages(Document doc, SaveFormat saveFormat)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| doc | Document | Das Eingabedokument. |
| saveFormat | SaveFormat | Speicherformat. Es sind nur Bildspeicherformate zulässig. |

### Rückgabewert

Gibt ein Array von Bildströmen zurück. Die Ströme sollten vom Endbenutzer entsorgt werden.

## Beispiele

Zeigt, wie ein Dokument in einen Bildstream konvertiert wird.

```csharp
string doc = MyDir + "Big document.docx";

Stream[] streams = Converter.ConvertToImages(doc, SaveFormat.Png);

ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.PageSet = new PageSet(1);
streams = Converter.ConvertToImages(doc, imageSaveOptions);

streams = Converter.ConvertToImages(new Document(doc), SaveFormat.Png);

streams = Converter.ConvertToImages(new Document(doc), imageSaveOptions);
```

### Siehe auch

* class [Document](../../../aspose.words/document/)
* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Converter](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## ConvertToImages(*[Document](../../../aspose.words/document/), [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)*) {#converttoimages_1}

Konvertiert die Seiten des angegebenen Dokuments unter Verwendung der angegebenen Speicheroptionen in Bilder und gibt ein Array von Streams zurück, die die Bilder enthalten.

```csharp
public static Stream[] ConvertToImages(Document doc, ImageSaveOptions saveOptions)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| doc | Document | Das Eingabedokument. |
| saveOptions | ImageSaveOptions | Optionen zum Speichern von Bildern. |

### Rückgabewert

Gibt ein Array von Bildströmen zurück. Die Ströme sollten vom Endbenutzer entsorgt werden.

## Beispiele

Zeigt, wie ein Dokument in einen Bildstream konvertiert wird.

```csharp
string doc = MyDir + "Big document.docx";

Stream[] streams = Converter.ConvertToImages(doc, SaveFormat.Png);

ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.PageSet = new PageSet(1);
streams = Converter.ConvertToImages(doc, imageSaveOptions);

streams = Converter.ConvertToImages(new Document(doc), SaveFormat.Png);

streams = Converter.ConvertToImages(new Document(doc), imageSaveOptions);
```

### Siehe auch

* class [Document](../../../aspose.words/document/)
* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [Converter](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)
