---
title: DocumentBuilder.InsertShape
linktitle: InsertShape
articleTitle: InsertShape
second_title: Aspose.Words för .NET
description: Lägg enkelt till anpassade inline-former med DocumentBuilders InsertShape-metod. Förbättra dina dokument med skräddarsydda bilder för effektfulla presentationer!
type: docs
weight: 460
url: /sv/net/aspose.words/documentbuilder/insertshape/
---
## InsertShape(*[ShapeType](../../../aspose.words.drawing/shapetype/), double, double*) {#insertshape_1}

Infogar inbäddad form med angiven typ och storlek.

```csharp
public Shape InsertShape(ShapeType shapeType, double width, double height)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| shapeType | ShapeType | Formtypen som ska infogas i dokumentet. |
| width | Double | Formens bredd i punkter. |
| height | Double | Formens höjd i punkter. |

### Returvärde

Formnoden som infogades.

## Exempel

Visar hur man infogar DML-former i ett dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Nedan följer två typer av omslag som former kan ha.
// 1 - Flytande:
builder.InsertShape(ShapeType.TopCornersRounded, RelativeHorizontalPosition.Page, 100,
        RelativeVerticalPosition.Page, 100, 50, 50, WrapType.None);

// 2 - Inline:
builder.InsertShape(ShapeType.DiagonalCornersRounded, 50, 50);

// Om du behöver skapa "icke-primitiva" former, till exempel SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// ÖvreHörnEttRundatEttBeskärt, EnkeltHörnRundat, ÖvreHörnRundade eller DiagonalaHörnRundade,
// spara sedan dokumentet med "Strict"- eller "Transitional"-kompatibilitet, vilket gör att formen kan sparas som DML.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.Docx);
saveOptions.Compliance = OoxmlCompliance.Iso29500_2008_Transitional;

doc.Save(ArtifactsDir + "Shape.ShapeInsertion.docx", saveOptions);
```

### Se även

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [ShapeType](../../../aspose.words.drawing/shapetype/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## InsertShape(*[ShapeType](../../../aspose.words.drawing/shapetype/), [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../../aspose.words.drawing/wraptype/)*) {#insertshape}

Infogar fritt flytande form med angiven position, storlek och radbrytningstyp.

```csharp
public Shape InsertShape(ShapeType shapeType, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| shapeType | ShapeType | Formtypen som ska infogas i dokumentet |
| horzPos | RelativeHorizontalPosition | Anger varifrån det horisontella avståndet till formen mäts. |
| left | Double | Avstånd i punkter från origo till vänster sida av formen. |
| vertPos | RelativeVerticalPosition | Anger varifrån det vertikala avståndet till formen mäts. |
| top | Double | Avstånd i punkter från origo till formens översida. |
| width | Double | Formens bredd i punkter. |
| height | Double | Formens höjd i punkter. |
| wrapType | WrapType | Anger hur text ska radbrytas runt formen. |

### Returvärde

Formnoden som infogades.

## Exempel

Visar hur man infogar DML-former i ett dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Nedan följer två typer av omslag som former kan ha.
// 1 - Flytande:
builder.InsertShape(ShapeType.TopCornersRounded, RelativeHorizontalPosition.Page, 100,
        RelativeVerticalPosition.Page, 100, 50, 50, WrapType.None);

// 2 - Inline:
builder.InsertShape(ShapeType.DiagonalCornersRounded, 50, 50);

// Om du behöver skapa "icke-primitiva" former, till exempel SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// ÖvreHörnEttRundatEttBeskärt, EnkeltHörnRundat, ÖvreHörnRundade eller DiagonalaHörnRundade,
// spara sedan dokumentet med "Strict"- eller "Transitional"-kompatibilitet, vilket gör att formen kan sparas som DML.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.Docx);
saveOptions.Compliance = OoxmlCompliance.Iso29500_2008_Transitional;

doc.Save(ArtifactsDir + "Shape.ShapeInsertion.docx", saveOptions);
```

### Se även

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [ShapeType](../../../aspose.words.drawing/shapetype/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
