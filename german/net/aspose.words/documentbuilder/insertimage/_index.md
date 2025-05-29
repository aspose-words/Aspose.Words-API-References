---
title: DocumentBuilder.InsertImage
linktitle: InsertImage
articleTitle: InsertImage
second_title: Aspose.Words für .NET
description: Verbessern Sie Ihre Dokumente mühelos mit der InsertImage-Methode von DocumentBuilder, die das nahtlose Einfügen von .NET-Bildern in voller Größe für beeindruckende visuelle Darstellungen ermöglicht.
type: docs
weight: 400
url: /de/net/aspose.words/documentbuilder/insertimage/
---
## InsertImage(*Image*) {#insertimage_3}

Fügt ein Bild aus einer .NETImage Objekt in das Dokument. Das Bild wird inline und im Maßstab 100 % eingefügt.

```csharp
public Shape InsertImage(Image image)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| image | Image | Das in das Dokument einzufügende Bild. |

### Rückgabewert

Der Bildknoten, der gerade eingefügt wurde.

## Bemerkungen

Sie können die Bildgröße, den Speicherort, die Positionierungsmethode und andere Einstellungen mit dem ändern.[`Shape`](../../../aspose.words.drawing/shape/) von dieser Methode zurückgegebenes Objekt.

## Beispiele

Zeigt, wie ein Bild aus einem Objekt in ein Dokument eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string imageFile = ImageDir + "Logo.jpg";

// Unten sind drei Möglichkeiten zum Einfügen eines Bilds aus einer Image-Objektinstanz aufgeführt.
// 1 – Inline-Form mit einer Standardgröße basierend auf den Originalabmessungen des Bildes:
builder.InsertImage(imageFile);

builder.InsertBreak(BreakType.PageBreak);

// 2 - Inline-Form mit benutzerdefinierten Abmessungen:
builder.InsertImage(imageFile, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - Schwebende Form mit benutzerdefinierten Abmessungen:
builder.InsertImage(imageFile, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
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
| fileName | String | Die Datei mit dem Bild. Kann jede gültige lokale oder Remote-URI sein. |

### Rückgabewert

Der Bildknoten, der gerade eingefügt wurde.

## Bemerkungen

Diese Überladung lädt das Bild automatisch herunter, bevor es in das Dokument eingefügt wird, wenn Sie eine Remote-URI angeben.

Sie können die Bildgröße, den Speicherort, die Positionierungsmethode und andere Einstellungen mit dem ändern.[`Shape`](../../../aspose.words.drawing/shape/) von dieser Methode zurückgegebenes Objekt.

## Beispiele

Zeigt, wie ein WebP-Bild eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertImage(ImageDir + "WebP image.webp");

doc.Save(ArtifactsDir + "Image.InsertWebpImage.docx");
```

Zeigt, wie ein GIF-Bild in das Dokument eingefügt wird.

```csharp
DocumentBuilder builder = new DocumentBuilder();

// Wir können ein GIF-Bild mithilfe eines Pfads oder eines Byte-Arrays einfügen.
// Es funktioniert nur, wenn DocumentBuilder für Word Version 2010 oder höher optimiert ist.
// Beachten Sie, dass der Zugriff auf die Bildbytes eine Konvertierung von GIF in PNG bewirkt.
Shape gifImage = builder.InsertImage(ImageDir + "Graphics Interchange Format.gif");

gifImage = builder.InsertImage(File.ReadAllBytes(ImageDir + "Graphics Interchange Format.gif"));

builder.Document.Save(ArtifactsDir + "InsertGif.docx");
```

Zeigt, wie eine Form mit einem Bild in ein Dokument eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Unten sind zwei Stellen aufgeführt, an denen die Methode "InsertShape" des Dokument-Generators
// kann das Bild, das die Form anzeigen wird, als Quelle verwenden.
// 1 – Übergeben Sie den Dateinamen einer Bilddatei im lokalen Dateisystem:
builder.Write("Image from local file: ");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.Writeln();

// 2 – Übergeben Sie eine URL, die auf ein Bild verweist.
builder.Write("Image from a URL: ");
builder.InsertImage(ImageUrl);
builder.Writeln();

doc.Save(ArtifactsDir + "Image.FromUrl.docx");
```

Zeigt, wie ein schwebendes Bild in die Mitte einer Seite eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie ein schwebendes Bild ein, das hinter dem überlappenden Text angezeigt wird, und richten Sie es an der Seitenmitte aus.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;
shape.BehindText = true;
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.HorizontalAlignment = HorizontalAlignment.Center;
shape.VerticalAlignment = VerticalAlignment.Center;

doc.Save(ArtifactsDir + "Image.CreateFloatingPageCenter.docx");
```

Zeigt, wie bestimmt wird, welches Bild eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertImage(ImageDir + "Scalable Vector Graphics.svg");

// Aspose.Words fügt SVG-Bild als PNG mit svgBlip-Erweiterung in das Dokument ein
// das die ursprüngliche Vektor-SVG-Bilddarstellung enthält.
doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertSvgImage.SvgWithSvgBlip.docx");

// Aspose.Words fügt das SVG-Bild als PNG in das Dokument ein, genau wie Microsoft Word es für das alte Format tut.
doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertSvgImage.Svg.doc");

doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2003);

// Aspose.Words fügt ein SVG-Bild als EMF-Metadatei in das Dokument ein, um das Bild in der Vektordarstellung zu behalten.
doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertSvgImage.Emf.docx");
```

Zeigt, wie ein Bild aus dem lokalen Dateisystem in ein Dokument eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Unten sind drei Möglichkeiten zum Einfügen eines Bildes aus einem lokalen Systemdateinamen aufgeführt.
// 1 – Inline-Form mit einer Standardgröße basierend auf den Originalabmessungen des Bildes:
builder.InsertImage(ImageDir + "Logo.jpg");

builder.InsertBreak(BreakType.PageBreak);

// 2 - Inline-Form mit benutzerdefinierten Abmessungen:
builder.InsertImage(ImageDir + "Transparent background logo.png", ConvertUtil.PixelToPoint(250),
    ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - Schwebende Form mit benutzerdefinierten Abmessungen:
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

Sie können die Bildgröße, den Speicherort, die Positionierungsmethode und andere Einstellungen mit dem ändern.[`Shape`](../../../aspose.words.drawing/shape/) von dieser Methode zurückgegebenes Objekt.

## Beispiele

Zeigt, wie eine Form mit einem Bild aus einem Stream in ein Dokument eingefügt wird.

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
    // Unten sind drei Möglichkeiten zum Einfügen eines Bildes aus einem Stream aufgeführt.
    // 1 – Inline-Form mit einer Standardgröße basierend auf den Originalabmessungen des Bildes:
    builder.InsertImage(stream);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 - Inline-Form mit benutzerdefinierten Abmessungen:
    builder.InsertImage(stream, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 - Schwebende Form mit benutzerdefinierten Abmessungen:
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

Sie können die Bildgröße, den Speicherort, die Positionierungsmethode und andere Einstellungen mit dem ändern.[`Shape`](../../../aspose.words.drawing/shape/) von dieser Methode zurückgegebenes Objekt.

## Beispiele

Zeigt, wie ein Bild aus einem Byte-Array in ein Dokument eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

byte[] imageByteArray = TestUtil.ImageToByteArray(ImageDir + "Logo.jpg");

// Unten sind drei Möglichkeiten zum Einfügen eines Bildes aus einem Byte-Array aufgeführt.
// 1 – Inline-Form mit einer Standardgröße basierend auf den Originalabmessungen des Bildes:
builder.InsertImage(imageByteArray);

builder.InsertBreak(BreakType.PageBreak);

// 2 - Inline-Form mit benutzerdefinierten Abmessungen:
builder.InsertImage(imageByteArray, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - Schwebende Form mit benutzerdefinierten Abmessungen:
builder.InsertImage(imageByteArray, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromByteArray.docx");
```

### Siehe auch

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## InsertImage(*Image, double, double*) {#insertimage_5}

Fügt ein Inline-Bild aus einem .NETImage -Objekt in das Dokument und skaliert es auf die angegebene Größe.

```csharp
public Shape InsertImage(Image image, double width, double height)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| image | Image | Das in das Dokument einzufügende Bild. |
| width | Double | Die Breite des Bildes in Punkten. Kann ein negativer oder Nullwert sein, um eine Skalierung von 100 % anzufordern. |
| height | Double | Die Höhe des Bildes in Punkten. Kann ein negativer oder Nullwert sein, um eine Skalierung von 100 % anzufordern. |

### Rückgabewert

Der Bildknoten, der gerade eingefügt wurde.

## Bemerkungen

Sie können die Bildgröße, den Speicherort, die Positionierungsmethode und andere Einstellungen mit dem ändern.[`Shape`](../../../aspose.words.drawing/shape/) von dieser Methode zurückgegebenes Objekt.

## Beispiele

Zeigt, wie ein Bild aus einem Objekt in ein Dokument eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string imageFile = ImageDir + "Logo.jpg";

// Unten sind drei Möglichkeiten zum Einfügen eines Bilds aus einer Image-Objektinstanz aufgeführt.
// 1 – Inline-Form mit einer Standardgröße basierend auf den Originalabmessungen des Bildes:
builder.InsertImage(imageFile);

builder.InsertBreak(BreakType.PageBreak);

// 2 - Inline-Form mit benutzerdefinierten Abmessungen:
builder.InsertImage(imageFile, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - Schwebende Form mit benutzerdefinierten Abmessungen:
builder.InsertImage(imageFile, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromImageObject.docx");
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
| width | Double | Die Breite des Bildes in Punkten. Kann ein negativer oder Nullwert sein, um eine Skalierung von 100 % anzufordern. |
| height | Double | Die Höhe des Bildes in Punkten. Kann ein negativer oder Nullwert sein, um eine Skalierung von 100 % anzufordern. |

### Rückgabewert

Der Bildknoten, der gerade eingefügt wurde.

## Bemerkungen

Sie können die Bildgröße, den Speicherort, die Positionierungsmethode und andere Einstellungen mit dem ändern.[`Shape`](../../../aspose.words.drawing/shape/) von dieser Methode zurückgegebenes Objekt.

## Beispiele

Zeigt, wie ein Bild aus dem lokalen Dateisystem in ein Dokument eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Unten sind drei Möglichkeiten zum Einfügen eines Bildes aus einem lokalen Systemdateinamen aufgeführt.
// 1 – Inline-Form mit einer Standardgröße basierend auf den Originalabmessungen des Bildes:
builder.InsertImage(ImageDir + "Logo.jpg");

builder.InsertBreak(BreakType.PageBreak);

// 2 - Inline-Form mit benutzerdefinierten Abmessungen:
builder.InsertImage(ImageDir + "Transparent background logo.png", ConvertUtil.PixelToPoint(250),
    ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - Schwebende Form mit benutzerdefinierten Abmessungen:
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
| width | Double | Die Breite des Bildes in Punkten. Kann ein negativer oder Nullwert sein, um eine Skalierung von 100 % anzufordern. |
| height | Double | Die Höhe des Bildes in Punkten. Kann ein negativer oder Nullwert sein, um eine Skalierung von 100 % anzufordern. |

### Rückgabewert

Der Bildknoten, der gerade eingefügt wurde.

## Bemerkungen

Sie können die Bildgröße, den Speicherort, die Positionierungsmethode und andere Einstellungen mit dem ändern.[`Shape`](../../../aspose.words.drawing/shape/) von dieser Methode zurückgegebenes Objekt.

## Beispiele

Zeigt, wie ein Bild aus einem Stream in ein Dokument eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

using (Stream stream = File.OpenRead(ImageDir + "Logo.jpg"))
{
    // Unten sind drei Möglichkeiten zum Einfügen eines Bildes aus einem Stream aufgeführt.
    // 1 – Inline-Form mit einer Standardgröße basierend auf den Originalabmessungen des Bildes:
    builder.InsertImage(stream);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 - Inline-Form mit benutzerdefinierten Abmessungen:
    builder.InsertImage(stream, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 - Schwebende Form mit benutzerdefinierten Abmessungen:
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
| width | Double | Die Breite des Bildes in Punkten. Kann ein negativer oder Nullwert sein, um eine Skalierung von 100 % anzufordern. |
| height | Double | Die Höhe des Bildes in Punkten. Kann ein negativer oder Nullwert sein, um eine Skalierung von 100 % anzufordern. |

### Rückgabewert

Der Bildknoten, der gerade eingefügt wurde.

## Bemerkungen

Sie können die Bildgröße, den Speicherort, die Positionierungsmethode und andere Einstellungen mit dem ändern.[`Shape`](../../../aspose.words.drawing/shape/) von dieser Methode zurückgegebenes Objekt.

## Beispiele

Zeigt, wie ein Bild aus einem Byte-Array in ein Dokument eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

byte[] imageByteArray = TestUtil.ImageToByteArray(ImageDir + "Logo.jpg");

// Unten sind drei Möglichkeiten zum Einfügen eines Bildes aus einem Byte-Array aufgeführt.
// 1 – Inline-Form mit einer Standardgröße basierend auf den Originalabmessungen des Bildes:
builder.InsertImage(imageByteArray);

builder.InsertBreak(BreakType.PageBreak);

// 2 - Inline-Form mit benutzerdefinierten Abmessungen:
builder.InsertImage(imageByteArray, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - Schwebende Form mit benutzerdefinierten Abmessungen:
builder.InsertImage(imageByteArray, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromByteArray.docx");
```

### Siehe auch

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## InsertImage(*Image, [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../../aspose.words.drawing/wraptype/)*) {#insertimage_4}

Fügt ein Bild aus einer .NETImage Objekt an der angegebenen Position und Größe.

```csharp
public Shape InsertImage(Image image, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| image | Image | Das in das Dokument einzufügende Bild. |
| horzPos | RelativeHorizontalPosition | Gibt an, von wo aus die Entfernung zum Bild gemessen wird. |
| left | Double | Abstand in Punkten vom Ursprung zur linken Seite des Bildes. |
| vertPos | RelativeVerticalPosition | Gibt an, von wo aus die Entfernung zum Bild gemessen wird. |
| top | Double | Abstand in Punkten vom Ursprung zur oberen Bildseite. |
| width | Double | Die Breite des Bildes in Punkten. Kann ein negativer oder Nullwert sein, um eine Skalierung von 100 % anzufordern. |
| height | Double | Die Höhe des Bildes in Punkten. Kann ein negativer oder Nullwert sein, um eine Skalierung von 100 % anzufordern. |
| wrapType | WrapType | Gibt an, wie der Text um das Bild herumfließen soll. |

### Rückgabewert

Der Bildknoten, der gerade eingefügt wurde.

## Bemerkungen

Sie können die Bildgröße, den Speicherort, die Positionierungsmethode und andere Einstellungen mit dem ändern.[`Shape`](../../../aspose.words.drawing/shape/) von dieser Methode zurückgegebenes Objekt.

## Beispiele

Zeigt, wie ein Bild aus einem Objekt in ein Dokument eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string imageFile = ImageDir + "Logo.jpg";

// Unten sind drei Möglichkeiten zum Einfügen eines Bilds aus einer Image-Objektinstanz aufgeführt.
// 1 – Inline-Form mit einer Standardgröße basierend auf den Originalabmessungen des Bildes:
builder.InsertImage(imageFile);

builder.InsertBreak(BreakType.PageBreak);

// 2 - Inline-Form mit benutzerdefinierten Abmessungen:
builder.InsertImage(imageFile, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - Schwebende Form mit benutzerdefinierten Abmessungen:
builder.InsertImage(imageFile, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromImageObject.docx");
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

Fügt ein Bild aus einer Datei oder URL an der angegebenen Position und in der angegebenen Größe ein.

```csharp
public Shape InsertImage(string fileName, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | String | Die Datei, die das Bild enthält. |
| horzPos | RelativeHorizontalPosition | Gibt an, von wo aus die Entfernung zum Bild gemessen wird. |
| left | Double | Abstand in Punkten vom Ursprung zur linken Seite des Bildes. |
| vertPos | RelativeVerticalPosition | Gibt an, von wo aus die Entfernung zum Bild gemessen wird. |
| top | Double | Abstand in Punkten vom Ursprung zur oberen Bildseite. |
| width | Double | Die Breite des Bildes in Punkten. Kann ein negativer oder Nullwert sein, um eine Skalierung von 100 % anzufordern. |
| height | Double | Die Höhe des Bildes in Punkten. Kann ein negativer oder Nullwert sein, um eine Skalierung von 100 % anzufordern. |
| wrapType | WrapType | Gibt an, wie der Text um das Bild herumfließen soll. |

### Rückgabewert

Der Bildknoten, der gerade eingefügt wurde.

## Bemerkungen

Sie können die Bildgröße, den Speicherort, die Positionierungsmethode und andere Einstellungen mit dem ändern.[`Shape`](../../../aspose.words.drawing/shape/) von dieser Methode zurückgegebenes Objekt.

## Beispiele

Zeigt, wie ein Bild eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Es gibt zwei Möglichkeiten, mit einem Dokumentgenerator ein Bild als Quelle zu verwenden und es dann als schwebende Form einzufügen.
// 1 – Aus einer Datei im lokalen Dateisystem:
builder.InsertImage(ImageDir + "Transparent background logo.png", RelativeHorizontalPosition.Margin, 100,
    RelativeVerticalPosition.Margin, 0, 200, 200, WrapType.Square);

// 2 - Von einer URL:
builder.InsertImage(ImageUrl, RelativeHorizontalPosition.Margin, 100,
    RelativeVerticalPosition.Margin, 250, 200, 200, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertFloatingImage.docx");
```

Zeigt, wie ein Bild aus dem lokalen Dateisystem unter Beibehaltung seiner Abmessungen in ein Dokument eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Die Methode InsertImage erstellt eine schwebende Form mit dem übergebenen Bild in ihren Bilddaten.
// Wir können die Abmessungen der Form angeben und sie an diese Methode übergeben.
Shape imageShape = builder.InsertImage(ImageDir + "Logo.jpg", RelativeHorizontalPosition.Margin, 0,
    RelativeVerticalPosition.Margin, 0, -1, -1, WrapType.Square);

// Durch die Übergabe negativer Werte als gewünschte Dimensionen wird automatisch definiert
// die Abmessungen der Form basierend auf den Abmessungen ihres Bildes.
Assert.AreEqual(300.0d, imageShape.Width);
Assert.AreEqual(300.0d, imageShape.Height);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertImageOriginalSize.docx");
```

Zeigt, wie ein Bild aus dem lokalen Dateisystem in ein Dokument eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Unten sind drei Möglichkeiten zum Einfügen eines Bildes aus einem lokalen Systemdateinamen aufgeführt.
// 1 – Inline-Form mit einer Standardgröße basierend auf den Originalabmessungen des Bildes:
builder.InsertImage(ImageDir + "Logo.jpg");

builder.InsertBreak(BreakType.PageBreak);

// 2 - Inline-Form mit benutzerdefinierten Abmessungen:
builder.InsertImage(ImageDir + "Transparent background logo.png", ConvertUtil.PixelToPoint(250),
    ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - Schwebende Form mit benutzerdefinierten Abmessungen:
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

Fügt ein Bild aus einem Stream an der angegebenen Position und in der angegebenen Größe ein.

```csharp
public Shape InsertImage(Stream stream, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| stream | Stream | Der Stream, der das Bild enthält. |
| horzPos | RelativeHorizontalPosition | Gibt an, von wo aus die Entfernung zum Bild gemessen wird. |
| left | Double | Abstand in Punkten vom Ursprung zur linken Seite des Bildes. |
| vertPos | RelativeVerticalPosition | Gibt an, von wo aus die Entfernung zum Bild gemessen wird. |
| top | Double | Abstand in Punkten vom Ursprung zur oberen Bildseite. |
| width | Double | Die Breite des Bildes in Punkten. Kann ein negativer oder Nullwert sein, um eine Skalierung von 100 % anzufordern. |
| height | Double | Die Höhe des Bildes in Punkten. Kann ein negativer oder Nullwert sein, um eine Skalierung von 100 % anzufordern. |
| wrapType | WrapType | Gibt an, wie der Text um das Bild herumfließen soll. |

### Rückgabewert

Der Bildknoten, der gerade eingefügt wurde.

## Bemerkungen

Sie können die Bildgröße, den Speicherort, die Positionierungsmethode und andere Einstellungen mit dem ändern.[`Shape`](../../../aspose.words.drawing/shape/) von dieser Methode zurückgegebenes Objekt.

## Beispiele

Zeigt, wie ein Bild aus einem Stream in ein Dokument eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

using (Stream stream = File.OpenRead(ImageDir + "Logo.jpg"))
{
    // Unten sind drei Möglichkeiten zum Einfügen eines Bildes aus einem Stream aufgeführt.
    // 1 – Inline-Form mit einer Standardgröße basierend auf den Originalabmessungen des Bildes:
    builder.InsertImage(stream);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 - Inline-Form mit benutzerdefinierten Abmessungen:
    builder.InsertImage(stream, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 - Schwebende Form mit benutzerdefinierten Abmessungen:
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
| horzPos | RelativeHorizontalPosition | Gibt an, von wo aus die Entfernung zum Bild gemessen wird. |
| left | Double | Abstand in Punkten vom Ursprung zur linken Seite des Bildes. |
| vertPos | RelativeVerticalPosition | Gibt an, von wo aus die Entfernung zum Bild gemessen wird. |
| top | Double | Abstand in Punkten vom Ursprung zur oberen Bildseite. |
| width | Double | Die Breite des Bildes in Punkten. Kann ein negativer oder Nullwert sein, um eine Skalierung von 100 % anzufordern. |
| height | Double | Die Höhe des Bildes in Punkten. Kann ein negativer oder Nullwert sein, um eine Skalierung von 100 % anzufordern. |
| wrapType | WrapType | Gibt an, wie der Text um das Bild herumfließen soll. |

### Rückgabewert

Der Bildknoten, der gerade eingefügt wurde.

## Bemerkungen

Sie können die Bildgröße, den Speicherort, die Positionierungsmethode und andere Einstellungen mit dem ändern.[`Shape`](../../../aspose.words.drawing/shape/) von dieser Methode zurückgegebenes Objekt.

## Beispiele

Zeigt, wie ein Bild aus einem Byte-Array in ein Dokument eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

byte[] imageByteArray = TestUtil.ImageToByteArray(ImageDir + "Logo.jpg");

// Unten sind drei Möglichkeiten zum Einfügen eines Bildes aus einem Byte-Array aufgeführt.
// 1 – Inline-Form mit einer Standardgröße basierend auf den Originalabmessungen des Bildes:
builder.InsertImage(imageByteArray);

builder.InsertBreak(BreakType.PageBreak);

// 2 - Inline-Form mit benutzerdefinierten Abmessungen:
builder.InsertImage(imageByteArray, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - Schwebende Form mit benutzerdefinierten Abmessungen:
builder.InsertImage(imageByteArray, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromByteArray.docx");
```

### Siehe auch

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
