---
title: Aspose::Words::Drawing::Shape::get_Filled method
linktitle: get_Filled
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Shape::get_Filled method. Determines whether the closed path of the shape will be filled in C++.'
type: docs
weight: 7000
url: /cpp/aspose.words.drawing/shape/get_filled/
---
## Shape::get_Filled method


Determines whether the closed path of the shape will be filled.

```cpp
bool Aspose::Words::Drawing::Shape::get_Filled()
```

## Remarks


This is a shortcut to the [On](../../fill/get_on/) property.

The default value is **true**.

## Examples



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

## See Also

* Class [Shape](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
