---
title: InsertOleObjectAsIcon
second_title: Aspose.Words för .NET API Referens
description: Infogar ett inbäddat eller länkat OLEobjekt som ikon i dokumentet. Tillåter att ange ikonfil och bildtext. Upptäcker OLEobjekttyp med filtillägg.
type: docs
weight: 380
url: /sv/net/aspose.words/documentbuilder/insertoleobjectasicon/
---
## InsertOleObjectAsIcon(string, bool, string, string) {#insertoleobjectasicon_1}

Infogar ett inbäddat eller länkat OLE-objekt som ikon i dokumentet. Tillåter att ange ikonfil och bildtext. Upptäcker OLE-objekttyp med filtillägg.

```csharp
public Shape InsertOleObjectAsIcon(string fileName, bool isLinked, string iconFile, 
    string iconCaption)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fileName | String | Fullständig sökväg till filen. |
| isLinked | Boolean | Om true infogas länkat OLE-objekt annars infogas inbäddat OLE-objekt. |
| iconFile | String | Fullständig sökväg till ICO-filen. Om värdet är null kommer Aspose.Words att använda en fördefinierad bild. |
| iconCaption | String | Ikontext. Om värdet är null kommer Aspose.Words att använda filnamnet. |

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

## InsertOleObjectAsIcon(string, string, bool, string, string) {#insertoleobjectasicon_2}

Infogar ett inbäddat eller länkat OLE-objekt som ikon i dokumentet. Tillåter att ange ikonfil och bildtext. Upptäcker OLE-objekttyp med hjälp av given progID-parameter.

```csharp
public Shape InsertOleObjectAsIcon(string fileName, string progId, bool isLinked, string iconFile, 
    string iconCaption)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fileName | String | Fullständig sökväg till filen. |
| progId | String | ProgId för OLE-objekt. |
| isLinked | Boolean | Om true infogas länkat OLE-objekt annars infogas inbäddat OLE-objekt. |
| iconFile | String | Fullständig sökväg till ICO-filen. Om värdet är null kommer Aspose.Words att använda en fördefinierad bild. |
| iconCaption | String | Ikontext. Om värdet är null kommer Aspose.Words att använda filnamnet. |

### Returvärde

Formnod som innehåller Ole-objektet och infogat vid den aktuella Builder-positionen.

### Exempel

Visar hur man infogar ett inbäddat eller länkat OLE-objekt som ikon i dokumentet.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Om 'iconFile' och 'iconCaption' utelämnas, väljer denna överbelastade metod
// ikonen enligt 'progId' och använder filnamnet för ikontexten.
builder.InsertOleObjectAsIcon(MyDir + "Presentation.pptx", "Package", false, ImageDir + "Logo icon.ico", "My embedded file");

builder.InsertBreak(BreakType.LineBreak);

using (FileStream stream = new FileStream(MyDir + "Presentation.pptx", FileMode.Open))
{
    // Om 'iconFile' och 'iconCaption' utelämnas, väljer denna överbelastade metod
    // ikonen enligt filtillägget och använder filnamnet för ikontexten.
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
* namnutrymme [Aspose.Words](../../documentbuilder/)
* hopsättning [Aspose.Words](../../../)

---

## InsertOleObjectAsIcon(Stream, string, string, string) {#insertoleobjectasicon}

Infogar ett inbäddat OLE-objekt som ikon från en ström i dokumentet. Tillåter att ange ikonfil och bildtext. Upptäcker OLE-objekttyp med hjälp av given progID-parameter.

```csharp
public Shape InsertOleObjectAsIcon(Stream stream, string progId, string iconFile, 
    string iconCaption)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| stream | Stream | Ström som innehåller applikationsdata. |
| progId | String | ProgId för OLE-objekt. |
| iconFile | String | Fullständig sökväg till ICO-filen. Om värdet är null kommer Aspose.Words att använda en fördefinierad bild. |
| iconCaption | String | Ikontext. Om värdet är null kommer Aspose.Words att använda den fördefinierade ikontexten. |

### Returvärde

Formnod som innehåller Ole-objektet och infogat vid den aktuella Builder-positionen.

### Exempel

Visar hur man infogar ett inbäddat eller länkat OLE-objekt som ikon i dokumentet.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Om 'iconFile' och 'iconCaption' utelämnas, väljer denna överbelastade metod
// ikonen enligt 'progId' och använder filnamnet för ikontexten.
builder.InsertOleObjectAsIcon(MyDir + "Presentation.pptx", "Package", false, ImageDir + "Logo icon.ico", "My embedded file");

builder.InsertBreak(BreakType.LineBreak);

using (FileStream stream = new FileStream(MyDir + "Presentation.pptx", FileMode.Open))
{
    // Om 'iconFile' och 'iconCaption' utelämnas, väljer denna överbelastade metod
    // ikonen enligt filtillägget och använder filnamnet för ikontexten.
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
* namnutrymme [Aspose.Words](../../documentbuilder/)
* hopsättning [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
