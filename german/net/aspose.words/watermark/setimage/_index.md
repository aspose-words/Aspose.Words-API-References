---
title: Watermark.SetImage
second_title: Aspose.Words für .NET-API-Referenz
description: Watermark methode. Fügt dem Dokument ein Bildwasserzeichen hinzu.
type: docs
weight: 30
url: /de/net/aspose.words/watermark/setimage/
---
## SetImage(Image) {#setimage}

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
| ArgumentNullException | Wird ausgelöst, wenn das Bild vorhanden ist`Null` . |

### Siehe auch

* class [Watermark](../)
* namensraum [Aspose.Words](../../watermark/)
* Montage [Aspose.Words](../../../)

---

## SetImage(Image, ImageWatermarkOptions) {#setimage_1}

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
| ArgumentNullException | Wird ausgelöst, wenn das Bild vorhanden ist`Null` . |

### Bemerkungen

Wenn[`ImageWatermarkOptions`](../../imagewatermarkoptions/) Ist`Null`, das Wasserzeichen wird mit Standardoptionen eingestellt.

### Beispiele

Zeigt, wie man aus einem Bild im lokalen Dateisystem ein Wasserzeichen erstellt.

```csharp
Document doc = new Document();

            // Ändern Sie das Erscheinungsbild des Bildwasserzeichens mit einem ImageWatermarkOptions-Objekt.
            // Übergebe es dann beim Erstellen eines Wasserzeichens aus einer Bilddatei.
            ImageWatermarkOptions imageWatermarkOptions = new ImageWatermarkOptions();
            imageWatermarkOptions.Scale = 5;
            imageWatermarkOptions.IsWashout = false;

#if NET48 || JAVA
            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"), imageWatermarkOptions);
#elif NET5_0_OR_GREATER || __MOBILE__
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
* namensraum [Aspose.Words](../../watermark/)
* Montage [Aspose.Words](../../../)

---

## SetImage(string, ImageWatermarkOptions) {#setimage_2}

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
| ArgumentNullException | Wird ausgelöst, wenn der Pfad vorhanden ist`Null` . |

### Bemerkungen

Wenn[`ImageWatermarkOptions`](../../imagewatermarkoptions/) Ist`Null`, das Wasserzeichen wird mit Standardoptionen eingestellt.

### Siehe auch

* class [ImageWatermarkOptions](../../imagewatermarkoptions/)
* class [Watermark](../)
* namensraum [Aspose.Words](../../watermark/)
* Montage [Aspose.Words](../../../)


