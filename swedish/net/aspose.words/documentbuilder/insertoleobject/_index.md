---
title: DocumentBuilder.InsertOleObject
second_title: Aspose.Words för .NET API Referens
description: DocumentBuilder metod. Infogar ett inbäddat OLEobjekt från en ström i dokumentet.
type: docs
weight: 400
url: /sv/net/aspose.words/documentbuilder/insertoleobject/
---
## InsertOleObject(Stream, string, bool, Stream) {#insertoleobject}

Infogar ett inbäddat OLE-objekt från en ström i dokumentet.

```csharp
public Shape InsertOleObject(Stream stream, string progId, bool asIcon, Stream presentation)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| stream | Stream | Ström som innehåller applikationsdata. |
| progId | String | Programmatisk identifierare för OLE-objekt. |
| asIcon | Boolean | Anger antingen ikoniskt eller normalt läge för OLE-objekt som infogas. |
| presentation | Stream | Bildpresentation av OLE-objekt. Om värdet är`null` Aspose.Words kommer att använda en av de fördefinierade bilderna. |

### Returvärde

Formnod som innehåller Ole-objektet och infogat vid den aktuella Builder-positionen.

### Exempel

Visar hur man använder dokumentbyggaren för att bädda in OLE-objekt i ett dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga ett Microsoft Excel-kalkylblad från det lokala filsystemet
// i dokumentet samtidigt som det behåller dess standardutseende.
using (Stream spreadsheetStream = File.Open(MyDir + "Spreadsheet.xlsx", FileMode.Open))
{
    builder.Writeln("Spreadsheet Ole object:");
    // Om 'presentation' utelämnas och 'asIcon' är inställd, väljs denna överbelastade metod
    // ikonen enligt 'progId' och använder den fördefinierade ikontexten.
    builder.InsertOleObject(spreadsheetStream, "OleObject.xlsx", false, null);
}

// Infoga en Microsoft Powerpoint-presentation som ett OLE-objekt.
// Den här gången kommer en bild att laddas ner från webben för en ikon.
using (Stream powerpointStream = File.Open(MyDir + "Presentation.pptx", FileMode.Open))
{
    using (HttpClient httpClient = new HttpClient())
    {
        byte[] imgBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");

        using (MemoryStream imageStream = new MemoryStream(imgBytes))
        {
            builder.InsertParagraph();
            builder.Writeln("Powerpoint Ole object:");
            builder.InsertOleObject(powerpointStream, "OleObject.pptx", true, imageStream);
        }
    }
}

// Dubbelklicka på dessa objekt i Microsoft Word för att öppna
// de länkade filerna med sina respektive program.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertOleObjects.docx");
```

### Se även

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../documentbuilder/)
* hopsättning [Aspose.Words](../../../)

---

## InsertOleObject(string, bool, bool, Stream) {#insertoleobject_1}

Infogar ett inbäddat eller länkat OLE-objekt från en fil i dokumentet. Upptäcker OLE-objekttyp med filtillägg.

```csharp
public Shape InsertOleObject(string fileName, bool isLinked, bool asIcon, Stream presentation)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fileName | String | Fullständig sökväg till filen. |
| isLinked | Boolean | Om`Sann` sedan infogas länkat OLE-objekt annars infogas inbäddat OLE-objekt. |
| asIcon | Boolean | Anger antingen ikoniskt eller normalt läge för OLE-objekt som infogas. |
| presentation | Stream | Bildpresentation av OLE-objekt. Om värdet är`null` Aspose.Words kommer att använda en av de fördefinierade bilderna. |

### Returvärde

Formnod som innehåller Ole-objektet och infogat vid den aktuella Builder-positionen.

### Exempel

Visar hur man infogar ett OLE-objekt i ett dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// OLE-objekt är länkar till filer i vårt lokala filsystem som kan öppnas av andra installerade applikationer.
// Dubbelklicka på dessa former startar programmet och använd det sedan för att öppna det länkade objektet.
// Det finns tre sätt att använda metoden InsertOleObject för att infoga dessa former och konfigurera deras utseende.
// 1 - Bild tagen från det lokala filsystemet:
using (FileStream imageStream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open))
{
    // Om 'presentation' utelämnas och 'asIcon' är inställd, väljs denna överbelastade metod
    // ikonen enligt filtillägget och använder filnamnet för ikontexten.
    builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", false, false, imageStream); 
}

// Om 'presentation' utelämnas och 'asIcon' är inställd, väljs denna överbelastade metod
// ikonen enligt 'progId' och använder filnamnet för ikontexten.
// 2 - Ikon baserad på programmet som öppnar objektet:
builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", "Excel.Sheet", false, true, null);

// Om 'iconFile' och 'iconCaption' utelämnas, väljer denna överbelastade metod
// ikonen enligt 'progId' och använder den fördefinierade ikontexten.
// 3 - Bildikon som är 32 x 32 pixlar eller mindre från det lokala filsystemet, med en anpassad bildtext:
builder.InsertOleObjectAsIcon(MyDir + "Presentation.pptx", false, ImageDir + "Logo icon.ico",
    "Double click to view presentation!");

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOleObject.docx");
```

### Se även

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../documentbuilder/)
* hopsättning [Aspose.Words](../../../)

---

## InsertOleObject(string, string, bool, bool, Stream) {#insertoleobject_2}

Infogar ett inbäddat eller länkat OLE-objekt från en fil i dokumentet. Upptäcker OLE-objekttyp med hjälp av given progID-parameter.

```csharp
public Shape InsertOleObject(string fileName, string progId, bool isLinked, bool asIcon, 
    Stream presentation)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fileName | String | Fullständig sökväg till filen. |
| progId | String | ProgId för OLE-objekt. |
| isLinked | Boolean | Om`Sann` sedan infogas länkat OLE-objekt annars infogas inbäddat OLE-objekt. |
| asIcon | Boolean | Anger antingen ikoniskt eller normalt läge för OLE-objekt som infogas. |
| presentation | Stream | Bildpresentation av OLE-objekt. Om värdet är`null` Aspose.Words kommer att använda en av de fördefinierade bilderna. |

### Returvärde

Formnod som innehåller Ole-objektet och infogat vid den aktuella Builder-positionen.

### Exempel

Visar hur man infogar ett OLE-objekt i ett dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// OLE-objekt är länkar till filer i vårt lokala filsystem som kan öppnas av andra installerade applikationer.
// Dubbelklicka på dessa former startar programmet och använd det sedan för att öppna det länkade objektet.
// Det finns tre sätt att använda metoden InsertOleObject för att infoga dessa former och konfigurera deras utseende.
// 1 - Bild tagen från det lokala filsystemet:
using (FileStream imageStream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open))
{
    // Om 'presentation' utelämnas och 'asIcon' är inställd, väljs denna överbelastade metod
    // ikonen enligt filtillägget och använder filnamnet för ikontexten.
    builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", false, false, imageStream); 
}

// Om 'presentation' utelämnas och 'asIcon' är inställd, väljs denna överbelastade metod
// ikonen enligt 'progId' och använder filnamnet för ikontexten.
// 2 - Ikon baserad på programmet som öppnar objektet:
builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", "Excel.Sheet", false, true, null);

// Om 'iconFile' och 'iconCaption' utelämnas, väljer denna överbelastade metod
// ikonen enligt 'progId' och använder den fördefinierade ikontexten.
// 3 - Bildikon som är 32 x 32 pixlar eller mindre från det lokala filsystemet, med en anpassad bildtext:
builder.InsertOleObjectAsIcon(MyDir + "Presentation.pptx", false, ImageDir + "Logo icon.ico",
    "Double click to view presentation!");

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOleObject.docx");
```

### Se även

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../documentbuilder/)
* hopsättning [Aspose.Words](../../../)


