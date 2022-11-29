---
title: InsertShape
second_title: Aspose.Words for C++ API Reference
description: Inserts free-floating shape with specified position, size and text wrap type.
type: docs
weight: 547
url: /cpp/aspose.words/documentbuilder/insertshape/
---
## DocumentBuilder::InsertShape(Aspose::Words::Drawing::ShapeType, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


Inserts free-floating shape with specified position, size and text wrap type.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertShape(Aspose::Words::Drawing::ShapeType shapeType, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| Parameter | Type | Description |
| --- | --- | --- |
| shapeType | Aspose::Words::Drawing::ShapeType | The shape type to insert into the document |
| horzPos | Aspose::Words::Drawing::RelativeHorizontalPosition | Specifies where the horizontal distance to the shape is measured from. |
| left | double | Distance in points from the origin to the left side of the shape. |
| vertPos | Aspose::Words::Drawing::RelativeVerticalPosition | Specifies where the vertical distance to the shape is measured from. |
| top | double | Distance in points from the origin to the top side of the shape. |
| width | double | The width of the shape in points. |
| height | double | The width of the shape in points. |
| wrapType | Aspose::Words::Drawing::WrapType | Specifies how to wrap text around the shape. |

### ReturnValue

The shape node that was inserted.

## Examples



Shows how to insert DML shapes into a document. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Below are two wrapping types that shapes may have.
// 1 -  Floating:
builder->InsertShape(ShapeType::TopCornersRounded, RelativeHorizontalPosition::Page, 100, RelativeVerticalPosition::Page, 100, 50, 50, WrapType::None);

// 2 -  Inline:
builder->InsertShape(ShapeType::DiagonalCornersRounded, 50, 50);

// If you need to create "non-primitive" shapes, such as SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded, or DiagonalCornersRounded,
// then save the document with "Strict" or "Transitional" compliance, which allows saving shape as DML.
auto saveOptions = MakeObject<OoxmlSaveOptions>(SaveFormat::Docx);
saveOptions->set_Compliance(OoxmlCompliance::Iso29500_2008_Transitional);

doc->Save(ArtifactsDir + u"Shape.ShapeInsertion.docx", saveOptions);
```

## See Also

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [ShapeType](../../../aspose.words.drawing/shapetype/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
## DocumentBuilder::InsertShape(Aspose::Words::Drawing::ShapeType, double, double) method


Inserts inline shape with specified type and size.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertShape(Aspose::Words::Drawing::ShapeType shapeType, double width, double height)
```


| Parameter | Type | Description |
| --- | --- | --- |
| shapeType | Aspose::Words::Drawing::ShapeType | The shape type to insert into the document. |
| width | double | The width of the shape in points. |
| height | double | The height of the shape in points. |

### ReturnValue

The shape node that was inserted.

## Examples



Shows how to insert DML shapes into a document. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Below are two wrapping types that shapes may have.
// 1 -  Floating:
builder->InsertShape(ShapeType::TopCornersRounded, RelativeHorizontalPosition::Page, 100, RelativeVerticalPosition::Page, 100, 50, 50, WrapType::None);

// 2 -  Inline:
builder->InsertShape(ShapeType::DiagonalCornersRounded, 50, 50);

// If you need to create "non-primitive" shapes, such as SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded, or DiagonalCornersRounded,
// then save the document with "Strict" or "Transitional" compliance, which allows saving shape as DML.
auto saveOptions = MakeObject<OoxmlSaveOptions>(SaveFormat::Docx);
saveOptions->set_Compliance(OoxmlCompliance::Iso29500_2008_Transitional);

doc->Save(ArtifactsDir + u"Shape.ShapeInsertion.docx", saveOptions);
```

## See Also

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [ShapeType](../../../aspose.words.drawing/shapetype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
