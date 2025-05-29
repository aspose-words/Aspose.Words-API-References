---
title: Watermarker.SetImage
linktitle: SetImage
articleTitle: SetImage
second_title: Aspose.Words für .NET
description: Optimieren Sie Ihre Dokumente mit der Watermarker SetImage-Methode. Fügen Sie mühelos benutzerdefinierte Bildwasserzeichen für einen professionellen Touch hinzu.
type: docs
weight: 20
url: /de/net/aspose.words.lowcode/watermarker/setimage/
---
## SetImage(*string, string, string*) {#setimage_6}

Fügt dem Dokument ein Bildwasserzeichen hinzu.

```csharp
public static void SetImage(string inputFileName, string outputFileName, 
    string watermarkImageFileName)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | String | Der Name der Eingabedatei. |
| outputFileName | String | Der Name der Ausgabedatei. |
| watermarkImageFileName | String | Bild, das als Wasserzeichen angezeigt wird. |

## Bemerkungen

Wenn das Ausgabeformat ein Bild (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP) ist, wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jedes Teil nach der Regel „outputFile_partIndex.extension“ zu generieren.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelne TIFF-Datei mit mehreren Frames gespeichert.

## Beispiele

Zeigt, wie ein Wasserzeichenbild in das Dokument eingefügt wird.

```csharp
string doc = MyDir + "Document.docx";
string watermarkImage = ImageDir + "Logo.jpg";

Watermarker.SetImage(doc, ArtifactsDir + "LowCode.SetWatermarkImage.1.docx", watermarkImage);
Watermarker.SetImage(doc, ArtifactsDir + "LowCode.SetWatermarkText.2.docx", SaveFormat.Docx, watermarkImage);

ImageWatermarkOptions options = new ImageWatermarkOptions();
options.Scale = 50;
Watermarker.SetImage(doc, ArtifactsDir + "LowCode.SetWatermarkText.3.docx", watermarkImage, options);
Watermarker.SetImage(doc, ArtifactsDir + "LowCode.SetWatermarkText.4.docx", SaveFormat.Docx, watermarkImage, options);
```

### Siehe auch

* class [Watermarker](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## SetImage(*string, string, string, [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)*) {#setimage_7}

Fügt dem Dokument mit Optionen ein Bildwasserzeichen hinzu.

```csharp
public static void SetImage(string inputFileName, string outputFileName, 
    string watermarkImageFileName, ImageWatermarkOptions options)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | String | Der Name der Eingabedatei. |
| outputFileName | String | Der Name der Ausgabedatei. |
| watermarkImageFileName | String | Bild, das als Wasserzeichen angezeigt wird. |
| options | ImageWatermarkOptions | Definiert zusätzliche Optionen für das Bildwasserzeichen. |

## Bemerkungen

Wenn das Ausgabeformat ein Bild (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP) ist, wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jedes Teil nach der Regel „outputFile_partIndex.extension“ zu generieren.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelne TIFF-Datei mit mehreren Frames gespeichert.

## Beispiele

Zeigt, wie ein Wasserzeichenbild in das Dokument eingefügt wird.

```csharp
string doc = MyDir + "Document.docx";
string watermarkImage = ImageDir + "Logo.jpg";

Watermarker.SetImage(doc, ArtifactsDir + "LowCode.SetWatermarkImage.1.docx", watermarkImage);
Watermarker.SetImage(doc, ArtifactsDir + "LowCode.SetWatermarkText.2.docx", SaveFormat.Docx, watermarkImage);

ImageWatermarkOptions options = new ImageWatermarkOptions();
options.Scale = 50;
Watermarker.SetImage(doc, ArtifactsDir + "LowCode.SetWatermarkText.3.docx", watermarkImage, options);
Watermarker.SetImage(doc, ArtifactsDir + "LowCode.SetWatermarkText.4.docx", SaveFormat.Docx, watermarkImage, options);
```

### Siehe auch

* class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* class [Watermarker](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## SetImage(*string, string, [SaveFormat](../../../aspose.words/saveformat/), string, [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)*) {#setimage_4}

Fügt dem Dokument mit Optionen und angegebenem Speicherformat ein Bildwasserzeichen hinzu.

```csharp
public static void SetImage(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    string watermarkImageFileName, ImageWatermarkOptions options = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | String | Der Name der Eingabedatei. |
| outputFileName | String | Der Name der Ausgabedatei. |
| saveFormat | SaveFormat | Das Speicherformat. |
| watermarkImageFileName | String | Bild, das als Wasserzeichen angezeigt wird. |
| options | ImageWatermarkOptions | Definiert zusätzliche Optionen für das Bildwasserzeichen. |

## Bemerkungen

Wenn das Ausgabeformat ein Bild (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP) ist, wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jedes Teil nach der Regel „outputFile_partIndex.extension“ zu generieren.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelne TIFF-Datei mit mehreren Frames gespeichert.

## Beispiele

Zeigt, wie ein Wasserzeichenbild in das Dokument eingefügt wird.

```csharp
string doc = MyDir + "Document.docx";
string watermarkImage = ImageDir + "Logo.jpg";

Watermarker.SetImage(doc, ArtifactsDir + "LowCode.SetWatermarkImage.1.docx", watermarkImage);
Watermarker.SetImage(doc, ArtifactsDir + "LowCode.SetWatermarkText.2.docx", SaveFormat.Docx, watermarkImage);

ImageWatermarkOptions options = new ImageWatermarkOptions();
options.Scale = 50;
Watermarker.SetImage(doc, ArtifactsDir + "LowCode.SetWatermarkText.3.docx", watermarkImage, options);
Watermarker.SetImage(doc, ArtifactsDir + "LowCode.SetWatermarkText.4.docx", SaveFormat.Docx, watermarkImage, options);
```

### Siehe auch

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* class [Watermarker](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## SetImage(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), string, [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)*) {#setimage_5}

Fügt dem Dokument mit Optionen und angegebenem Speicherformat ein Bildwasserzeichen hinzu.

```csharp
public static void SetImage(string inputFileName, string outputFileName, SaveOptions saveOptions, 
    string watermarkImageFileName, ImageWatermarkOptions options = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | String | Der Name der Eingabedatei. |
| outputFileName | String | Der Name der Ausgabedatei. |
| saveOptions | SaveOptions | Die Speicheroptionen. |
| watermarkImageFileName | String | Bild, das als Wasserzeichen angezeigt wird. |
| options | ImageWatermarkOptions | Definiert zusätzliche Optionen für das Bildwasserzeichen. |

## Bemerkungen

Wenn das Ausgabeformat ein Bild (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP) ist, wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jedes Teil nach der Regel „outputFile_partIndex.extension“ zu generieren.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelne TIFF-Datei mit mehreren Frames gespeichert.

### Siehe auch

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* class [Watermarker](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## SetImage(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), Image, [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)*) {#setimage}

Fügt dem Dokument aus Streams mit Optionen ein Bildwasserzeichen hinzu.

```csharp
public static void SetImage(Stream inputStream, Stream outputStream, SaveFormat saveFormat, 
    Image watermarkImage, ImageWatermarkOptions options = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | Stream | Der Eingabestream. |
| outputStream | Stream | Der Ausgabestream. |
| saveFormat | SaveFormat | Das Speicherformat. |
| watermarkImage | Image | Bild, das als Wasserzeichen angezeigt wird. |
| options | ImageWatermarkOptions | Definiert zusätzliche Optionen für das Bildwasserzeichen. |

## Bemerkungen

Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird nur die erste Seite der Ausgabe im angegebenen Stream gespeichert.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelnes TIFF mit mehreren Frames im angegebenen Stream gespeichert.

## Beispiele

Zeigt, wie ein Wasserzeichenbild aus einem Stream in das Dokument eingefügt wird.

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.SetWatermarkText.1.docx", FileMode.Create, FileAccess.ReadWrite))
        Watermarker.SetImage(streamIn, streamOut, SaveFormat.Docx, System.Drawing.Image.FromFile(ImageDir + "Logo.jpg"));
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.SetWatermarkText.2.docx", FileMode.Create, FileAccess.ReadWrite))
        Watermarker.SetImage(streamIn, streamOut, SaveFormat.Docx, System.Drawing.Image.FromFile(ImageDir + "Logo.jpg"), new ImageWatermarkOptions() { Scale = 50 });
}
```

### Siehe auch

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* class [Watermarker](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## SetImage(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), Image, [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)*) {#setimage_2}

Fügt dem Dokument aus Streams mit Optionen ein Bildwasserzeichen hinzu.

```csharp
public static void SetImage(Stream inputStream, Stream outputStream, SaveOptions saveOptions, 
    Image watermarkImage, ImageWatermarkOptions options = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | Stream | Der Eingabestream. |
| outputStream | Stream | Der Ausgabestream. |
| saveOptions | SaveOptions | Die Speicheroptionen. |
| watermarkImage | Image | Bild, das als Wasserzeichen angezeigt wird. |
| options | ImageWatermarkOptions | Definiert zusätzliche Optionen für das Bildwasserzeichen. |

## Bemerkungen

Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird nur die erste Seite der Ausgabe im angegebenen Stream gespeichert.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelnes TIFF mit mehreren Frames im angegebenen Stream gespeichert.

### Siehe auch

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* class [Watermarker](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## SetImage(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), Stream, [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)*) {#setimage_1}

Fügt dem Dokument aus Streams mit Optionen ein Bildwasserzeichen hinzu.

```csharp
public static void SetImage(Stream inputStream, Stream outputStream, SaveFormat saveFormat, 
    Stream watermarkImageStream, ImageWatermarkOptions options = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | Stream | Der Eingabestream. |
| outputStream | Stream | Der Ausgabestream. |
| saveFormat | SaveFormat | Das Speicherformat. |
| watermarkImageStream | Stream | Bildstream, der als Wasserzeichen angezeigt wird. |
| options | ImageWatermarkOptions | Definiert zusätzliche Optionen für das Bildwasserzeichen. |

## Bemerkungen

Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird nur die erste Seite der Ausgabe im angegebenen Stream gespeichert.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelnes TIFF mit mehreren Frames im angegebenen Stream gespeichert.

### Siehe auch

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* class [Watermarker](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## SetImage(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), Stream, [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)*) {#setimage_3}

Fügt dem Dokument aus Streams mit Optionen ein Bildwasserzeichen hinzu.

```csharp
public static void SetImage(Stream inputStream, Stream outputStream, SaveOptions saveOptions, 
    Stream watermarkImageStream, ImageWatermarkOptions options = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | Stream | Der Eingabestream. |
| outputStream | Stream | Der Ausgabestream. |
| saveOptions | SaveOptions | Die Speicheroptionen. |
| watermarkImageStream | Stream | Bildstream, der als Wasserzeichen angezeigt wird. |
| options | ImageWatermarkOptions | Definiert zusätzliche Optionen für das Bildwasserzeichen. |

## Bemerkungen

Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird nur die erste Seite der Ausgabe im angegebenen Stream gespeichert.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelnes TIFF mit mehreren Frames im angegebenen Stream gespeichert.

### Siehe auch

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* class [Watermarker](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)
