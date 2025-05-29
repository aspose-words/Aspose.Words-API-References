---
title: DocumentBuilder.InsertOnlineVideo
linktitle: InsertOnlineVideo
articleTitle: InsertOnlineVideo
second_title: Aspose.Words für .NET
description: Fügen Sie mit der InsertOnlineVideo-Methode von DocumentBuilder mühelos Onlinevideos in Ihre Dokumente ein und skalieren Sie sie, um die Interaktion und Kreativität zu steigern.
type: docs
weight: 440
url: /de/net/aspose.words/documentbuilder/insertonlinevideo/
---
## InsertOnlineVideo(*string, [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../../aspose.words.drawing/wraptype/)*) {#insertonlinevideo}

Fügt ein Online-Videoobjekt in das Dokument ein und skaliert es auf die angegebene Größe.

```csharp
public Shape InsertOnlineVideo(string videoUrl, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| videoUrl | String | Die URL zum Video. |
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

Das Einfügen von Online-Videos aus den folgenden Quellen wird unterstützt:

* https://www.youtube.com/
* https://vimeo.com/

Wenn Ihr Online-Video nicht richtig angezeigt wird, verwenden Sie`InsertOnlineVideo`, das benutzerdefinierten eingebetteten HTML-Code akzeptiert.

Der Code zum Einbetten von Videos kann je nach Anbieter unterschiedlich sein. Einzelheiten erfahren Sie bei Ihrem jeweiligen Anbieter.

## Beispiele

Zeigt, wie ein Onlinevideo in ein Dokument eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string videoUrl = "https://vimeo.com/52477838";

// Fügen Sie eine Form ein, die beim Anklicken in Microsoft Word ein Video aus dem Internet abspielt.
// Diese rechteckige Form enthält ein Bild basierend auf dem ersten Frame des verknüpften Videos
// und eine visuelle Aufforderung mit der Wiedergabetaste. Das Video hat ein Seitenverhältnis von 16:9.
// Wir werden die Größe der Form auf dieses Verhältnis einstellen, damit das Bild nicht gestreckt erscheint.
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
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## InsertOnlineVideo(*string, string, byte[], double, double*) {#insertonlinevideo_3}

Fügt ein Online-Videoobjekt in das Dokument ein und skaliert es auf die angegebene Größe.

```csharp
public Shape InsertOnlineVideo(string videoUrl, string videoEmbedCode, byte[] thumbnailImageBytes, 
    double width, double height)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| videoUrl | String | Die URL zum Video. |
| videoEmbedCode | String | Der Einbettungscode für das Video. |
| thumbnailImageBytes | Byte[] | Die Bytes der Miniaturansicht. |
| width | Double | Die Breite des Bildes in Punkten. Kann ein negativer oder Nullwert sein, um eine Skalierung von 100 % anzufordern. |
| height | Double | Die Höhe des Bildes in Punkten. Kann ein negativer oder Nullwert sein, um eine Skalierung von 100 % anzufordern. |

### Rückgabewert

Der Bildknoten, der gerade eingefügt wurde.

## Bemerkungen

Sie können die Bildgröße, den Speicherort, die Positionierungsmethode und andere Einstellungen mit dem ändern.[`Shape`](../../../aspose.words.drawing/shape/) von dieser Methode zurückgegebenes Objekt.

## Beispiele

Zeigt, wie Sie ein Onlinevideo mit einer benutzerdefinierten Miniaturansicht in ein Dokument einfügen.

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
        // Unten sind zwei Möglichkeiten zum Erstellen einer Form mit einem benutzerdefinierten Miniaturbild, das auf ein Online-Video verweist
        // das abgespielt wird, wenn wir in Microsoft Word auf die Form klicken.
        // 1 – Fügen Sie am Knoteneinfügecursor des Builders eine Inline-Form ein:
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
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## InsertOnlineVideo(*string, string, byte[], [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../../aspose.words.drawing/wraptype/)*) {#insertonlinevideo_2}

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
| thumbnailImageBytes | Byte[] | Die Bytes der Miniaturansicht. |
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

Zeigt, wie Sie ein Onlinevideo mit einer benutzerdefinierten Miniaturansicht in ein Dokument einfügen.

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
        // Unten sind zwei Möglichkeiten zum Erstellen einer Form mit einem benutzerdefinierten Miniaturbild, das auf ein Online-Video verweist
        // das abgespielt wird, wenn wir in Microsoft Word auf die Form klicken.
        // 1 – Fügen Sie am Knoteneinfügecursor des Builders eine Inline-Form ein:
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
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## InsertOnlineVideo(*string, double, double*) {#insertonlinevideo_1}

Fügt ein Online-Videoobjekt in das Dokument ein und skaliert es auf die angegebene Größe.

```csharp
public Shape InsertOnlineVideo(string videoUrl, double width, double height)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| videoUrl | String | Die URL zum Video. |
| width | Double | Die Breite des Bildes in Punkten. Kann ein negativer oder Nullwert sein, um eine Skalierung von 100 % anzufordern. |
| height | Double | Die Höhe des Bildes in Punkten. Kann ein negativer oder Nullwert sein, um eine Skalierung von 100 % anzufordern. |

### Rückgabewert

Der Bildknoten, der gerade eingefügt wurde.

## Bemerkungen

Sie können die Bildgröße, den Speicherort, die Positionierungsmethode und andere Einstellungen mit dem ändern.[`Shape`](../../../aspose.words.drawing/shape/) von dieser Methode zurückgegebenes Objekt.

Das Einfügen von Online-Videos aus den folgenden Quellen wird unterstützt:

* https://www.youtube.com/
* https://vimeo.com/

Wenn Ihr Online-Video nicht richtig angezeigt wird, verwenden Sie`InsertOnlineVideo`, das benutzerdefinierten eingebetteten HTML-Code akzeptiert.

Der Code zum Einbetten von Videos kann je nach Anbieter unterschiedlich sein. Einzelheiten erfahren Sie bei Ihrem jeweiligen Anbieter.

## Beispiele

Zeigt, wie Sie mithilfe einer URL ein Onlinevideo in ein Dokument einfügen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertOnlineVideo("https://youtu.be/g1N9ke8Prmk", 360, 270);

// Wir können das Video von Microsoft Word aus ansehen, indem wir auf die Form klicken.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertVideoWithUrl.docx");
```

### Siehe auch

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
