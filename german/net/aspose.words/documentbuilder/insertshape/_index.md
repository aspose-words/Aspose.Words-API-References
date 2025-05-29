---
title: DocumentBuilder.InsertShape
linktitle: InsertShape
articleTitle: InsertShape
second_title: Aspose.Words für .NET
description: Fügen Sie mühelos benutzerdefinierte Inline-Formen mit der InsertShape-Methode von DocumentBuilder hinzu. Optimieren Sie Ihre Dokumente mit maßgeschneiderten visuellen Elementen für eindrucksvolle Präsentationen!
type: docs
weight: 460
url: /de/net/aspose.words/documentbuilder/insertshape/
---
## InsertShape(*[ShapeType](../../../aspose.words.drawing/shapetype/), double, double*) {#insertshape_1}

Fügt eine Inline-Form mit angegebenem Typ und angegebener Größe ein.

```csharp
public Shape InsertShape(ShapeType shapeType, double width, double height)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| shapeType | ShapeType | Der in das Dokument einzufügende Formtyp. |
| width | Double | Die Breite der Form in Punkten. |
| height | Double | Die Höhe der Form in Punkten. |

### Rückgabewert

Der eingefügte Formknoten.

## Beispiele

Zeigt, wie DML-Formen in ein Dokument eingefügt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Unten sind zwei Umbrucharten aufgeführt, die Formen haben können.
// 1 - Schwebend:
builder.InsertShape(ShapeType.TopCornersRounded, RelativeHorizontalPosition.Page, 100,
        RelativeVerticalPosition.Page, 100, 50, 50, WrapType.None);

// 2 - Inline:
builder.InsertShape(ShapeType.DiagonalCornersRounded, 50, 50);

// Wenn Sie „nicht-primitive“ Formen erstellen müssen, wie z. B. SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded oder DiagonalCornersRounded,
// Speichern Sie das Dokument dann mit der Konformität „Strict“ oder „Transitional“, wodurch die Form als DML gespeichert werden kann.
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

Fügt eine frei schwebende Form mit angegebener Position, Größe und Textumbruchart ein.

```csharp
public Shape InsertShape(ShapeType shapeType, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| shapeType | ShapeType | Der in das Dokument einzufügende Formtyp |
| horzPos | RelativeHorizontalPosition | Gibt an, von wo aus der horizontale Abstand zur Form gemessen wird. |
| left | Double | Abstand in Punkten vom Ursprung zur linken Seite der Form. |
| vertPos | RelativeVerticalPosition | Gibt an, von wo aus der vertikale Abstand zur Form gemessen wird. |
| top | Double | Abstand in Punkten vom Ursprung zur Oberseite der Form. |
| width | Double | Die Breite der Form in Punkten. |
| height | Double | Die Höhe der Form in Punkten. |
| wrapType | WrapType | Gibt an, wie der Text um die Form herumfließen soll. |

### Rückgabewert

Der eingefügte Formknoten.

## Beispiele

Zeigt, wie DML-Formen in ein Dokument eingefügt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Unten sind zwei Umbrucharten aufgeführt, die Formen haben können.
// 1 - Schwebend:
builder.InsertShape(ShapeType.TopCornersRounded, RelativeHorizontalPosition.Page, 100,
        RelativeVerticalPosition.Page, 100, 50, 50, WrapType.None);

// 2 - Inline:
builder.InsertShape(ShapeType.DiagonalCornersRounded, 50, 50);

// Wenn Sie „nicht-primitive“ Formen erstellen müssen, wie z. B. SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded oder DiagonalCornersRounded,
// Speichern Sie das Dokument dann mit der Konformität „Strict“ oder „Transitional“, wodurch die Form als DML gespeichert werden kann.
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
