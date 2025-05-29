---
title: DocumentBuilder.InsertOnlineVideo
linktitle: InsertOnlineVideo
articleTitle: InsertOnlineVideo
second_title: Aspose.Words för .NET
description: Lägg enkelt till och skala onlinevideor i dina dokument med DocumentBuilders InsertOnlineVideo-metod för ökat engagemang och kreativitet.
type: docs
weight: 440
url: /sv/net/aspose.words/documentbuilder/insertonlinevideo/
---
## InsertOnlineVideo(*string, [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../../aspose.words.drawing/wraptype/)*) {#insertonlinevideo}

Infogar ett onlinevideoobjekt i dokumentet och skalar det till den angivna storleken.

```csharp
public Shape InsertOnlineVideo(string videoUrl, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| videoUrl | String | URL:en till videon. |
| horzPos | RelativeHorizontalPosition | Anger varifrån avståndet till bilden mäts. |
| left | Double | Avstånd i punkter från origo till bildens vänstra sida. |
| vertPos | RelativeVerticalPosition | Anger varifrån avståndet till bilden mäts. |
| top | Double | Avstånd i punkter från origo till bildens översida. |
| width | Double | Bildens bredd i punkter. Kan vara ett negativt eller nollvärde för att begära 100 % skala. |
| height | Double | Bildens höjd i punkter. Kan vara ett negativt eller nollvärde för att begära 100 % skala. |
| wrapType | WrapType | Anger hur text ska radbrytas runt bilden. |

### Returvärde

Bildnoden som just infogades.

## Anmärkningar

Du kan ändra bildstorlek, plats, positioneringsmetod och andra inställningar med hjälp av [`Shape`](../../../aspose.words.drawing/shape/) objekt som returneras av den här metoden.

Insättning av onlinevideo från följande resurser stöds:

* https://www.youtube.com/
* https://vimeo.com/

Om din onlinevideo inte visas korrekt, använd`InsertOnlineVideo`, som accepterar anpassad inbäddad HTML-kod.

Koden för att bädda in video kan variera mellan leverantörer, kontakta din valda leverantör för mer information.

## Exempel

Visar hur man infogar en onlinevideo i ett dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string videoUrl = "https://vimeo.com/52477838";

// Infoga en form som spelar upp en video från webben när man klickar på den i Microsoft Word.
// Denna rektangulära form kommer att innehålla en bild baserad på den första bildrutan i den länkade videon
// och en visuell uppmaning med en "uppspelningsknapp". Videon har ett bildförhållande på 16:9.
// Vi ställer in formens storlek på det förhållandet, så att bilden inte verkar utsträckt.
builder.InsertOnlineVideo(videoUrl, RelativeHorizontalPosition.LeftMargin, 0,
    RelativeVerticalPosition.TopMargin, 0, 320, 180, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOnlineVideo.docx");
```

### Se även

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## InsertOnlineVideo(*string, string, byte[], double, double*) {#insertonlinevideo_3}

Infogar ett onlinevideoobjekt i dokumentet och skalar det till den angivna storleken.

```csharp
public Shape InsertOnlineVideo(string videoUrl, string videoEmbedCode, byte[] thumbnailImageBytes, 
    double width, double height)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| videoUrl | String | URL:en till videon. |
| videoEmbedCode | String | Inbäddningskoden för videon. |
| thumbnailImageBytes | Byte[] | Miniatyrbildens byte. |
| width | Double | Bildens bredd i punkter. Kan vara ett negativt eller nollvärde för att begära 100 % skala. |
| height | Double | Bildens höjd i punkter. Kan vara ett negativt eller nollvärde för att begära 100 % skala. |

### Returvärde

Bildnoden som just infogades.

## Anmärkningar

Du kan ändra bildstorlek, plats, positioneringsmetod och andra inställningar med hjälp av [`Shape`](../../../aspose.words.drawing/shape/) objekt som returneras av den här metoden.

## Exempel

Visar hur man infogar en onlinevideo i ett dokument med en anpassad miniatyrbild.

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
        // Nedan följer två sätt att skapa en form med en anpassad miniatyrbild, som länkar till en onlinevideo
        // som spelas upp när vi klickar på formen i Microsoft Word.
        // 1 - Infoga en inbäddad form vid byggarens nodinsättningsmarkör:
        builder.InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes, image.Width, image.Height);

        builder.InsertBreak(BreakType.PageBreak);

        // 2 - Infoga en flytande form:
        double left = builder.PageSetup.RightMargin - image.Width;
        double top = builder.PageSetup.BottomMargin - image.Height;

        builder.InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes,
            RelativeHorizontalPosition.RightMargin, left, RelativeVerticalPosition.BottomMargin, top,
            image.Width, image.Height, WrapType.Square);
    }
}

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOnlineVideoCustomThumbnail.docx");
```

### Se även

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## InsertOnlineVideo(*string, string, byte[], [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../../aspose.words.drawing/wraptype/)*) {#insertonlinevideo_2}

Infogar ett onlinevideoobjekt i dokumentet och skalar det till den angivna storleken.

```csharp
public Shape InsertOnlineVideo(string videoUrl, string videoEmbedCode, byte[] thumbnailImageBytes, 
    RelativeHorizontalPosition horzPos, double left, RelativeVerticalPosition vertPos, double top, 
    double width, double height, WrapType wrapType)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| videoUrl | String | URL:en till videon. |
| videoEmbedCode | String | Inbäddningskoden för videon. |
| thumbnailImageBytes | Byte[] | Miniatyrbildens byte. |
| horzPos | RelativeHorizontalPosition | Anger varifrån avståndet till bilden mäts. |
| left | Double | Avstånd i punkter från origo till bildens vänstra sida. |
| vertPos | RelativeVerticalPosition | Anger varifrån avståndet till bilden mäts. |
| top | Double | Avstånd i punkter från origo till bildens översida. |
| width | Double | Bildens bredd i punkter. Kan vara ett negativt eller nollvärde för att begära 100 % skala. |
| height | Double | Bildens höjd i punkter. Kan vara ett negativt eller nollvärde för att begära 100 % skala. |
| wrapType | WrapType | Anger hur text ska radbrytas runt bilden. |

### Returvärde

Bildnoden som just infogades.

## Anmärkningar

Du kan ändra bildstorlek, plats, positioneringsmetod och andra inställningar med hjälp av [`Shape`](../../../aspose.words.drawing/shape/) objekt som returneras av den här metoden.

## Exempel

Visar hur man infogar en onlinevideo i ett dokument med en anpassad miniatyrbild.

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
        // Nedan följer två sätt att skapa en form med en anpassad miniatyrbild, som länkar till en onlinevideo
        // som spelas upp när vi klickar på formen i Microsoft Word.
        // 1 - Infoga en inbäddad form vid byggarens nodinsättningsmarkör:
        builder.InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes, image.Width, image.Height);

        builder.InsertBreak(BreakType.PageBreak);

        // 2 - Infoga en flytande form:
        double left = builder.PageSetup.RightMargin - image.Width;
        double top = builder.PageSetup.BottomMargin - image.Height;

        builder.InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes,
            RelativeHorizontalPosition.RightMargin, left, RelativeVerticalPosition.BottomMargin, top,
            image.Width, image.Height, WrapType.Square);
    }
}

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOnlineVideoCustomThumbnail.docx");
```

### Se även

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## InsertOnlineVideo(*string, double, double*) {#insertonlinevideo_1}

Infogar ett onlinevideoobjekt i dokumentet och skalar det till den angivna storleken.

```csharp
public Shape InsertOnlineVideo(string videoUrl, double width, double height)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| videoUrl | String | URL:en till videon. |
| width | Double | Bildens bredd i punkter. Kan vara ett negativt eller nollvärde för att begära 100 % skala. |
| height | Double | Bildens höjd i punkter. Kan vara ett negativt eller nollvärde för att begära 100 % skala. |

### Returvärde

Bildnoden som just infogades.

## Anmärkningar

Du kan ändra bildstorlek, plats, positioneringsmetod och andra inställningar med hjälp av [`Shape`](../../../aspose.words.drawing/shape/) objekt som returneras av den här metoden.

Insättning av onlinevideo från följande resurser stöds:

* https://www.youtube.com/
* https://vimeo.com/

Om din onlinevideo inte visas korrekt, använd`InsertOnlineVideo`, som accepterar anpassad inbäddad HTML-kod.

Koden för att bädda in video kan variera mellan leverantörer, kontakta din valda leverantör för mer information.

## Exempel

Visar hur man infogar en onlinevideo i ett dokument med hjälp av en URL.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertOnlineVideo("https://youtu.be/g1N9ke8Prmk", 360, 270);

// Vi kan titta på videon från Microsoft Word genom att klicka på formen.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertVideoWithUrl.docx");
```

### Se även

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
