---
title: Aspose::Words::Fields::FieldEQ class
linktitle: FieldEQ
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldEQ class. Implements the EQ field. To learn more, visit the  documentation article in C++.'
type: docs
weight: 40000
url: /cpp/aspose.words.fields/fieldeq/
---
## FieldEQ class


Implements the EQ field. To learn more, visit the [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) documentation article.

```cpp
class FieldEQ : public Aspose::Words::Fields::Field
```

## Methods

| Method | Description |
| --- | --- |
| [AsOfficeMath](./asofficemath/)() | Returns Office [Math](../../aspose.words.math/) object corresponded to the EQ field. |
| [get_DisplayResult](../field/get_displayresult/)() | Gets the text that represents the displayed field result. |
| [get_End](../field/get_end/)() const | Gets the node that represents the field end. |
| [get_FieldEnd](../field/get_fieldend/)() const | Gets the node that represents the field end. |
| [get_FieldStart](../field/get_fieldstart/)() const | Gets the node that represents the start of the field. |
| [get_Format](../field/get_format/)() | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting. |
| [get_IsDirty](../field/get_isdirty/)() | Gets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [get_IsLocked](../field/get_islocked/)() | Gets or sets whether the field is locked (should not recalculate its result). |
| [get_LocaleId](../field/get_localeid/)() | Gets or sets the LCID of the field. |
| [get_Result](../field/get_result/)() | Gets or sets text that is between the field separator and field end. |
| [get_Separator](../field/get_separator/)() | Gets the node that represents the field separator. Can be **null**. |
| [get_Start](../field/get_start/)() const | Gets the node that represents the start of the field. |
| virtual [get_Type](../field/get_type/)() const | Gets the Microsoft Word field type. |
| [GetFieldCode](../field/getfieldcode/)() | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Returns text between field start and field separator (or field end if there is no separator). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../field/remove/)() | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns **null**. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter for [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter for [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_Result](../field/set_result/)(const System::String\&) | Setter for [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Performs the field unlink. |
| [Update](../field/update/)() | Performs the field update. Throws if the field is being updated already. |
| [Update](../field/update/)(bool) | Performs a field update. Throws if the field is being updated already. |

## Examples



Shows how to use the EQ field to display a variety of mathematical equations. 
```cpp
void FieldEQ_()
{
    auto doc = MakeObject<Document>();
    auto builder = MakeObject<DocumentBuilder>(doc);

    // An EQ field displays a mathematical equation consisting of one or many elements.
    // Each element takes the following form: [switch][options][arguments].
    // There may be one switch, and several possible options.
    // The arguments are a set of coma-separated values enclosed by round braces.

    // Here we use a document builder to insert an EQ field, with an "\f" switch, which corresponds to "Fraction".
    // We will pass values 1 and 4 as arguments, and we will not use any options.
    // This field will display a fraction with 1 as the numerator and 4 as the denominator.
    SharedPtr<FieldEQ> field = InsertFieldEQ(builder, u"\\f(1,4)");

    ASSERT_EQ(u" EQ \\f(1,4)", field->GetFieldCode());

    // One EQ field may contain multiple elements placed sequentially.
    // We can also nest elements inside one another by placing the inner elements
    // inside the argument brackets of outer elements.
    // We can find the full list of switches, along with their uses here:
    // https://blogs.msdn.microsoft.com/murrays/2018/01/23/microsoft-word-eq-field/

    // Below are applications of nine different EQ field switches that we can use to create different kinds of objects.
    // 1 -  Array switch "\a", aligned left, 2 columns, 3 points of horizontal and vertical spacing:
    InsertFieldEQ(builder, u"\\a \\al \\co2 \\vs3 \\hs3(4x,- 4y,-4x,+ y)");

    // 2 -  Bracket switch "\b", bracket character "[", to enclose the contents in a set of square braces:
    // Note that we are nesting an array inside the brackets, which will altogether look like a matrix in the output.
    InsertFieldEQ(builder, u"\\b \\bc\\[ (\\a \\al \\co3 \\vs3 \\hs3(1,0,0,0,1,0,0,0,1))");

    // 3 -  Displacement switch "\d", displacing text "B" 30 spaces to the right of "A", displaying the gap as an underline:
    InsertFieldEQ(builder, u"A \\d \\fo30 \\li() B");

    // 4 -  Formula consisting of multiple fractions:
    InsertFieldEQ(builder, u"\\f(d,dx)(u + v) = \\f(du,dx) + \\f(dv,dx)");

    // 5 -  Integral switch "\i", with a summation symbol:
    InsertFieldEQ(builder, u"\\i \\su(n=1,5,n)");

    // 6 -  List switch "\l":
    InsertFieldEQ(builder, u"\\l(1,1,2,3,n,8,13)");

    // 7 -  Radical switch "\r", displaying a cubed root of x:
    InsertFieldEQ(builder, u"\\r (3,x)");

    // 8 -  Subscript/superscript switch "/s", first as a superscript and then as a subscript:
    InsertFieldEQ(builder, u"\\s \\up8(Superscript) Text \\s \\do8(Subscript)");

    // 9 -  Box switch "\x", with lines at the top, bottom, left and right of the input:
    InsertFieldEQ(builder, u"\\x \\to \\bo \\le \\ri(5)");

    // Some more complex combinations.
    InsertFieldEQ(builder, u"\\a \\ac \\vs1 \\co1(lim,n→∞) \\b (\\f(n,n2 + 12) + \\f(n,n2 + 22) + ... + \\f(n,n2 + n2))");
    InsertFieldEQ(builder, u"\\i (,,  \\b(\\f(x,x2 + 3x + 2))) \\s \\up10(2)");
    InsertFieldEQ(builder, u"\\i \\in( tan x, \\s \\up2(sec x), \\b(\\r(3) )\\s \\up4(t) \\s \\up7(2)  dt)");

    doc->Save(ArtifactsDir + u"Field.EQ.docx");
}

static SharedPtr<FieldEQ> InsertFieldEQ(SharedPtr<DocumentBuilder> builder, String args)
{
    auto field = System::ExplicitCast<FieldEQ>(builder->InsertField(FieldType::FieldEquation, true));
    builder->MoveTo(field->get_Separator());
    builder->Write(args);
    builder->MoveTo(field->get_Start()->get_ParentNode());

    builder->InsertParagraph();
    return field;
}
```

## See Also

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
