---
title: Aspose::Words::DocumentBuilder::InsertGroupShape method
linktitle: InsertGroupShape
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::DocumentBuilder::InsertGroupShape method. Groups the shapes passed as a parameter into a new GroupShape node which is inserted into the current position in C++.'
type: docs
weight: 35500
url: /cpp/aspose.words/documentbuilder/insertgroupshape/
---
## DocumentBuilder::InsertGroupShape(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Drawing::ShapeBase\>\>\&) method


Groups the shapes passed as a parameter into a new GroupShape node which is inserted into the current position.

```cpp
System::SharedPtr<Aspose::Words::Drawing::GroupShape> Aspose::Words::DocumentBuilder::InsertGroupShape(const System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::ShapeBase>> &shapes)
```


| Parameter | Type | Description |
| --- | --- | --- |
| shapes | const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Drawing::ShapeBase\>\>\& | The list of shapes to be grouped. |
## Remarks


The position and dimension of the new GroupShape will be calculated automatically.

VML and DML shapes cannot be grouped together.

## See Also

* Class [GroupShape](../../../aspose.words.drawing/groupshape/)
* Class [ShapeBase](../../../aspose.words.drawing/shapebase/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertGroupShape(double, double, double, double, const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Drawing::ShapeBase\>\>\&) method


Groups the shapes passed as a parameter into a new GroupShape node of the specified size which is inserted into the specified position.

```cpp
System::SharedPtr<Aspose::Words::Drawing::GroupShape> Aspose::Words::DocumentBuilder::InsertGroupShape(double left, double top, double width, double height, const System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::ShapeBase>> &shapes)
```


| Parameter | Type | Description |
| --- | --- | --- |
| left | double | Distance in points from the origin to the left side of the group shape. |
| top | double | Distance in points from the origin to the top side of the group shape. |
| width | double | The width of the group shape in points. A negative value is not allowed. |
| height | double | The height of the group shape in points. A negative value is not allowed. |
| shapes | const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Drawing::ShapeBase\>\>\& | The list of shapes to be grouped. |

## See Also

* Class [GroupShape](../../../aspose.words.drawing/groupshape/)
* Class [ShapeBase](../../../aspose.words.drawing/shapebase/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
