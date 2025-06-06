---
title: Watermark.SetImage
linktitle: SetImage
articleTitle: SetImage
second_title: Aspose.Words für .NET
description: Optimieren Sie Ihre Dokumente mit der Wasserzeichen-SetImage-Methode. Fügen Sie mühelos beeindruckende Bildwasserzeichen für einen professionellen Touch hinzu.
type: docs
weight: 30
url: /de/net/aspose.words/watermark/setimage/
---
## SetImage(*Image*) {#setimage}

Fügt dem Dokument ein Bildwasserzeichen hinzu.

```csharp
public void SetImage(Image image)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| image | Image | Bild, das als Wasserzeichen angezeigt wird. |

### Ausnahmen

| Ausnahme | Bedingung |
| --- | --- |
| ArgumentNullException | Wird ausgelöst, wenn das Bild`null` . |

## Beispiele

Zeigt, wie aus einem Bild im lokalen Dateisystem ein Wasserzeichen erstellt wird.

```csharp
Document doc = new Document();

            // Ändern Sie das Erscheinungsbild des Bildwasserzeichens mit einem ImageWatermarkOptions-Objekt.
            // und übergeben Sie es dann beim Erstellen eines Wasserzeichens aus einer Bilddatei.
            ImageWatermarkOptions imageWatermarkOptions = new ImageWatermarkOptions();
            imageWatermarkOptions.Scale = 5;
            imageWatermarkOptions.IsWashout = false;

#if NET461_OR_GREATER || JAVA
            // Wir haben verschiedene Möglichkeiten, Bilder einzufügen:
            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"), imageWatermarkOptions);

            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"));

            doc.Watermark.SetImage(ImageDir + "Logo.jpg", imageWatermarkOptions);
#elif NET5_0_OR_GREATER
            using (SKBitmap image = SKBitmap.Decode(ImageDir + "Logo.jpg"))
            {
                doc.Watermark.SetImage(image, imageWatermarkOptions);
            }
#endif

            doc.Save(ArtifactsDir + "Document.ImageWatermark.docx");
```

### Siehe auch

* class [Watermark](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## SetImage(*Image, [ImageWatermarkOptions](../../imagewatermarkoptions/)*) {#setimage_1}

Fügt dem Dokument ein Bildwasserzeichen hinzu.

```csharp
public void SetImage(Image image, ImageWatermarkOptions options)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| image | Image | Bild, das als Wasserzeichen angezeigt wird. |
| options | ImageWatermarkOptions | Definiert zusätzliche Optionen für das Bildwasserzeichen. |

### Ausnahmen

| Ausnahme | Bedingung |
| --- | --- |
| ArgumentNullException | Wird ausgelöst, wenn das Bild`null` . |

## Bemerkungen

Wenn[`ImageWatermarkOptions`](../../imagewatermarkoptions/) Ist`null`, das Wasserzeichen wird mit den Standardoptionen gesetzt.

## Beispiele

Zeigt, wie aus einem Bild im lokalen Dateisystem ein Wasserzeichen erstellt wird.

```csharp
Document doc = new Document();

            // Ändern Sie das Erscheinungsbild des Bildwasserzeichens mit einem ImageWatermarkOptions-Objekt.
            // und übergeben Sie es dann beim Erstellen eines Wasserzeichens aus einer Bilddatei.
            ImageWatermarkOptions imageWatermarkOptions = new ImageWatermarkOptions();
            imageWatermarkOptions.Scale = 5;
            imageWatermarkOptions.IsWashout = false;

#if NET461_OR_GREATER || JAVA
            // Wir haben verschiedene Möglichkeiten, Bilder einzufügen:
            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"), imageWatermarkOptions);

            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"));

            doc.Watermark.SetImage(ImageDir + "Logo.jpg", imageWatermarkOptions);
#elif NET5_0_OR_GREATER
            using (SKBitmap image = SKBitmap.Decode(ImageDir + "Logo.jpg"))
            {
                doc.Watermark.SetImage(image, imageWatermarkOptions);
            }
#endif

            doc.Save(ArtifactsDir + "Document.ImageWatermark.docx");
```

### Siehe auch

* class [ImageWatermarkOptions](../../imagewatermarkoptions/)
* class [Watermark](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## SetImage(*string, [ImageWatermarkOptions](../../imagewatermarkoptions/)*) {#setimage_3}

Fügt dem Dokument ein Bildwasserzeichen hinzu.

```csharp
public void SetImage(string imagePath, ImageWatermarkOptions options)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| imagePath | String | Pfad zur Bilddatei, die als Wasserzeichen angezeigt wird. |
| options | ImageWatermarkOptions | Definiert zusätzliche Optionen für das Bildwasserzeichen. |

### Ausnahmen

| Ausnahme | Bedingung |
| --- | --- |
| ArgumentNullException | Wirft, wenn der Pfad`null` . |

## Bemerkungen

Wenn[`ImageWatermarkOptions`](../../imagewatermarkoptions/) Ist`null`, das Wasserzeichen wird mit den Standardoptionen gesetzt.

## Beispiele

Zeigt, wie aus einem Bild im lokalen Dateisystem ein Wasserzeichen erstellt wird.

```csharp
Document doc = new Document();

            // Ändern Sie das Erscheinungsbild des Bildwasserzeichens mit einem ImageWatermarkOptions-Objekt.
            // und übergeben Sie es dann beim Erstellen eines Wasserzeichens aus einer Bilddatei.
            ImageWatermarkOptions imageWatermarkOptions = new ImageWatermarkOptions();
            imageWatermarkOptions.Scale = 5;
            imageWatermarkOptions.IsWashout = false;

#if NET461_OR_GREATER || JAVA
            // Wir haben verschiedene Möglichkeiten, Bilder einzufügen:
            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"), imageWatermarkOptions);

            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"));

            doc.Watermark.SetImage(ImageDir + "Logo.jpg", imageWatermarkOptions);
#elif NET5_0_OR_GREATER
            using (SKBitmap image = SKBitmap.Decode(ImageDir + "Logo.jpg"))
            {
                doc.Watermark.SetImage(image, imageWatermarkOptions);
            }
#endif

            doc.Save(ArtifactsDir + "Document.ImageWatermark.docx");
```

### Siehe auch

* class [ImageWatermarkOptions](../../imagewatermarkoptions/)
* class [Watermark](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## SetImage(*Stream, [ImageWatermarkOptions](../../imagewatermarkoptions/)*) {#setimage_2}

Fügt dem Dokument ein Bildwasserzeichen hinzu.

```csharp
public void SetImage(Stream imageStream, ImageWatermarkOptions options)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| imageStream | Stream | Der Stream mit den Bilddaten, die als Wasserzeichen angezeigt werden. |
| options | ImageWatermarkOptions | Definiert zusätzliche Optionen für das Bildwasserzeichen. |

### Ausnahmen

| Ausnahme | Bedingung |
| --- | --- |
| ArgumentNullException | Wirft, wenn der Pfad`null` . |

## Bemerkungen

Wenn[`ImageWatermarkOptions`](../../imagewatermarkoptions/) Ist`null`, das Wasserzeichen wird mit den Standardoptionen gesetzt.

## Beispiele

Zeigt, wie aus einem Bildstream ein Wasserzeichen erstellt wird.

```csharp
Document doc = new Document();

// Ändern Sie das Erscheinungsbild des Bildwasserzeichens mit einem ImageWatermarkOptions-Objekt.
// und übergeben Sie es dann beim Erstellen eines Wasserzeichens aus einer Bilddatei.
ImageWatermarkOptions imageWatermarkOptions = new ImageWatermarkOptions();
imageWatermarkOptions.Scale = 5;

using (FileStream imageStream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open, FileAccess.Read))
    doc.Watermark.SetImage(imageStream, imageWatermarkOptions);

doc.Save(ArtifactsDir + "Document.ImageWatermarkStream.docx");
```

### Siehe auch

* class [ImageWatermarkOptions](../../imagewatermarkoptions/)
* class [Watermark](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
