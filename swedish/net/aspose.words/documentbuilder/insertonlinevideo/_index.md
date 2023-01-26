---
title: InsertOnlineVideo
second_title: Aspose.Words för .NET API Referens
description: Infogar ett onlinevideoobjekt i dokumentet och skalar det till den angivna storleken.
type: docs
weight: 390
url: /sv/net/aspose.words/documentbuilder/insertonlinevideo/
---
## InsertOnlineVideo(string, double, double) {#insertonlinevideo_1}

Infogar ett onlinevideoobjekt i dokumentet och skalar det till den angivna storleken.

```csharp
public Shape InsertOnlineVideo(string videoUrl, double width, double height)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| videoUrl | String | Webbadressen till videon. |
| width | Double | Bildens bredd i punkter. Kan vara ett negativt eller noll värde för att begära 100 % skala. |
| height | Double | Bildens höjd i punkter. Kan vara ett negativt eller noll värde för att begära 100 % skala. |

### Returvärde

Bildnoden som precis infogades.

### Anmärkningar

Du kan ändra bildstorlek, plats, positioneringsmetod och andra inställningar med hjälp av [`Shape`](../../../aspose.words.drawing/shape/) objekt som returneras med denna metod.

Infogning av onlinevideo från följande resurser stöds:

* https://www.youtube.com/
* https://vimeo.com/

Om din onlinevideo inte visas korrekt, använd`InsertOnlineVideo`, som accepterar anpassad inbäddad html-kod.

Koden för inbäddning av video kan variera mellan olika leverantörer, kontakta din motsvarande leverantör för mer information.

### Exempel

Visar hur man infogar en onlinevideo i ett dokument med hjälp av en URL.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertOnlineVideo("https://youtu.be/t_1LYZ102RA", 360, 270);

// Vi kan se videon från Microsoft Word genom att klicka på formen.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertVideoWithUrl.docx");
```

### Se även

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../documentbuilder/)
* hopsättning [Aspose.Words](../../../)

---

## InsertOnlineVideo(string, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) {#insertonlinevideo}

Infogar ett onlinevideoobjekt i dokumentet och skalar det till den angivna storleken.

```csharp
public Shape InsertOnlineVideo(string videoUrl, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| videoUrl | String | Webbadressen till videon. |
| horzPos | RelativeHorizontalPosition | Anger varifrån avståndet till bilden mäts. |
| left | Double | Avstånd i punkter från origo till vänster sida av bilden. |
| vertPos | RelativeVerticalPosition | Anger var avståndet till bilden mätt från. |
| top | Double | Avstånd i punkter från origo till bildens övre sida. |
| width | Double | Bildens bredd i punkter. Kan vara ett negativt eller noll värde för att begära 100 % skala. |
| height | Double | Bildens höjd i punkter. Kan vara ett negativt eller noll värde för att begära 100 % skala. |
| wrapType | WrapType | Anger hur text lindas runt bilden. |

### Returvärde

Bildnoden som precis infogades.

### Anmärkningar

Du kan ändra bildstorlek, plats, positioneringsmetod och andra inställningar med hjälp av [`Shape`](../../../aspose.words.drawing/shape/) objekt som returneras med denna metod.

Infogning av onlinevideo från följande resurser stöds:

* https://www.youtube.com/
* https://vimeo.com/

Om din onlinevideo inte visas korrekt, använd`InsertOnlineVideo`, som accepterar anpassad inbäddad html-kod.

Koden för inbäddning av video kan variera mellan olika leverantörer, kontakta din motsvarande leverantör för mer information.

### Exempel

Visar hur man infogar en onlinevideo i ett dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string videoUrl = "https://vimeo.com/52477838";

// Infoga en form som spelar upp en video från webben när den klickas i Microsoft Word.
// Den här rektangulära formen kommer att innehålla en bild baserad på den första bildrutan i den länkade videon
// och en visuell uppmaning av "spelaknapp". Videon har ett bildförhållande på 16:9.
// Vi kommer att ställa in formens storlek till det förhållandet, så att bilden inte ser utsträckt ut.
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
* namnutrymme [Aspose.Words](../../documentbuilder/)
* hopsättning [Aspose.Words](../../../)

---

## InsertOnlineVideo(string, string, byte[], double, double) {#insertonlinevideo_3}

Infogar ett onlinevideoobjekt i dokumentet och skalar det till den angivna storleken.

```csharp
public Shape InsertOnlineVideo(string videoUrl, string videoEmbedCode, byte[] thumbnailImageBytes, 
    double width, double height)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| videoUrl | String | Webbadressen till videon. |
| videoEmbedCode | String | Inbäddningskoden för videon. |
| thumbnailImageBytes | Byte[] | Miniatyrbilden bytes. |
| width | Double | Bildens bredd i punkter. Kan vara ett negativt eller noll värde för att begära 100 % skala. |
| height | Double | Bildens höjd i punkter. Kan vara ett negativt eller noll värde för att begära 100 % skala. |

### Returvärde

Bildnoden som precis infogades.

### Anmärkningar

Du kan ändra bildstorlek, plats, positioneringsmetod och andra inställningar med hjälp av [`Shape`](../../../aspose.words.drawing/shape/) objekt som returneras med denna metod.

### Exempel

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
        // Nedan finns två sätt att skapa en form med en anpassad miniatyrbild, som länkar till en onlinevideo
        // som kommer att spelas upp när vi klickar på formen i Microsoft Word.
        // 1 - Infoga en inline-form vid byggarens nodinfogningsmarkör:
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
* namnutrymme [Aspose.Words](../../documentbuilder/)
* hopsättning [Aspose.Words](../../../)

---

## InsertOnlineVideo(string, string, byte[], RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) {#insertonlinevideo_2}

Infogar ett onlinevideoobjekt i dokumentet och skalar det till den angivna storleken.

```csharp
public Shape InsertOnlineVideo(string videoUrl, string videoEmbedCode, byte[] thumbnailImageBytes, 
    RelativeHorizontalPosition horzPos, double left, RelativeVerticalPosition vertPos, double top, 
    double width, double height, WrapType wrapType)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| videoUrl | String | Webbadressen till videon. |
| videoEmbedCode | String | Inbäddningskoden för videon. |
| thumbnailImageBytes | Byte[] | Miniatyrbilden bytes. |
| horzPos | RelativeHorizontalPosition | Anger varifrån avståndet till bilden mäts. |
| left | Double | Avstånd i punkter från origo till vänster sida av bilden. |
| vertPos | RelativeVerticalPosition | Anger var avståndet till bilden mätt från. |
| top | Double | Avstånd i punkter från origo till bildens övre sida. |
| width | Double | Bildens bredd i punkter. Kan vara ett negativt eller noll värde för att begära 100 % skala. |
| height | Double | Bildens höjd i punkter. Kan vara ett negativt eller noll värde för att begära 100 % skala. |
| wrapType | WrapType | Anger hur text lindas runt bilden. |

### Returvärde

Bildnoden som precis infogades.

### Anmärkningar

Du kan ändra bildstorlek, plats, positioneringsmetod och andra inställningar med hjälp av [`Shape`](../../../aspose.words.drawing/shape/) objekt som returneras med denna metod.

### Exempel

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
        // Nedan finns två sätt att skapa en form med en anpassad miniatyrbild, som länkar till en onlinevideo
        // som kommer att spelas upp när vi klickar på formen i Microsoft Word.
        // 1 - Infoga en inline-form vid byggarens nodinfogningsmarkör:
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
* namnutrymme [Aspose.Words](../../documentbuilder/)
* hopsättning [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
