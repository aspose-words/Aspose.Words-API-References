---
title: InsertOnlineVideo
second_title: Aspose.Words für .NET-API-Referenz
description: Fügt ein OnlineVideoobjekt in das Dokument ein und skaliert es auf die angegebene Größe.
type: docs
weight: 390
url: /de/net/aspose.words/documentbuilder/insertonlinevideo/
---
## InsertOnlineVideo(string, double, double) {#insertonlinevideo_1}

Fügt ein Online-Videoobjekt in das Dokument ein und skaliert es auf die angegebene Größe.

```csharp
public Shape InsertOnlineVideo(string videoUrl, double width, double height)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| videoUrl | String | Die URL zum Video. |
| width | Double | Die Breite des Bildes in Punkt. Kann ein negativer oder Nullwert sein, um eine Skalierung von 100 % anzufordern. |
| height | Double | Die Höhe des Bildes in Punkten. Kann ein negativer oder Nullwert sein, um eine Skalierung von 100 % anzufordern. |

### Rückgabewert

Der gerade eingefügte Bildknoten.

### Bemerkungen

Sie können die Bildgröße, Position, Positionierungsmethode und andere Einstellungen mit dem ändern.[`Shape`](../../../aspose.words.drawing/shape/) Objekt, das von dieser Methode zurückgegeben wird.

Das Einfügen von Onlinevideos aus den folgenden Ressourcen wird unterstützt:

* https://www.youtube.com/
* https://vimeo.com/

Wenn Ihr Online-Video nicht richtig angezeigt wird, verwenden Sie`InsertOnlineVideo`, die benutzerdefinierten eingebetteten HTML-Code akzeptiert.

Der Code zum Einbetten von Videos kann je nach Anbieter variieren, wenden Sie sich für Einzelheiten an Ihren entsprechenden Anbieter Ihrer Wahl.

### Beispiele

Zeigt, wie Sie ein Online-Video mithilfe einer URL in ein Dokument einfügen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertOnlineVideo("https://youtu.be/t_1LYZ102RA", 360, 270);

// Wir können das Video von Microsoft Word ansehen, indem wir auf die Form klicken.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertVideoWithUrl.docx");
```

### Siehe auch

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../documentbuilder/)
* Montage [Aspose.Words](../../../)

---

## InsertOnlineVideo(string, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) {#insertonlinevideo}

Fügt ein Online-Videoobjekt in das Dokument ein und skaliert es auf die angegebene Größe.

```csharp
public Shape InsertOnlineVideo(string videoUrl, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| videoUrl | String | Die URL zum Video. |
| horzPos | RelativeHorizontalPosition | Gibt an, von wo aus der Abstand zum Bild gemessen wird. |
| left | Double | Abstand in Punkten vom Ursprung zur linken Seite des Bildes. |
| vertPos | RelativeVerticalPosition | Gibt an, von wo aus der Abstand zum Bild gemessen wird. |
| top | Double | Abstand in Punkten vom Ursprung zur oberen Seite des Bildes. |
| width | Double | Die Breite des Bildes in Punkt. Kann ein negativer oder Nullwert sein, um eine Skalierung von 100 % anzufordern. |
| height | Double | Die Höhe des Bildes in Punkten. Kann ein negativer oder Nullwert sein, um eine Skalierung von 100 % anzufordern. |
| wrapType | WrapType | Gibt an, wie Text um das Bild herumgeführt wird. |

### Rückgabewert

Der gerade eingefügte Bildknoten.

### Bemerkungen

Sie können die Bildgröße, Position, Positionierungsmethode und andere Einstellungen mit dem ändern.[`Shape`](../../../aspose.words.drawing/shape/) Objekt, das von dieser Methode zurückgegeben wird.

Das Einfügen von Onlinevideos aus den folgenden Ressourcen wird unterstützt:

* https://www.youtube.com/
* https://vimeo.com/

Wenn Ihr Online-Video nicht richtig angezeigt wird, verwenden Sie`InsertOnlineVideo`, die benutzerdefinierten eingebetteten HTML-Code akzeptiert.

Der Code zum Einbetten von Videos kann je nach Anbieter variieren, wenden Sie sich für Einzelheiten an Ihren entsprechenden Anbieter Ihrer Wahl.

### Beispiele

Zeigt, wie Sie ein Online-Video in ein Dokument einfügen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string videoUrl = "https://vimeo.com/52477838";

// Fügen Sie eine Form ein, die ein Video aus dem Internet abspielt, wenn Sie in Microsoft Word darauf klicken.
// Diese rechteckige Form enthält ein Bild, das auf dem ersten Frame des verknüpften Videos basiert
// und eine visuelle Aufforderung "Play-Button". Das Video hat ein Seitenverhältnis von 16:9.
// Wir werden die Größe der Form auf dieses Verhältnis setzen, damit das Bild nicht gestreckt erscheint.
builder.InsertOnlineVideo(videoUrl, RelativeHorizontalPosition.LeftMargin, 0,
    RelativeVerticalPosition.TopMargin, 0, 320, 180, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOnlineVideo.docx");
```

### Siehe auch

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../documentbuilder/)
* Montage [Aspose.Words](../../../)

---

## InsertOnlineVideo(string, string, byte[], double, double) {#insertonlinevideo_3}

Fügt ein Online-Videoobjekt in das Dokument ein und skaliert es auf die angegebene Größe.

```csharp
public Shape InsertOnlineVideo(string videoUrl, string videoEmbedCode, byte[] thumbnailImageBytes, 
    double width, double height)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| videoUrl | String | Die URL zum Video. |
| videoEmbedCode | String | Der Einbettungscode für das Video. |
| thumbnailImageBytes | Byte[] | Die Miniaturbildbytes. |
| width | Double | Die Breite des Bildes in Punkt. Kann ein negativer oder Nullwert sein, um eine Skalierung von 100 % anzufordern. |
| height | Double | Die Höhe des Bildes in Punkten. Kann ein negativer oder Nullwert sein, um eine Skalierung von 100 % anzufordern. |

### Rückgabewert

Der gerade eingefügte Bildknoten.

### Bemerkungen

Sie können die Bildgröße, Position, Positionierungsmethode und andere Einstellungen mit dem ändern.[`Shape`](../../../aspose.words.drawing/shape/) Objekt, das von dieser Methode zurückgegeben wird.

### Beispiele

Zeigt, wie Sie ein Online-Video mit einer benutzerdefinierten Miniaturansicht in ein Dokument einfügen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string videoUrl = "https://vimeo.com/52477838";
string videoEmbedCode =
    "<iframe src=\"https://player.vimeo.com/video/52477838\" width=\"640\" height=\"360\" frameborder=\"0\" " +
    "title=\"Aspose\" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>";

byte[] thumbnailImageBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");

using (MemoryStream stream = new MemoryStream(thumbnailImageBytes))
{
    using (Image image = Image.FromStream(stream))
    {
        // Im Folgenden finden Sie zwei Möglichkeiten zum Erstellen einer Form mit einem benutzerdefinierten Miniaturbild, das mit einem Online-Video verknüpft ist
        // das wird abgespielt, wenn wir in Microsoft Word auf die Form klicken.
        // 1 - Fügen Sie eine Inline-Form am Einfügecursor des Builder-Knotens ein:
        builder.InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes, image.Width, image.Height);

        builder.InsertBreak(BreakType.PageBreak);

        // 2 - Fügen Sie eine schwebende Form ein:
        double left = builder.PageSetup.RightMargin - image.Width;
        double top = builder.PageSetup.BottomMargin - image.Height;

        builder.InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes,
            RelativeHorizontalPosition.RightMargin, left, RelativeVerticalPosition.BottomMargin, top,
            image.Width, image.Height, WrapType.Square);
    }
}

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOnlineVideoCustomThumbnail.docx");
```

### Siehe auch

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../documentbuilder/)
* Montage [Aspose.Words](../../../)

---

## InsertOnlineVideo(string, string, byte[], RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) {#insertonlinevideo_2}

Fügt ein Online-Videoobjekt in das Dokument ein und skaliert es auf die angegebene Größe.

```csharp
public Shape InsertOnlineVideo(string videoUrl, string videoEmbedCode, byte[] thumbnailImageBytes, 
    RelativeHorizontalPosition horzPos, double left, RelativeVerticalPosition vertPos, double top, 
    double width, double height, WrapType wrapType)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| videoUrl | String | Die URL zum Video. |
| videoEmbedCode | String | Der Einbettungscode für das Video. |
| thumbnailImageBytes | Byte[] | Die Miniaturbildbytes. |
| horzPos | RelativeHorizontalPosition | Gibt an, von wo aus der Abstand zum Bild gemessen wird. |
| left | Double | Abstand in Punkten vom Ursprung zur linken Seite des Bildes. |
| vertPos | RelativeVerticalPosition | Gibt an, von wo aus der Abstand zum Bild gemessen wird. |
| top | Double | Abstand in Punkten vom Ursprung zur oberen Seite des Bildes. |
| width | Double | Die Breite des Bildes in Punkt. Kann ein negativer oder Nullwert sein, um eine Skalierung von 100 % anzufordern. |
| height | Double | Die Höhe des Bildes in Punkten. Kann ein negativer oder Nullwert sein, um eine Skalierung von 100 % anzufordern. |
| wrapType | WrapType | Gibt an, wie Text um das Bild herumgeführt wird. |

### Rückgabewert

Der gerade eingefügte Bildknoten.

### Bemerkungen

Sie können die Bildgröße, Position, Positionierungsmethode und andere Einstellungen mit dem ändern.[`Shape`](../../../aspose.words.drawing/shape/) Objekt, das von dieser Methode zurückgegeben wird.

### Beispiele

Zeigt, wie Sie ein Online-Video mit einer benutzerdefinierten Miniaturansicht in ein Dokument einfügen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string videoUrl = "https://vimeo.com/52477838";
string videoEmbedCode =
    "<iframe src=\"https://player.vimeo.com/video/52477838\" width=\"640\" height=\"360\" frameborder=\"0\" " +
    "title=\"Aspose\" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>";

byte[] thumbnailImageBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");

using (MemoryStream stream = new MemoryStream(thumbnailImageBytes))
{
    using (Image image = Image.FromStream(stream))
    {
        // Im Folgenden finden Sie zwei Möglichkeiten zum Erstellen einer Form mit einem benutzerdefinierten Miniaturbild, das mit einem Online-Video verknüpft ist
        // das wird abgespielt, wenn wir in Microsoft Word auf die Form klicken.
        // 1 - Fügen Sie eine Inline-Form am Einfügecursor des Builder-Knotens ein:
        builder.InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes, image.Width, image.Height);

        builder.InsertBreak(BreakType.PageBreak);

        // 2 - Fügen Sie eine schwebende Form ein:
        double left = builder.PageSetup.RightMargin - image.Width;
        double top = builder.PageSetup.BottomMargin - image.Height;

        builder.InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes,
            RelativeHorizontalPosition.RightMargin, left, RelativeVerticalPosition.BottomMargin, top,
            image.Width, image.Height, WrapType.Square);
    }
}

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOnlineVideoCustomThumbnail.docx");
```

### Siehe auch

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../documentbuilder/)
* Montage [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
