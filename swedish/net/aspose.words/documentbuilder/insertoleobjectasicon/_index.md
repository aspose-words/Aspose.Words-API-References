---
title: DocumentBuilder.InsertOleObjectAsIcon
linktitle: InsertOleObjectAsIcon
articleTitle: InsertOleObjectAsIcon
second_title: Aspose.Words för .NET
description: Infoga enkelt OLE-objekt som ikoner i dina dokument med DocumentBuilder. Anpassa ikoner och bildtexter samtidigt som du säkerställer sömlös integration.
type: docs
weight: 430
url: /sv/net/aspose.words/documentbuilder/insertoleobjectasicon/
---
## InsertOleObjectAsIcon(*string, bool, string, string*) {#insertoleobjectasicon_1}

Infogar ett inbäddat eller länkat OLE-objekt som ikon i dokumentet. Gör det möjligt att ange ikonfil och bildtext. Identifierar OLE-objekttyp med hjälp av filändelsen.

```csharp
public Shape InsertOleObjectAsIcon(string fileName, bool isLinked, string iconFile, 
    string iconCaption)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fileName | String | Fullständig sökväg till filen. |
| isLinked | Boolean | Om`sann` sedan infogas det länkade OLE-objektet, annars infogas det inbäddade OLE-objektet. |
| iconFile | String | Fullständig sökväg till ICO-filen. Om värdet är`null` Aspose.Words kommer att använda en fördefinierad bild. |
| iconCaption | String | Ikontext. Om värdet är`null` Aspose.Words kommer att använda filnamnet . |

### Returvärde

Formnod som innehåller Ole-objektet och infogas vid den aktuella Builder-positionen.

## Exempel

Visar hur man infogar ett OLE-objekt i ett dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// OLE-objekt är länkar till filer i vårt lokala filsystem som kan öppnas av andra installerade program.
// Dubbelklicka på dessa former för att starta applikationen och sedan använda den för att öppna det länkade objektet.
// Det finns tre sätt att använda InsertOleObject-metoden för att infoga dessa former och konfigurera deras utseende.
// 1 - Bild tagen från det lokala filsystemet:
using (FileStream imageStream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open))
{
    // Om 'presentation' utelämnas och 'asIcon' är satt, väljer denna överbelastade metod
    // ikonen enligt filändelsen och använder filnamnet som ikonens bildtext.
    builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", false, false, imageStream); 
}

// Om 'presentation' utelämnas och 'asIcon' är satt, väljer denna överbelastade metod
// ikonen enligt 'progId' och använder filnamnet som ikonens bildtext.
// 2 - Ikon baserad på applikationen som öppnar objektet:
builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", "Excel.Sheet", false, true, null);

// Om 'iconFile' och 'iconCaption' utelämnas, väljer denna överbelastade metod
// ikonen enligt 'progId' och använder den fördefinierade ikonbilden.
// 3 - Bildikon som är 32 x 32 pixlar eller mindre från det lokala filsystemet, med en anpassad bildtext:
builder.InsertOleObjectAsIcon(MyDir + "Presentation.pptx", false, ImageDir + "Logo icon.ico",
    "Double click to view presentation!");

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOleObject.docx");
```

### Se även

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## InsertOleObjectAsIcon(*string, string, bool, string, string*) {#insertoleobjectasicon_2}

Infogar ett inbäddat eller länkat OLE-objekt som ikon i dokumentet. Gör det möjligt att ange ikonfil och bildtext. Identifierar OLE-objekttyp med hjälp av given progID-parameter.

```csharp
public Shape InsertOleObjectAsIcon(string fileName, string progId, bool isLinked, string iconFile, 
    string iconCaption)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fileName | String | Fullständig sökväg till filen. |
| progId | String | ProgId för OLE-objekt. |
| isLinked | Boolean | Om`sann` sedan infogas det länkade OLE-objektet, annars infogas det inbäddade OLE-objektet. |
| iconFile | String | Fullständig sökväg till ICO-filen. Om värdet är`null` Aspose.Words kommer att använda en fördefinierad bild. |
| iconCaption | String | Ikontext. Om värdet är`null` Aspose.Words kommer att använda filnamnet . |

### Returvärde

Formnod som innehåller Ole-objektet och infogas vid den aktuella Builder-positionen.

## Exempel

Visar hur man infogar ett inbäddat eller länkat OLE-objekt som en ikon i dokumentet.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Om 'iconFile' och 'iconCaption' utelämnas, väljer denna överbelastade metod
// ikonen enligt 'progId' och använder filnamnet som ikonens bildtext.
builder.InsertOleObjectAsIcon(MyDir + "Presentation.pptx", "Package", false, ImageDir + "Logo icon.ico", "My embedded file");

builder.InsertBreak(BreakType.LineBreak);

using (FileStream stream = new FileStream(MyDir + "Presentation.pptx", FileMode.Open))
{
    // Om 'iconFile' och 'iconCaption' utelämnas, väljer denna överbelastade metod
    // ikonen enligt filändelsen och använder filnamnet som ikonens bildtext.
    Shape shape = builder.InsertOleObjectAsIcon(stream, "PowerPoint.Application", ImageDir + "Logo icon.ico",
        "My embedded file stream");

    OlePackage setOlePackage = shape.OleFormat.OlePackage;
    setOlePackage.FileName = "Presentation.pptx";
    setOlePackage.DisplayName = "Presentation.pptx";
}

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOleObjectAsIcon.docx");
```

### Se även

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## InsertOleObjectAsIcon(*Stream, string, string, string*) {#insertoleobjectasicon}

Infogar ett inbäddat OLE-objekt som ikon från en ström i dokumentet. Tillåter att ange ikonfil och bildtext. Identifierar OLE-objekttyp med hjälp av given progID-parameter.

```csharp
public Shape InsertOleObjectAsIcon(Stream stream, string progId, string iconFile, 
    string iconCaption)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| stream | Stream | Ström som innehåller applikationsdata. |
| progId | String | ProgId för OLE-objekt. |
| iconFile | String | Fullständig sökväg till ICO-filen. Om värdet är`null` Aspose.Words kommer att använda en fördefinierad bild. |
| iconCaption | String | Ikontext. Om värdet är`null` Aspose.Words kommer att använda en fördefinierad ikonbildtext. |

### Returvärde

Formnod som innehåller Ole-objektet och infogas vid den aktuella Builder-positionen.

## Exempel

Visar hur man infogar ett inbäddat eller länkat OLE-objekt som en ikon i dokumentet.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Om 'iconFile' och 'iconCaption' utelämnas, väljer denna överbelastade metod
// ikonen enligt 'progId' och använder filnamnet som ikonens bildtext.
builder.InsertOleObjectAsIcon(MyDir + "Presentation.pptx", "Package", false, ImageDir + "Logo icon.ico", "My embedded file");

builder.InsertBreak(BreakType.LineBreak);

using (FileStream stream = new FileStream(MyDir + "Presentation.pptx", FileMode.Open))
{
    // Om 'iconFile' och 'iconCaption' utelämnas, väljer denna överbelastade metod
    // ikonen enligt filändelsen och använder filnamnet som ikonens bildtext.
    Shape shape = builder.InsertOleObjectAsIcon(stream, "PowerPoint.Application", ImageDir + "Logo icon.ico",
        "My embedded file stream");

    OlePackage setOlePackage = shape.OleFormat.OlePackage;
    setOlePackage.FileName = "Presentation.pptx";
    setOlePackage.DisplayName = "Presentation.pptx";
}

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOleObjectAsIcon.docx");
```

### Se även

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
