---
title: Aspose::Words::Drawing::ShapeBase::get_ShapeType method
linktitle: get_ShapeType
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::ShapeBase::get_ShapeType method. Gets the shape type in C++.'
type: docs
weight: 48000
url: /cpp/aspose.words.drawing/shapebase/get_shapetype/
---
## ShapeBase::get_ShapeType method


Gets the shape type.

```cpp
Aspose::Words::Drawing::ShapeType Aspose::Words::Drawing::ShapeBase::get_ShapeType()
```


## Examples



Shows how to create a group of shapes, and print its contents using a document visitor. 
```cpp
void GroupOfShapes()
{
    auto doc = MakeObject<Document>();
    auto builder = MakeObject<DocumentBuilder>(doc);

    // If you need to create "NonPrimitive" shapes, such as SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
    // TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded, DiagonalCornersRounded
    // please use DocumentBuilder.InsertShape methods.
    auto balloon = MakeObject<Shape>(doc, ShapeType::Balloon);
    balloon->set_Width(200);
    balloon->set_Height(200);
    balloon->get_Stroke()->set_Color(System::Drawing::Color::get_Red());

    auto cube = MakeObject<Shape>(doc, ShapeType::Cube);
    cube->set_Width(100);
    cube->set_Height(100);
    cube->get_Stroke()->set_Color(System::Drawing::Color::get_Blue());

    auto group = MakeObject<GroupShape>(doc);
    group->AppendChild(balloon);
    group->AppendChild(cube);

    ASSERT_TRUE(group->get_IsGroup());

    builder->InsertNode(group);

    auto printer = MakeObject<ExDrawing::ShapeGroupPrinter>();
    group->Accept(printer);

    std::cout << printer->GetText() << std::endl;
}

class ShapeGroupPrinter : public DocumentVisitor
{
public:
    ShapeGroupPrinter()
    {
        mBuilder = MakeObject<System::Text::StringBuilder>();
    }

    String GetText()
    {
        return mBuilder->ToString();
    }

    VisitorAction VisitGroupShapeStart(SharedPtr<GroupShape> groupShape) override
    {
        mBuilder->AppendLine(u"Shape group started:");
        return VisitorAction::Continue;
    }

    VisitorAction VisitGroupShapeEnd(SharedPtr<GroupShape> groupShape) override
    {
        mBuilder->AppendLine(u"End of shape group");
        return VisitorAction::Continue;
    }

    VisitorAction VisitShapeStart(SharedPtr<Shape> shape) override
    {
        mBuilder->AppendLine(String(u"\tShape - ") + System::ObjectExt::ToString(shape->get_ShapeType()) + u":");
        mBuilder->AppendLine(String(u"\t\tWidth: ") + shape->get_Width());
        mBuilder->AppendLine(String(u"\t\tHeight: ") + shape->get_Height());
        mBuilder->AppendLine(String(u"\t\tStroke color: ") + shape->get_Stroke()->get_Color());
        mBuilder->AppendLine(String(u"\t\tFill color: ") + shape->get_Fill()->get_ForeColor());
        return VisitorAction::Continue;
    }

    VisitorAction VisitShapeEnd(SharedPtr<Shape> shape) override
    {
        mBuilder->AppendLine(u"\tEnd of shape");
        return VisitorAction::Continue;
    }

private:
    SharedPtr<System::Text::StringBuilder> mBuilder;
};
```

## See Also

* Enum [ShapeType](../../shapetype/)
* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
