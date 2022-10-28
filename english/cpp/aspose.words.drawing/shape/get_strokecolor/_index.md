---
title: get_StrokeColor
second_title: Aspose.Words for C++ API Reference
description: Defines the color of a stroke.
type: docs
weight: 248
url: /cpp/aspose.words.drawing/shape/get_strokecolor/
---
## Shape.get_StrokeColor method


Defines the color of a stroke.

```cpp
System::Drawing::Color Aspose::Words::Drawing::Shape::get_StrokeColor()
```


This is a shortcut to the [Color](../../stroke/get_color/) property.

The default value is **Black**.

## Examples




Shows how to fill a shape with a solid color. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Write some text, and then cover it with a floating shape.
builder->get_Font()->set_Size(32);
builder->Writeln(u"Hello world!");

SharedPtr<Shape> shape = builder->InsertShape(ShapeType::CloudCallout, RelativeHorizontalPosition::LeftMargin, 25, RelativeVerticalPosition::TopMargin,
                                              25, 250, 150, WrapType::None);

// Use the "StrokeColor" property to set the color of the outline of the shape.
shape->set_StrokeColor(System::Drawing::Color::get_CadetBlue());

// Use the "FillColor" property to set the color of the inside area of the shape.
shape->set_FillColor(System::Drawing::Color::get_LightBlue());

// The "Opacity" property determines how transparent the color is on a 0-1 scale,
// with 1 being fully opaque, and 0 being invisible.
// The shape fill by default is fully opaque, so we cannot see the text that this shape is on top of.
ASPOSE_ASSERT_EQ(1.0, shape->get_Fill()->get_Opacity());

// Set the shape fill color's opacity to a lower value so that we can see the text underneath it.
shape->get_Fill()->set_Opacity(0.3);

doc->Save(ArtifactsDir + u"Shape.Fill.docx");
```


Shows how to iterate over all the shapes in a document. 
```cpp
void VisitShapes()
{
    auto doc = MakeObject<Document>(MyDir + u"Revision shape.docx");

    auto visitor = MakeObject<ExShape::ShapeAppearancePrinter>();
    doc->Accept(visitor);

    std::cout << visitor->GetText() << std::endl;
}

class ShapeAppearancePrinter : public DocumentVisitor
{
public:
    ShapeAppearancePrinter() : mShapesVisited(0), mTextIndentLevel(0)
    {
        mShapesVisited = 0;
        mTextIndentLevel = 0;
        mStringBuilder = MakeObject<System::Text::StringBuilder>();
    }

    String GetText()
    {
        return String::Format(u"Shapes visited: {0}\n{1}", mShapesVisited, mStringBuilder);
    }

    VisitorAction VisitShapeStart(SharedPtr<Shape> shape) override
    {
        AppendLine(String::Format(u"Shape found: {0}", shape->get_ShapeType()));

        mTextIndentLevel++;

        if (shape->get_HasChart())
        {
            AppendLine(String::Format(u"Has chart: {0}", shape->get_Chart()->get_Title()->get_Text()));
        }

        AppendLine(String::Format(u"Extrusion enabled: {0}", shape->get_ExtrusionEnabled()));
        AppendLine(String::Format(u"Shadow enabled: {0}", shape->get_ShadowEnabled()));
        AppendLine(String::Format(u"StoryType: {0}", shape->get_StoryType()));

        if (shape->get_Stroked())
        {
            ASPOSE_EXPECT_EQ(shape->get_Stroke()->get_Color(), shape->get_StrokeColor());
            AppendLine(String::Format(u"Stroke colors: {0}, {1}", shape->get_Stroke()->get_Color(), shape->get_Stroke()->get_Color2()));
            AppendLine(String::Format(u"Stroke weight: {0}", shape->get_StrokeWeight()));
        }

        if (shape->get_Filled())
        {
            AppendLine(String::Format(u"Filled: {0}", shape->get_FillColor()));
        }

        if (shape->get_OleFormat() != nullptr)
        {
            AppendLine(String::Format(u"Ole found of type: {0}", shape->get_OleFormat()->get_ProgId()));
        }

        if (shape->get_SignatureLine() != nullptr)
        {
            AppendLine(String::Format(u"Found signature line for: {0}, {1}", shape->get_SignatureLine()->get_Signer(),
                                      shape->get_SignatureLine()->get_SignerTitle()));
        }

        return VisitorAction::Continue;
    }

    VisitorAction VisitShapeEnd(SharedPtr<Shape> shape) override
    {
        mTextIndentLevel--;
        mShapesVisited++;
        AppendLine(String::Format(u"End of {0}", shape->get_ShapeType()));

        return VisitorAction::Continue;
    }

    VisitorAction VisitGroupShapeStart(SharedPtr<GroupShape> groupShape) override
    {
        AppendLine(String::Format(u"Shape group found: {0}", groupShape->get_ShapeType()));
        mTextIndentLevel++;

        return VisitorAction::Continue;
    }

    VisitorAction VisitGroupShapeEnd(SharedPtr<GroupShape> groupShape) override
    {
        mTextIndentLevel--;
        AppendLine(String::Format(u"End of {0}", groupShape->get_ShapeType()));

        return VisitorAction::Continue;
    }

private:
    int mShapesVisited;
    int mTextIndentLevel;
    SharedPtr<System::Text::StringBuilder> mStringBuilder;

    void AppendLine(String text)
    {
        for (int i = 0; i < mTextIndentLevel; i++)
        {
            mStringBuilder->Append(u'\t');
        }

        mStringBuilder->AppendLine(text);
    }
};
```

