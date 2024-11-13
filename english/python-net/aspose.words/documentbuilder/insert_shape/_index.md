---
title: DocumentBuilder.insert_shape method
linktitle: insert_shape method
articleTitle: insert_shape method
second_title: Aspose.Words for Python
description: "aspose.words.DocumentBuilder.insert_shape method"
type: docs
weight: 460
url: /python-net/aspose.words/documentbuilder/insert_shape/
---

## insert_shape(shape_type, width, height) {#shapetype_float_float}

Inserts inline shape with specified type and size.


```python
def insert_shape(self, shape_type: aspose.words.drawing.ShapeType, width: float, height: float):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| shape_type | [ShapeType](../../../aspose.words.drawing/shapetype/) | The shape type to insert into the document. |
| width | float | The width of the shape in points. |
| height | float | The height of the shape in points. |

### Returns

The shape node that was inserted.


## insert_shape(shape_type, horz_pos, left, vert_pos, top, width, height, wrap_type) {#shapetype_relativehorizontalposition_float_relativeverticalposition_float_float_float_wraptype}

Inserts free-floating shape with specified position, size and text wrap type.


```python
def insert_shape(self, shape_type: aspose.words.drawing.ShapeType, horz_pos: aspose.words.drawing.RelativeHorizontalPosition, left: float, vert_pos: aspose.words.drawing.RelativeVerticalPosition, top: float, width: float, height: float, wrap_type: aspose.words.drawing.WrapType):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| shape_type | [ShapeType](../../../aspose.words.drawing/shapetype/) | The shape type to insert into the document |
| horz_pos | [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/) | Specifies where the horizontal distance to the shape is measured from. |
| left | float | Distance in points from the origin to the left side of the shape. |
| vert_pos | [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/) | Specifies where the vertical distance to the shape is measured from. |
| top | float | Distance in points from the origin to the top side of the shape. |
| width | float | The width of the shape in points. |
| height | float | The height of the shape in points. |
| wrap_type | [WrapType](../../../aspose.words.drawing/wraptype/) | Specifies how to wrap text around the shape. |

### Returns

The shape node that was inserted.


## Examples

Shows how to insert DML shapes into a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Below are two wrapping types that shapes may have.
# 1 -  Floating:
builder.insert_shape(shape_type=aw.drawing.ShapeType.TOP_CORNERS_ROUNDED, horz_pos=aw.drawing.RelativeHorizontalPosition.PAGE, left=100, vert_pos=aw.drawing.RelativeVerticalPosition.PAGE, top=100, width=50, height=50, wrap_type=aw.drawing.WrapType.NONE)
# 2 -  Inline:
builder.insert_shape(shape_type=aw.drawing.ShapeType.DIAGONAL_CORNERS_ROUNDED, width=50, height=50)
# If you need to create "non-primitive" shapes, such as SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
# TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded, or DiagonalCornersRounded,
# then save the document with "Strict" or "Transitional" compliance, which allows saving shape as DML.
save_options = aw.saving.OoxmlSaveOptions(aw.SaveFormat.DOCX)
save_options.compliance = aw.saving.OoxmlCompliance.ISO29500_2008_TRANSITIONAL
doc.save(file_name=ARTIFACTS_DIR + 'Shape.ShapeInsertion.docx', save_options=save_options)
```

## See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

