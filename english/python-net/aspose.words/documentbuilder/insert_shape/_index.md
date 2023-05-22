---
title: DocumentBuilder.insert_shape method
linktitle: insert_shape method
articleTitle: insert_shape method
second_title: Aspose.Words for Python
description: "aspose.words.DocumentBuilder.insert_shape method"
type: docs
weight: 430
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
| shape_type | [ShapeType](../../../aspose.words.drawing/shapetype/) |  |
| width | float |  |
| height | float |  |

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
| shape_type | [ShapeType](../../../aspose.words.drawing/shapetype/) |  |
| horz_pos | [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/) |  |
| left | float |  |
| vert_pos | [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/) |  |
| top | float |  |
| width | float |  |
| height | float |  |
| wrap_type | [WrapType](../../../aspose.words.drawing/wraptype/) |  |

### Returns

The shape node that was inserted.


## Examples

Shows how to insert DML shapes into a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Below are two wrapping types that shapes may have.
# 1 -  Floating:
builder.insert_shape(aw.drawing.ShapeType.TOP_CORNERS_ROUNDED, aw.drawing.RelativeHorizontalPosition.PAGE, 100,
        aw.drawing.RelativeVerticalPosition.PAGE, 100, 50, 50, aw.drawing.WrapType.NONE)

# 2 -  Inline:
builder.insert_shape(aw.drawing.ShapeType.DIAGONAL_CORNERS_ROUNDED, 50, 50)

# If you need to create "non-primitive" shapes, such as SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
# TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded, or DiagonalCornersRounded,
# then save the document with "Strict" or "Transitional" compliance, which allows saving shape as DML.
save_options = aw.saving.OoxmlSaveOptions(aw.SaveFormat.DOCX)
save_options.compliance = aw.saving.OoxmlCompliance.ISO29500_2008_TRANSITIONAL

doc.save(ARTIFACTS_DIR + "Shape.shape_insertion.docx", save_options)
```

## See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

