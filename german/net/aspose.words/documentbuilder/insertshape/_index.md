---
title: DocumentBuilder.InsertShape
second_title: Aspose.Words für .NET-API-Referenz
description: DocumentBuilder methode. Fügt InlineForm mit angegebenem Typ und Größe ein.
type: docs
weight: 410
url: /de/net/aspose.words/documentbuilder/insertshape/
---
## InsertShape(ShapeType, double, double) {#insertshape_1}

Fügt Inline-Form mit angegebenem Typ und Größe ein.

```csharp
public Shape InsertShape(ShapeType shapeType, double width, double height)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| shapeType | ShapeType | Der Formtyp, der in das Dokument eingefügt werden soll. |
| width | Double | Die Breite der Form in Punkt. |
| height | Double | Die Höhe der Form in Punkt. |

### Rückgabewert

Der eingefügte Shape-Knoten.

### Beispiele

Zeigt, wie DML-Shapes in ein Dokument eingefügt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Unten sind zwei Wrapping-Typen, die Shapes haben können.
// 1 - Floating:
builder.InsertShape(ShapeType.TopCornersRounded, RelativeHorizontalPosition.Page, 100, 
        RelativeVerticalPosition.Page, 100, 50, 50, WrapType.None);

// 2 - Inline:
builder.InsertShape(ShapeType.DiagonalCornersRounded, 50, 50);

// Wenn Sie "nicht primitive" Formen erstellen müssen, wie SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded oder DiagonalCornersRounded,
// Speichern Sie dann das Dokument mit "Strict"- oder "Transitional"-Compliance, wodurch die Form als DML gespeichert werden kann.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.Docx);
saveOptions.Compliance = OoxmlCompliance.Iso29500_2008_Transitional;

doc.Save(ArtifactsDir + "Shape.ShapeInsertion.docx", saveOptions);
```

### Siehe auch

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [ShapeType](../../../aspose.words.drawing/shapetype/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../documentbuilder/)
* Montage [Aspose.Words](../../../)

---

## InsertShape(ShapeType, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) {#insertshape}

Fügt eine freischwebende Form mit angegebener Position, Größe und Textumbruchtyp ein.

```csharp
public Shape InsertShape(ShapeType shapeType, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| shapeType | ShapeType | Der Formtyp, der in das Dokument eingefügt werden soll |
| horzPos | RelativeHorizontalPosition | Gibt an, wo der horizontale Abstand zur Form gemessen wird. |
| left | Double | Abstand in Punkten vom Ursprung zur linken Seite der Form. |
| vertPos | RelativeVerticalPosition | Gibt an, wo der vertikale Abstand zur Form gemessen wird. |
| top | Double | Abstand in Punkten vom Ursprung zur Oberseite der Form. |
| width | Double | Die Breite der Form in Punkt. |
| height | Double | Die Breite der Form in Punkt. |
| wrapType | WrapType | Gibt an, wie Text um die Form gewickelt wird. |

### Rückgabewert

Der eingefügte Shape-Knoten.

### Beispiele

Zeigt, wie DML-Shapes in ein Dokument eingefügt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Unten sind zwei Wrapping-Typen, die Shapes haben können.
// 1 - Floating:
builder.InsertShape(ShapeType.TopCornersRounded, RelativeHorizontalPosition.Page, 100, 
        RelativeVerticalPosition.Page, 100, 50, 50, WrapType.None);

// 2 - Inline:
builder.InsertShape(ShapeType.DiagonalCornersRounded, 50, 50);

// Wenn Sie "nicht primitive" Formen erstellen müssen, wie SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded oder DiagonalCornersRounded,
// Speichern Sie dann das Dokument mit "Strict"- oder "Transitional"-Compliance, wodurch die Form als DML gespeichert werden kann.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.Docx);
saveOptions.Compliance = OoxmlCompliance.Iso29500_2008_Transitional;

doc.Save(ArtifactsDir + "Shape.ShapeInsertion.docx", saveOptions);
```

### Siehe auch

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [ShapeType](../../../aspose.words.drawing/shapetype/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../documentbuilder/)
* Montage [Aspose.Words](../../../)


