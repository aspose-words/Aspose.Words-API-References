---
title: DocumentBuilder.InsertShape
linktitle: InsertShape
articleTitle: InsertShape
second_title: Aspose.Words for .NET
description: DocumentBuilder InsertShape method. Inserts inline shape with specified type and size in C#.
type: docs
weight: 450
url: /net/aspose.words/documentbuilder/insertshape/
---
## InsertShape(*[ShapeType](../../../aspose.words.drawing/shapetype/), double, double*) {#insertshape_1}

Inserts inline shape with specified type and size.

```csharp
public Shape InsertShape(ShapeType shapeType, double width, double height)
```

| Parameter | Type | Description |
| --- | --- | --- |
| shapeType | ShapeType | The shape type to insert into the document. |
| width | Double | The width of the shape in points. |
| height | Double | The height of the shape in points. |

### Return Value

The shape node that was inserted.

## Examples

Shows how to insert DML shapes into a document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Below are two wrapping types that shapes may have.
// 1 -  Floating:
builder.InsertShape(ShapeType.TopCornersRounded, RelativeHorizontalPosition.Page, 100,
        RelativeVerticalPosition.Page, 100, 50, 50, WrapType.None);

// 2 -  Inline:
builder.InsertShape(ShapeType.DiagonalCornersRounded, 50, 50);

// If you need to create "non-primitive" shapes, such as SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded, or DiagonalCornersRounded,
// then save the document with "Strict" or "Transitional" compliance, which allows saving shape as DML.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.Docx);
saveOptions.Compliance = OoxmlCompliance.Iso29500_2008_Transitional;

doc.Save(ArtifactsDir + "Shape.ShapeInsertion.docx", saveOptions);
```

### See Also

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [ShapeType](../../../aspose.words.drawing/shapetype/)
* class [DocumentBuilder](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)

---

## InsertShape(*[ShapeType](../../../aspose.words.drawing/shapetype/), [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../../aspose.words.drawing/wraptype/)*) {#insertshape}

Inserts free-floating shape with specified position, size and text wrap type.

```csharp
public Shape InsertShape(ShapeType shapeType, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Parameter | Type | Description |
| --- | --- | --- |
| shapeType | ShapeType | The shape type to insert into the document |
| horzPos | RelativeHorizontalPosition | Specifies where the horizontal distance to the shape is measured from. |
| left | Double | Distance in points from the origin to the left side of the shape. |
| vertPos | RelativeVerticalPosition | Specifies where the vertical distance to the shape is measured from. |
| top | Double | Distance in points from the origin to the top side of the shape. |
| width | Double | The width of the shape in points. |
| height | Double | The height of the shape in points. |
| wrapType | WrapType | Specifies how to wrap text around the shape. |

### Return Value

The shape node that was inserted.

## Examples

Shows how to insert DML shapes into a document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Below are two wrapping types that shapes may have.
// 1 -  Floating:
builder.InsertShape(ShapeType.TopCornersRounded, RelativeHorizontalPosition.Page, 100,
        RelativeVerticalPosition.Page, 100, 50, 50, WrapType.None);

// 2 -  Inline:
builder.InsertShape(ShapeType.DiagonalCornersRounded, 50, 50);

// If you need to create "non-primitive" shapes, such as SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded, or DiagonalCornersRounded,
// then save the document with "Strict" or "Transitional" compliance, which allows saving shape as DML.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.Docx);
saveOptions.Compliance = OoxmlCompliance.Iso29500_2008_Transitional;

doc.Save(ArtifactsDir + "Shape.ShapeInsertion.docx", saveOptions);
```

### See Also

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [ShapeType](../../../aspose.words.drawing/shapetype/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
