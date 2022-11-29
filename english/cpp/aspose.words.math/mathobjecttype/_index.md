---
title: MathObjectType
second_title: Aspose.Words for C++ API Reference
description: Specifies type of an Office Math object.
type: docs
weight: 14
url: /cpp/aspose.words.math/mathobjecttype/
---
## MathObjectType enum


Specifies type of an Office [Math](../) object.

```cpp
enum class MathObjectType
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| OMath | 0 | Instance of mathematical text. |
| OMathPara | 1 | [Math](../) paragraph, or display math zone, that contains one or more [OMath](./) elements that are in display mode. |
| Accent | 2 | Accent function, consisting of a base and a combining diacritical mark. |
| Bar | 3 | Bar function, consisting of a base argument and an overbar or underbar. |
| BorderBox | 4 | [Border](../../aspose.words/border/) Box object, consisting of a border drawn around an instance of mathematical text (such as a formula or equation) |
| Box | 5 | Box object, which is used to group components of an equation or other instance of mathematical text. |
| Delimiter | 6 | Delimiter object, consisting of opening and closing delimiters (such as parentheses, braces, brackets, and vertical bars), and an element contained inside. |
| Degree | 7 | Degree in the mathematical radical. |
| Argument | 8 | Argument object. Encloses Office [Math](../) entities when they are used as arguments to other Office [Math](../) entities. |
| Array | 9 | Array object, consisting of one or more equations, expressions, or other mathematical text runs that can be vertically justified as a unit with respect to surrounding text on the line. |
| Fraction | 10 | Fraction object, consisting of a numerator and denominator separated by a fraction bar. |
| Denominator | 11 | Denominator of a fraction object. |
| Numerator | 12 | Numerator of the Fraction object. |
| Function | 13 | Function-Apply object, which consists of a function name and an argument element acted upon. |
| FunctionName | 14 | Name of the function. For example, function names are sin and cos. |
| GroupCharacter | 15 | Group-Character object, consisting of a character drawn above or below text, often with the purpose of visually grouping items. |
| Limit | 16 | Lower limit of the [LowerLimit](./) object and the upper limit of the [UpperLimit](./) function. |
| LowerLimit | 17 | Lower-Limit object, consisting of text on the baseline and reduced-size text immediately below it. |
| UpperLimit | 18 | Upper-Limit object, consisting of text on the baseline and reduced-size text immediately above it. |
| Matrix | 19 | Matrix object, consisting of one or more elements laid out in one or more rows and one or more columns. |
| MatrixRow | 20 | Single row of the matrix. |
| NAry | 21 | N-ary object, consisting of an n-ary object, a base (or operand), and optional upper and lower limits. |
| Phantom | 22 | Phantom object. |
| Radical | 23 | Radical object, consisting of a radical, a base element, and an optional degree . |
| SubscriptPart | 24 | Subscript of the object that can have subscript part. |
| SuperscriptPart | 25 | Superscript of the superscript object. |
| PreSubSuperscript | 26 | Pre-Sub-Superscript object, which consists of a base element and a subscript and superscript placed to the left of the base. |
| Subscript | 27 | Subscript object, which consists of a base element and a reduced-size script placed below and to the right. |
| SubSuperscript | 28 | Sub-superscript object, which consists of a base element, a reduced-size script placed below and to the right, and a reduced-size script placed above and to the right. |
| Supercript | 29 | Superscript object, which consists of a base element and a reduced-size script placed above and to the right. |


## Examples



Shows how to print the node structure of every office math node in a document. 
```cpp
void OfficeMathToText()
{
    auto doc = MakeObject<Document>(MyDir + u"DocumentVisitor-compatible features.docx");
    auto visitor = MakeObject<ExDocumentVisitor::OfficeMathStructurePrinter>();

    // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
    // and then traverses all the node's children in a depth-first manner.
    // The visitor can read and modify each visited node.
    doc->Accept(visitor);

    std::cout << visitor->GetText() << std::endl;
}

class OfficeMathStructurePrinter : public DocumentVisitor
{
public:
    OfficeMathStructurePrinter() : mVisitorIsInsideOfficeMath(false), mDocTraversalDepth(0)
    {
        mBuilder = MakeObject<System::Text::StringBuilder>();
        mVisitorIsInsideOfficeMath = false;
    }

    String GetText()
    {
        return mBuilder->ToString();
    }

    VisitorAction VisitRun(SharedPtr<Run> run) override
    {
        if (mVisitorIsInsideOfficeMath)
        {
            IndentAndAppendLine(String(u"[Run] \"") + run->GetText() + u"\"");
        }

        return VisitorAction::Continue;
    }

    VisitorAction VisitOfficeMathStart(SharedPtr<OfficeMath> officeMath) override
    {
        IndentAndAppendLine(String(u"[OfficeMath start] Math object type: ") + System::ObjectExt::ToString(officeMath->get_MathObjectType()));
        mDocTraversalDepth++;
        mVisitorIsInsideOfficeMath = true;

        return VisitorAction::Continue;
    }

    VisitorAction VisitOfficeMathEnd(SharedPtr<OfficeMath> officeMath) override
    {
        mDocTraversalDepth--;
        IndentAndAppendLine(u"[OfficeMath end]");
        mVisitorIsInsideOfficeMath = false;

        return VisitorAction::Continue;
    }

private:
    bool mVisitorIsInsideOfficeMath;
    int mDocTraversalDepth;
    SharedPtr<System::Text::StringBuilder> mBuilder;

    void IndentAndAppendLine(String text)
    {
        for (int i = 0; i < mDocTraversalDepth; i++)
        {
            mBuilder->Append(u"|  ");
        }

        mBuilder->AppendLine(text);
    }
};
```

## See Also

* Namespace [Aspose::Words::Math](../)
* Library [Aspose.Words](../../)
