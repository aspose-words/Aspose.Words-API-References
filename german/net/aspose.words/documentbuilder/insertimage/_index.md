---
title: DocumentBuilder.InsertImage
linktitle: InsertImage
articleTitle: InsertImage
second_title: Aspose.Words für .NET
description: DocumentBuilder InsertImage methode. Fügt ein Bild aus einem .NET einImage Objekt in das Dokument einfügen. Das Bild wird inline und im Maßstab 100  eingefügt in C#.
type: docs
weight: 370
url: /de/net/aspose.words/documentbuilder/insertimage/
---
## InsertImage(*Image*) {#insertimage_3}

Fügt ein Bild aus einem .NET einImage -Objekt in das Dokument einfügen. Das Bild wird inline und im Maßstab 100 % eingefügt.

```csharp
public Shape InsertImage(Image image)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| image | Image | Das Bild, das in das Dokument eingefügt werden soll. |

### Rückgabewert

Der Bildknoten, der gerade eingefügt wurde.

## Bemerkungen

Sie können die Bildgröße, Position, Positionierungsmethode und andere Einstellungen mit dem ändern[`Shape`](../../../aspose.words.drawing/shape/) Von dieser Methode zurückgegebenes Objekt.

## Beispiele

Zeigt, wie man ein Bild von einem Objekt in ein Dokument einfügt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Image image = Image.FromFile(ImageDir + "Logo.jpg");

// Nachfolgend finden Sie drei Möglichkeiten, ein Bild aus einer Image-Objektinstanz einzufügen.
// 1 – Inline-Form mit einer Standardgröße basierend auf den Originalabmessungen des Bildes:
builder.InsertImage(image);

builder.InsertBreak(BreakType.PageBreak);

// 2 – Inline-Form mit benutzerdefinierten Abmessungen:
builder.InsertImage(image, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 – Schwebende Form mit benutzerdefinierten Abmessungen:
builder.InsertImage(image, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromImageObject.docx");
```

### Siehe auch

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## InsertImage(*string*) {#insertimage_9}

Fügt ein Bild aus einer Datei oder URL in das Dokument ein. Das Bild wird inline und im Maßstab 100 % eingefügt.

```csharp
public Shape InsertImage(string fileName)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | String | Die Datei mit dem Bild. Kann ein beliebiger gültiger lokaler oder Remote-URI sein. |

### Rückgabewert

Der Bildknoten, der gerade eingefügt wurde.

## Bemerkungen

Diese Überladung lädt das Bild automatisch herunter, bevor es in document eingefügt wird, wenn Sie einen Remote-URI angeben.

Sie können die Bildgröße, Position, Positionierungsmethode und andere Einstellungen mit dem ändern[`Shape`](../../../aspose.words.drawing/shape/) Von dieser Methode zurückgegebenes Objekt.

## Beispiele

Zeigt, wie man ein GIF-Bild in das Dokument einfügt.

```csharp
DocumentBuilder builder = new DocumentBuilder();

// Wir können ein GIF-Bild mithilfe eines Pfads oder eines Byte-Arrays einfügen.
// Funktioniert nur, wenn DocumentBuilder für Word Version 2010 oder höher optimiert ist.
// Beachten Sie, dass der Zugriff auf die Bildbytes eine Konvertierung von Gif in PNG bewirkt.
Shape gifImage = builder.InsertImage(ImageDir + "Graphics Interchange Format.gif");

gifImage = builder.InsertImage(File.ReadAllBytes(ImageDir + "Graphics Interchange Format.gif"));

builder.Document.Save(ArtifactsDir + "InsertGif.docx");
```

Zeigt, wie man eine Form mit einem Bild in ein Dokument einfügt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Nachfolgend finden Sie zwei Speicherorte für die Methode „InsertShape“ des Document Builders
// kann das Bild liefern, das die Form anzeigt.
// 1 – Übergeben Sie einen lokalen Dateisystem-Dateinamen einer Bilddatei:
builder.Write("Image from local file: ");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.Writeln();

// 2 – Übergeben Sie eine URL, die auf ein Bild verweist.
builder.Write("Image from a URL: ");
builder.InsertImage(ImageUrl);
builder.Writeln();

doc.Save(ArtifactsDir + "Image.FromUrl.docx");
```

Zeigt, wie man ein schwebendes Bild in der Mitte einer Seite einfügt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie ein schwebendes Bild ein, das hinter dem überlappenden Text erscheint, und richten Sie es in der Mitte der Seite aus.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;
shape.BehindText = true;
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.HorizontalAlignment = HorizontalAlignment.Center;
shape.VerticalAlignment = VerticalAlignment.Center;

doc.Save(ArtifactsDir + "Image.CreateFloatingPageCenter.docx");
```

Zeigt, wie Sie bestimmen, welches Bild eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertImage(ImageDir + "Scalable Vector Graphics.svg");

// Aspose.Words fügt SVG-Bild als PNG mit der Erweiterung „svgBlip“ in das Dokument ein
// das die ursprüngliche Vektor-SVG-Bilddarstellung enthält.
doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertSvgImage.SvgWithSvgBlip.docx");

// Aspose.Words fügt das SVG-Bild als PNG in das Dokument ein, genau wie Microsoft Word es für das alte Format tut.
doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertSvgImage.Svg.doc");

doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2003);

// Aspose.Words fügt SVG-Bild als EMF-Metadatei in das Dokument ein, um das Bild in Vektordarstellung beizubehalten.
doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertSvgImage.Emf.docx");
```

Zeigt, wie man ein Bild aus dem lokalen Dateisystem in ein Dokument einfügt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Nachfolgend finden Sie drei Möglichkeiten, ein Bild aus einem lokalen Systemdateinamen einzufügen.
// 1 – Inline-Form mit einer Standardgröße basierend auf den Originalabmessungen des Bildes:
builder.InsertImage(ImageDir + "Logo.jpg");

builder.InsertBreak(BreakType.PageBreak);

// 2 – Inline-Form mit benutzerdefinierten Abmessungen:
builder.InsertImage(ImageDir + "Transparent background logo.png", ConvertUtil.PixelToPoint(250),
    ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 – Schwebende Form mit benutzerdefinierten Abmessungen:
builder.InsertImage(ImageDir + "Windows MetaFile.wmf", RelativeHorizontalPosition.Margin, 100, 
    RelativeVerticalPosition.Margin, 100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromFilename.docx");
```

### Siehe auch

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## InsertImage(*Stream*) {#insertimage_6}

Fügt ein Bild aus einem Stream in das Dokument ein. Das Bild wird inline und im Maßstab 100 % eingefügt.

```csharp
public Shape InsertImage(Stream stream)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| stream | Stream | Der Stream, der das Bild enthält. |

### Rückgabewert

Der Bildknoten, der gerade eingefügt wurde.

## Bemerkungen

Sie können die Bildgröße, Position, Positionierungsmethode und andere Einstellungen mit dem ändern[`Shape`](../../../aspose.words.drawing/shape/) Von dieser Methode zurückgegebenes Objekt.

## Beispiele

Zeigt, wie man eine Form mit einem Bild aus einem Stream in ein Dokument einfügt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

using (Stream stream = File.OpenRead(ImageDir + "Logo.jpg"))
{
    builder.Write("Image from stream: ");
    builder.InsertImage(stream);
}

doc.Save(ArtifactsDir + "Image.FromStream.docx");
```

Zeigt, wie ein Bild aus einem Stream in ein Dokument eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

using (Stream stream = File.OpenRead(ImageDir + "Logo.jpg"))
{
    // Nachfolgend finden Sie drei Möglichkeiten, ein Bild aus einem Stream einzufügen.
    // 1 – Inline-Form mit einer Standardgröße basierend auf den Originalabmessungen des Bildes:
    builder.InsertImage(stream);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 – Inline-Form mit benutzerdefinierten Abmessungen:
    builder.InsertImage(stream, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 – Schwebende Form mit benutzerdefinierten Abmessungen:
    builder.InsertImage(stream, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
        100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromStream.docx");
```

### Siehe auch

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## InsertImage(*byte[]*) {#insertimage}

Fügt ein Bild aus einem Byte-Array in das Dokument ein. Das Bild wird inline und im Maßstab 100 % eingefügt.

```csharp
public Shape InsertImage(byte[] imageBytes)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| imageBytes | Byte[] | Das Byte-Array, das das Bild enthält. |

### Rückgabewert

Der Bildknoten, der gerade eingefügt wurde.

## Bemerkungen

Sie können die Bildgröße, Position, Positionierungsmethode und andere Einstellungen mit dem ändern[`Shape`](../../../aspose.words.drawing/shape/) Von dieser Methode zurückgegebenes Objekt.

## Beispiele

Zeigt, wie man ein Bild aus einem Byte-Array in ein Dokument einfügt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Image image = Image.FromFile(ImageDir + "Logo.jpg");

using (MemoryStream ms = new MemoryStream())
{
    image.Save(ms, ImageFormat.Png);
    byte[] imageByteArray = ms.ToArray();

    // Nachfolgend finden Sie drei Möglichkeiten, ein Bild aus einem Byte-Array einzufügen.
    // 1 – Inline-Form mit einer Standardgröße basierend auf den Originalabmessungen des Bildes:
    builder.InsertImage(imageByteArray);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 – Inline-Form mit benutzerdefinierten Abmessungen:
    builder.InsertImage(imageByteArray, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 – Schwebende Form mit benutzerdefinierten Abmessungen:
    builder.InsertImage(imageByteArray, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin, 
    100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromByteArray.docx");
```

Zeigt, wie ein Bild aus einem Byte-Array in ein Dokument eingefügt wird (.NetStandard 2.0).

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Durch die Dekodierung des Bildes wird es in das .png-Format konvertiert.
using (SKBitmap bitmap = SKBitmap.Decode(ImageDir + "Logo.jpg"))
{
    using (SKImage image = SKImage.FromBitmap(bitmap))
    {
        using (SKData data = image.Encode())
        {
            byte[] imageByteArray = data.ToArray();

            // Nachfolgend finden Sie drei Möglichkeiten, ein Bild aus einem Byte-Array einzufügen.
            // 1 – Inline-Form mit einer Standardgröße basierend auf den Originalabmessungen des Bildes:
            builder.InsertImage(imageByteArray);

            builder.InsertBreak(BreakType.PageBreak);

            // 2 – Inline-Form mit benutzerdefinierten Abmessungen:
            builder.InsertImage(imageByteArray, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

            builder.InsertBreak(BreakType.PageBreak);

            // 3 – Schwebende Form mit benutzerdefinierten Abmessungen:
            builder.InsertImage(imageByteArray, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
                100, 200, 100, WrapType.Square);
        }
    }
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromByteArrayNetStandard2.docx");
```

### Siehe auch

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## InsertImage(*Image, double, double*) {#insertimage_5}

Fügt ein Inline-Bild aus einem .NET einImage -Objekt in das Dokument ein und skaliert es auf die angegebene Größe.

```csharp
public Shape InsertImage(Image image, double width, double height)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| image | Image | Das Bild, das in das Dokument eingefügt werden soll. |
| width | Double | Die Breite des Bildes in Punkten. Kann ein negativer Wert oder ein Nullwert sein, um eine Skalierung von 100 % anzufordern. |
| height | Double | Die Höhe des Bildes in Punkten. Kann ein negativer Wert oder ein Nullwert sein, um eine Skalierung von 100 % anzufordern. |

### Rückgabewert

Der Bildknoten, der gerade eingefügt wurde.

## Bemerkungen

Sie können die Bildgröße, Position, Positionierungsmethode und andere Einstellungen mit dem ändern[`Shape`](../../../aspose.words.drawing/shape/) Von dieser Methode zurückgegebenes Objekt.

## Beispiele

Zeigt, wie man ein Bild von einem Objekt in ein Dokument einfügt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Image image = Image.FromFile(ImageDir + "Logo.jpg");

// Nachfolgend finden Sie drei Möglichkeiten, ein Bild aus einer Image-Objektinstanz einzufügen.
// 1 – Inline-Form mit einer Standardgröße basierend auf den Originalabmessungen des Bildes:
builder.InsertImage(image);

builder.InsertBreak(BreakType.PageBreak);

// 2 – Inline-Form mit benutzerdefinierten Abmessungen:
builder.InsertImage(image, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 – Schwebende Form mit benutzerdefinierten Abmessungen:
builder.InsertImage(image, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromImageObject.docx");
```

Zeigt, wie man ein Bild von einem Objekt in ein Dokument einfügt (.NetStandard 2.0).

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Durch die Dekodierung des Bildes wird es in das .png-Format konvertiert.
using (SKBitmap bitmap = SKBitmap.Decode(ImageDir + "Logo.jpg"))
{
    // Nachfolgend finden Sie drei Möglichkeiten, ein Bild aus einer Image-Objektinstanz einzufügen.
    // 1 – Inline-Form mit einer Standardgröße basierend auf den Originalabmessungen des Bildes:
    builder.InsertImage(bitmap);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 – Inline-Form mit benutzerdefinierten Abmessungen:
    builder.InsertImage(bitmap, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 – Schwebende Form mit benutzerdefinierten Abmessungen:
    builder.InsertImage(bitmap, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
        100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromImageObjectNetStandard2.docx");
```

### Siehe auch

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## InsertImage(*string, double, double*) {#insertimage_11}

Fügt ein Inline-Bild aus einer Datei oder URL in das Dokument ein und skaliert es auf die angegebene Größe.

```csharp
public Shape InsertImage(string fileName, double width, double height)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | String | Die Datei, die das Bild enthält. |
| width | Double | Die Breite des Bildes in Punkten. Kann ein negativer Wert oder ein Nullwert sein, um eine Skalierung von 100 % anzufordern. |
| height | Double | Die Höhe des Bildes in Punkten. Kann ein negativer Wert oder ein Nullwert sein, um eine Skalierung von 100 % anzufordern. |

### Rückgabewert

Der Bildknoten, der gerade eingefügt wurde.

## Bemerkungen

Sie können die Bildgröße, Position, Positionierungsmethode und andere Einstellungen mit dem ändern[`Shape`](../../../aspose.words.drawing/shape/) Von dieser Methode zurückgegebenes Objekt.

## Beispiele

Zeigt, wie man ein Bild aus dem lokalen Dateisystem in ein Dokument einfügt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Nachfolgend finden Sie drei Möglichkeiten, ein Bild aus einem lokalen Systemdateinamen einzufügen.
// 1 – Inline-Form mit einer Standardgröße basierend auf den Originalabmessungen des Bildes:
builder.InsertImage(ImageDir + "Logo.jpg");

builder.InsertBreak(BreakType.PageBreak);

// 2 – Inline-Form mit benutzerdefinierten Abmessungen:
builder.InsertImage(ImageDir + "Transparent background logo.png", ConvertUtil.PixelToPoint(250),
    ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 – Schwebende Form mit benutzerdefinierten Abmessungen:
builder.InsertImage(ImageDir + "Windows MetaFile.wmf", RelativeHorizontalPosition.Margin, 100, 
    RelativeVerticalPosition.Margin, 100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromFilename.docx");
```

### Siehe auch

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## InsertImage(*Stream, double, double*) {#insertimage_8}

Fügt ein Inline-Bild aus einem Stream in das Dokument ein und skaliert es auf die angegebene Größe.

```csharp
public Shape InsertImage(Stream stream, double width, double height)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| stream | Stream | Der Stream, der das Bild enthält. |
| width | Double | Die Breite des Bildes in Punkten. Kann ein negativer Wert oder ein Nullwert sein, um eine Skalierung von 100 % anzufordern. |
| height | Double | Die Höhe des Bildes in Punkten. Kann ein negativer Wert oder ein Nullwert sein, um eine Skalierung von 100 % anzufordern. |

### Rückgabewert

Der Bildknoten, der gerade eingefügt wurde.

## Bemerkungen

Sie können die Bildgröße, Position, Positionierungsmethode und andere Einstellungen mit dem ändern[`Shape`](../../../aspose.words.drawing/shape/) Von dieser Methode zurückgegebenes Objekt.

## Beispiele

Zeigt, wie ein Bild aus einem Stream in ein Dokument eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

using (Stream stream = File.OpenRead(ImageDir + "Logo.jpg"))
{
    // Nachfolgend finden Sie drei Möglichkeiten, ein Bild aus einem Stream einzufügen.
    // 1 – Inline-Form mit einer Standardgröße basierend auf den Originalabmessungen des Bildes:
    builder.InsertImage(stream);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 – Inline-Form mit benutzerdefinierten Abmessungen:
    builder.InsertImage(stream, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 – Schwebende Form mit benutzerdefinierten Abmessungen:
    builder.InsertImage(stream, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
        100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromStream.docx");
```

### Siehe auch

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## InsertImage(*byte[], double, double*) {#insertimage_2}

Fügt ein Inline-Bild aus einem Byte-Array in das Dokument ein und skaliert es auf die angegebene Größe.

```csharp
public Shape InsertImage(byte[] imageBytes, double width, double height)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| imageBytes | Byte[] | Das Byte-Array, das das Bild enthält. |
| width | Double | Die Breite des Bildes in Punkten. Kann ein negativer Wert oder ein Nullwert sein, um eine Skalierung von 100 % anzufordern. |
| height | Double | Die Höhe des Bildes in Punkten. Kann ein negativer Wert oder ein Nullwert sein, um eine Skalierung von 100 % anzufordern. |

### Rückgabewert

Der Bildknoten, der gerade eingefügt wurde.

## Bemerkungen

Sie können die Bildgröße, Position, Positionierungsmethode und andere Einstellungen mit dem ändern[`Shape`](../../../aspose.words.drawing/shape/) Von dieser Methode zurückgegebenes Objekt.

## Beispiele

Zeigt, wie man ein Bild aus einem Byte-Array in ein Dokument einfügt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Image image = Image.FromFile(ImageDir + "Logo.jpg");

using (MemoryStream ms = new MemoryStream())
{
    image.Save(ms, ImageFormat.Png);
    byte[] imageByteArray = ms.ToArray();

    // Nachfolgend finden Sie drei Möglichkeiten, ein Bild aus einem Byte-Array einzufügen.
    // 1 – Inline-Form mit einer Standardgröße basierend auf den Originalabmessungen des Bildes:
    builder.InsertImage(imageByteArray);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 – Inline-Form mit benutzerdefinierten Abmessungen:
    builder.InsertImage(imageByteArray, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 – Schwebende Form mit benutzerdefinierten Abmessungen:
    builder.InsertImage(imageByteArray, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin, 
    100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromByteArray.docx");
```

Zeigt, wie ein Bild aus einem Byte-Array in ein Dokument eingefügt wird (.NetStandard 2.0).

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Durch die Dekodierung des Bildes wird es in das .png-Format konvertiert.
using (SKBitmap bitmap = SKBitmap.Decode(ImageDir + "Logo.jpg"))
{
    using (SKImage image = SKImage.FromBitmap(bitmap))
    {
        using (SKData data = image.Encode())
        {
            byte[] imageByteArray = data.ToArray();

            // Nachfolgend finden Sie drei Möglichkeiten, ein Bild aus einem Byte-Array einzufügen.
            // 1 – Inline-Form mit einer Standardgröße basierend auf den Originalabmessungen des Bildes:
            builder.InsertImage(imageByteArray);

            builder.InsertBreak(BreakType.PageBreak);

            // 2 – Inline-Form mit benutzerdefinierten Abmessungen:
            builder.InsertImage(imageByteArray, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

            builder.InsertBreak(BreakType.PageBreak);

            // 3 – Schwebende Form mit benutzerdefinierten Abmessungen:
            builder.InsertImage(imageByteArray, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
                100, 200, 100, WrapType.Square);
        }
    }
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromByteArrayNetStandard2.docx");
```

### Siehe auch

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## InsertImage(*Image, [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../../aspose.words.drawing/wraptype/)*) {#insertimage_4}

Fügt ein Bild aus einem .NET einImage Objekt an der angegebenen Position und Größe.

```csharp
public Shape InsertImage(Image image, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| image | Image | Das Bild, das in das Dokument eingefügt werden soll. |
| horzPos | RelativeHorizontalPosition | Gibt an, von wo aus der Abstand zum Bild gemessen wird. |
| left | Double | Abstand in Punkten vom Ursprung zur linken Seite des Bildes. |
| vertPos | RelativeVerticalPosition | Gibt an, von wo aus der Abstand zum Bild gemessen wird. |
| top | Double | Abstand in Punkten vom Ursprung zur oberen Seite des Bildes. |
| width | Double | Die Breite des Bildes in Punkten. Kann ein negativer Wert oder ein Nullwert sein, um eine Skalierung von 100 % anzufordern. |
| height | Double | Die Höhe des Bildes in Punkten. Kann ein negativer Wert oder ein Nullwert sein, um eine Skalierung von 100 % anzufordern. |
| wrapType | WrapType | Gibt an, wie Text um das Bild herum umbrochen wird. |

### Rückgabewert

Der Bildknoten, der gerade eingefügt wurde.

## Bemerkungen

Sie können die Bildgröße, Position, Positionierungsmethode und andere Einstellungen mit dem ändern[`Shape`](../../../aspose.words.drawing/shape/) Von dieser Methode zurückgegebenes Objekt.

## Beispiele

Zeigt, wie man ein Bild von einem Objekt in ein Dokument einfügt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Image image = Image.FromFile(ImageDir + "Logo.jpg");

// Nachfolgend finden Sie drei Möglichkeiten, ein Bild aus einer Image-Objektinstanz einzufügen.
// 1 – Inline-Form mit einer Standardgröße basierend auf den Originalabmessungen des Bildes:
builder.InsertImage(image);

builder.InsertBreak(BreakType.PageBreak);

// 2 – Inline-Form mit benutzerdefinierten Abmessungen:
builder.InsertImage(image, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 – Schwebende Form mit benutzerdefinierten Abmessungen:
builder.InsertImage(image, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromImageObject.docx");
```

Zeigt, wie man ein Bild von einem Objekt in ein Dokument einfügt (.NetStandard 2.0).

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Durch die Dekodierung des Bildes wird es in das .png-Format konvertiert.
using (SKBitmap bitmap = SKBitmap.Decode(ImageDir + "Logo.jpg"))
{
    // Nachfolgend finden Sie drei Möglichkeiten, ein Bild aus einer Image-Objektinstanz einzufügen.
    // 1 – Inline-Form mit einer Standardgröße basierend auf den Originalabmessungen des Bildes:
    builder.InsertImage(bitmap);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 – Inline-Form mit benutzerdefinierten Abmessungen:
    builder.InsertImage(bitmap, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 – Schwebende Form mit benutzerdefinierten Abmessungen:
    builder.InsertImage(bitmap, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
        100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromImageObjectNetStandard2.docx");
```

### Siehe auch

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## InsertImage(*string, [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../../aspose.words.drawing/wraptype/)*) {#insertimage_10}

Fügt ein Bild aus einer Datei oder URL an der angegebenen Position und Größe ein.

```csharp
public Shape InsertImage(string fileName, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | String | Die Datei, die das Bild enthält. |
| horzPos | RelativeHorizontalPosition | Gibt an, von wo aus der Abstand zum Bild gemessen wird. |
| left | Double | Abstand in Punkten vom Ursprung zur linken Seite des Bildes. |
| vertPos | RelativeVerticalPosition | Gibt an, von wo aus der Abstand zum Bild gemessen wird. |
| top | Double | Abstand in Punkten vom Ursprung zur oberen Seite des Bildes. |
| width | Double | Die Breite des Bildes in Punkten. Kann ein negativer Wert oder ein Nullwert sein, um eine Skalierung von 100 % anzufordern. |
| height | Double | Die Höhe des Bildes in Punkten. Kann ein negativer Wert oder ein Nullwert sein, um eine Skalierung von 100 % anzufordern. |
| wrapType | WrapType | Gibt an, wie Text um das Bild herum umbrochen wird. |

### Rückgabewert

Der Bildknoten, der gerade eingefügt wurde.

## Bemerkungen

Sie können die Bildgröße, Position, Positionierungsmethode und andere Einstellungen mit dem ändern[`Shape`](../../../aspose.words.drawing/shape/) Von dieser Methode zurückgegebenes Objekt.

## Beispiele

Zeigt, wie ein Bild eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Es gibt zwei Möglichkeiten, mit einem Document Builder ein Bild zu erstellen und es dann als schwebende Form einzufügen.
// 1 - Aus einer Datei im lokalen Dateisystem:
builder.InsertImage(ImageDir + "Transparent background logo.png", RelativeHorizontalPosition.Margin, 100,
    RelativeVerticalPosition.Margin, 0, 200, 200, WrapType.Square);

// 2 - Von einer URL:
builder.InsertImage(ImageUrl, RelativeHorizontalPosition.Margin, 100,
    RelativeVerticalPosition.Margin, 250, 200, 200, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertFloatingImage.docx");
```

Zeigt, wie man ein Bild aus dem lokalen Dateisystem in ein Dokument einfügt und dabei seine Abmessungen beibehält.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Die Methode „InsertImage“ erstellt eine schwebende Form mit dem übergebenen Bild in ihren Bilddaten.
// Wir können die Abmessungen der Form angeben und sie an diese Methode übergeben.
Shape imageShape = builder.InsertImage(ImageDir + "Logo.jpg", RelativeHorizontalPosition.Margin, 0,
    RelativeVerticalPosition.Margin, 0, -1, -1, WrapType.Square);

// Übergabe negativer Werte, da die beabsichtigten Abmessungen automatisch definiert werden
// die Abmessungen der Form basierend auf den Abmessungen ihres Bildes.
Assert.AreEqual(300.0d, imageShape.Width);
Assert.AreEqual(300.0d, imageShape.Height);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertImageOriginalSize.docx");
```

Zeigt, wie man ein Bild aus dem lokalen Dateisystem in ein Dokument einfügt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Nachfolgend finden Sie drei Möglichkeiten, ein Bild aus einem lokalen Systemdateinamen einzufügen.
// 1 – Inline-Form mit einer Standardgröße basierend auf den Originalabmessungen des Bildes:
builder.InsertImage(ImageDir + "Logo.jpg");

builder.InsertBreak(BreakType.PageBreak);

// 2 – Inline-Form mit benutzerdefinierten Abmessungen:
builder.InsertImage(ImageDir + "Transparent background logo.png", ConvertUtil.PixelToPoint(250),
    ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 – Schwebende Form mit benutzerdefinierten Abmessungen:
builder.InsertImage(ImageDir + "Windows MetaFile.wmf", RelativeHorizontalPosition.Margin, 100, 
    RelativeVerticalPosition.Margin, 100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromFilename.docx");
```

### Siehe auch

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## InsertImage(*Stream, [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../../aspose.words.drawing/wraptype/)*) {#insertimage_7}

Fügt ein Bild aus einem Stream an der angegebenen Position und Größe ein.

```csharp
public Shape InsertImage(Stream stream, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| stream | Stream | Der Stream, der das Bild enthält. |
| horzPos | RelativeHorizontalPosition | Gibt an, von wo aus der Abstand zum Bild gemessen wird. |
| left | Double | Abstand in Punkten vom Ursprung zur linken Seite des Bildes. |
| vertPos | RelativeVerticalPosition | Gibt an, von wo aus der Abstand zum Bild gemessen wird. |
| top | Double | Abstand in Punkten vom Ursprung zur oberen Seite des Bildes. |
| width | Double | Die Breite des Bildes in Punkten. Kann ein negativer Wert oder ein Nullwert sein, um eine Skalierung von 100 % anzufordern. |
| height | Double | Die Höhe des Bildes in Punkten. Kann ein negativer Wert oder ein Nullwert sein, um eine Skalierung von 100 % anzufordern. |
| wrapType | WrapType | Gibt an, wie Text um das Bild herum umbrochen wird. |

### Rückgabewert

Der Bildknoten, der gerade eingefügt wurde.

## Bemerkungen

Sie können die Bildgröße, Position, Positionierungsmethode und andere Einstellungen mit dem ändern[`Shape`](../../../aspose.words.drawing/shape/) Von dieser Methode zurückgegebenes Objekt.

## Beispiele

Zeigt, wie ein Bild aus einem Stream in ein Dokument eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

using (Stream stream = File.OpenRead(ImageDir + "Logo.jpg"))
{
    // Nachfolgend finden Sie drei Möglichkeiten, ein Bild aus einem Stream einzufügen.
    // 1 – Inline-Form mit einer Standardgröße basierend auf den Originalabmessungen des Bildes:
    builder.InsertImage(stream);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 – Inline-Form mit benutzerdefinierten Abmessungen:
    builder.InsertImage(stream, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 – Schwebende Form mit benutzerdefinierten Abmessungen:
    builder.InsertImage(stream, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
        100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromStream.docx");
```

### Siehe auch

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## InsertImage(*byte[], [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../../aspose.words.drawing/wraptype/)*) {#insertimage_1}

Fügt ein Bild aus einem Byte-Array an der angegebenen Position und Größe ein.

```csharp
public Shape InsertImage(byte[] imageBytes, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| imageBytes | Byte[] | Das Byte-Array, das das Bild enthält. |
| horzPos | RelativeHorizontalPosition | Gibt an, von wo aus der Abstand zum Bild gemessen wird. |
| left | Double | Abstand in Punkten vom Ursprung zur linken Seite des Bildes. |
| vertPos | RelativeVerticalPosition | Gibt an, von wo aus der Abstand zum Bild gemessen wird. |
| top | Double | Abstand in Punkten vom Ursprung zur oberen Seite des Bildes. |
| width | Double | Die Breite des Bildes in Punkten. Kann ein negativer Wert oder ein Nullwert sein, um eine Skalierung von 100 % anzufordern. |
| height | Double | Die Höhe des Bildes in Punkten. Kann ein negativer Wert oder ein Nullwert sein, um eine Skalierung von 100 % anzufordern. |
| wrapType | WrapType | Gibt an, wie Text um das Bild herum umbrochen wird. |

### Rückgabewert

Der Bildknoten, der gerade eingefügt wurde.

## Bemerkungen

Sie können die Bildgröße, Position, Positionierungsmethode und andere Einstellungen mit dem ändern[`Shape`](../../../aspose.words.drawing/shape/) Von dieser Methode zurückgegebenes Objekt.

## Beispiele

Zeigt, wie man ein Bild aus einem Byte-Array in ein Dokument einfügt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Image image = Image.FromFile(ImageDir + "Logo.jpg");

using (MemoryStream ms = new MemoryStream())
{
    image.Save(ms, ImageFormat.Png);
    byte[] imageByteArray = ms.ToArray();

    // Nachfolgend finden Sie drei Möglichkeiten, ein Bild aus einem Byte-Array einzufügen.
    // 1 – Inline-Form mit einer Standardgröße basierend auf den Originalabmessungen des Bildes:
    builder.InsertImage(imageByteArray);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 – Inline-Form mit benutzerdefinierten Abmessungen:
    builder.InsertImage(imageByteArray, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 – Schwebende Form mit benutzerdefinierten Abmessungen:
    builder.InsertImage(imageByteArray, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin, 
    100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromByteArray.docx");
```

Zeigt, wie ein Bild aus einem Byte-Array in ein Dokument eingefügt wird (.NetStandard 2.0).

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Durch die Dekodierung des Bildes wird es in das .png-Format konvertiert.
using (SKBitmap bitmap = SKBitmap.Decode(ImageDir + "Logo.jpg"))
{
    using (SKImage image = SKImage.FromBitmap(bitmap))
    {
        using (SKData data = image.Encode())
        {
            byte[] imageByteArray = data.ToArray();

            // Nachfolgend finden Sie drei Möglichkeiten, ein Bild aus einem Byte-Array einzufügen.
            // 1 – Inline-Form mit einer Standardgröße basierend auf den Originalabmessungen des Bildes:
            builder.InsertImage(imageByteArray);

            builder.InsertBreak(BreakType.PageBreak);

            // 2 – Inline-Form mit benutzerdefinierten Abmessungen:
            builder.InsertImage(imageByteArray, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

            builder.InsertBreak(BreakType.PageBreak);

            // 3 – Schwebende Form mit benutzerdefinierten Abmessungen:
            builder.InsertImage(imageByteArray, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
                100, 200, 100, WrapType.Square);
        }
    }
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromByteArrayNetStandard2.docx");
```

### Siehe auch

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
