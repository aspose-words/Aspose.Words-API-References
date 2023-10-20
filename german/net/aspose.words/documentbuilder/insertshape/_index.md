---
title: DocumentBuilder.InsertShape
linktitle: InsertShape
articleTitle: InsertShape
second_title: Aspose.Words für .NET
description: DocumentBuilder InsertShape methode. Fügt eine InlineForm mit dem angegebenen Typ und der angegebenen Größe ein in C#.
type: docs
weight: 430
url: /de/net/aspose.words/documentbuilder/insertshape/
---
## InsertShape(*[ShapeType](../../../aspose.words.drawing/shapetype/), double, double*) {#insertshape_1}

Fügt eine Inline-Form mit dem angegebenen Typ und der angegebenen Größe ein.

```csharp
public Shape InsertShape(ShapeType shapeType, double width, double height)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| shapeType | ShapeType | Der Formtyp, der in das Dokument eingefügt werden soll. |
| width | Double | Die Breite der Form in Punkten. |
| height | Double | Die Höhe der Form in Punkten. |

### Rückgabewert

Der eingefügte Formknoten.

## Beispiele

Zeigt, wie DML-Formen in ein Dokument eingefügt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Nachfolgend sind zwei Umhüllungstypen aufgeführt, die Formen haben können.
// 1 - Floating:
builder.InsertShape(ShapeType.TopCornersRounded, RelativeHorizontalPosition.Page, 100, 
        RelativeVerticalPosition.Page, 100, 50, 50, WrapType.None);

// 2 - Inline:
builder.InsertShape(ShapeType.DiagonalCornersRounded, 50, 50);

// Wenn Sie „nicht-primitive“ Formen erstellen müssen, wie z. B. SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded oder DiagonalCornersRounded,
// Speichern Sie dann das Dokument mit der Konformität „Streng“ oder „Übergang“, was das Speichern der Form als DML ermöglicht.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.Docx);
saveOptions.Compliance = OoxmlCompliance.Iso29500_2008_Transitional;

doc.Save(ArtifactsDir + "Shape.ShapeInsertion.docx", saveOptions);
```

### Siehe auch

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [ShapeType](../../../aspose.words.drawing/shapetype/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## InsertShape(*[ShapeType](../../../aspose.words.drawing/shapetype/), [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../../aspose.words.drawing/wraptype/)*) {#insertshape}

Fügt eine frei schwebende Form mit angegebener Position, Größe und Textumbruchtyp ein.

```csharp
public Shape InsertShape(ShapeType shapeType, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| shapeType | ShapeType | Der Formtyp, der in das Dokument eingefügt werden soll |
| horzPos | RelativeHorizontalPosition | Gibt an, von wo aus der horizontale Abstand zur Form gemessen wird. |
| left | Double | Abstand in Punkten vom Ursprung zur linken Seite der Form. |
| vertPos | RelativeVerticalPosition | Gibt an, von wo aus der vertikale Abstand zur Form gemessen wird. |
| top | Double | Abstand in Punkten vom Ursprung zur Oberseite der Form. |
| width | Double | Die Breite der Form in Punkten. |
| height | Double | Die Breite der Form in Punkten. |
| wrapType | WrapType | Gibt an, wie Text um die Form gewickelt wird. |

### Rückgabewert

Der eingefügte Formknoten.

## Beispiele

Zeigt, wie DML-Formen in ein Dokument eingefügt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Nachfolgend sind zwei Umhüllungstypen aufgeführt, die Formen haben können.
// 1 - Floating:
builder.InsertShape(ShapeType.TopCornersRounded, RelativeHorizontalPosition.Page, 100, 
        RelativeVerticalPosition.Page, 100, 50, 50, WrapType.None);

// 2 - Inline:
builder.InsertShape(ShapeType.DiagonalCornersRounded, 50, 50);

// Wenn Sie „nicht-primitive“ Formen erstellen müssen, wie z. B. SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded oder DiagonalCornersRounded,
// Speichern Sie dann das Dokument mit der Konformität „Streng“ oder „Übergang“, was das Speichern der Form als DML ermöglicht.
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
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
