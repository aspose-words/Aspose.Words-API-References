---
title: FieldEQ Class
linktitle: FieldEQ
articleTitle: FieldEQ
second_title: Aspose.Words for .NET
description: Aspose.Words.Fields.FieldEQ class. Implements the EQ field in C#.
type: docs
weight: 2070
url: /net/aspose.words.fields/fieldeq/
---
## FieldEQ class

Implements the EQ field.

To learn more, visit the [Working with Fields](https://docs.aspose.com/words/net/working-with-fields/) documentation article.

```csharp
public class FieldEQ : Field
```

## Constructors

| Name | Description |
| --- | --- |
| [FieldEQ](fieldeq/)() | The default constructor. |

## Properties

| Name | Description |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Gets the text that represents the displayed field result. |
| [End](../../aspose.words.fields/field/end/) { get; } | Gets the node that represents the field end. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Gets a [`FieldFormat`](../fieldformat/) object that provides typed access to field's formatting. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Gets or sets whether the field is locked (should not recalculate its result). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Gets or sets the LCID of the field. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Gets or sets text that is between the field separator and field end. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Gets the node that represents the field separator. Can be `null`. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Gets the node that represents the start of the field. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Gets the Microsoft Word field type. |

## Methods

| Name | Description |
| --- | --- |
| [AsOfficeMath](../../aspose.words.fields/fieldeq/asofficemath/)() | Returns Office Math object corresponded to the EQ field. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Returns text between field start and field separator (or field end if there is no separator). |
| [Remove](../../aspose.words.fields/field/remove/)() | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns `null`. |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Performs the field unlink. |
| [Update](../../aspose.words.fields/field/update/)() | Performs the field update. Throws if the field is being updated already. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Performs a field update. Throws if the field is being updated already. |

## Examples

Shows how to replace the EQ field with Office Math.

```csharp
Document doc = new Document(MyDir + "Field sample - EQ.docx");
FieldEQ fieldEQ = doc.Range.Fields.OfType<FieldEQ>().First();

OfficeMath officeMath = fieldEQ.AsOfficeMath();

fieldEQ.Start.ParentNode.InsertBefore(officeMath, fieldEQ.Start);
fieldEQ.Remove();

doc.Save(ArtifactsDir + "Field.EQAsOfficeMath.docx");
```

Shows how to use the EQ field to display a variety of mathematical equations.

```csharp
public void FieldEQ()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // An EQ field displays a mathematical equation consisting of one or many elements.
    // Each element takes the following form: [switch][options][arguments].
    // There may be one switch, and several possible options.
    // The arguments are a set of coma-separated values enclosed by round braces.

    // Here we use a document builder to insert an EQ field, with an "\f" switch, which corresponds to "Fraction".
    // We will pass values 1 and 4 as arguments, and we will not use any options.
    // This field will display a fraction with 1 as the numerator and 4 as the denominator.
    FieldEQ field = InsertFieldEQ(builder, @"\f(1,4)");

    Assert.AreEqual(@" EQ \f(1,4)", field.GetFieldCode());

    // One EQ field may contain multiple elements placed sequentially.
    // We can also nest elements inside one another by placing the inner elements
    // inside the argument brackets of outer elements.
    // We can find the full list of switches, along with their uses here:
    // https://blogs.msdn.microsoft.com/murrays/2018/01/23/microsoft-word-eq-field/

    // Below are applications of nine different EQ field switches that we can use to create different kinds of objects. 
    // 1 -  Array switch "\a", aligned left, 2 columns, 3 points of horizontal and vertical spacing:
    InsertFieldEQ(builder, @"\a \al \co2 \vs3 \hs3(4x,- 4y,-4x,+ y)");

    // 2 -  Bracket switch "\b", bracket character "[", to enclose the contents in a set of square braces:
    // Note that we are nesting an array inside the brackets, which will altogether look like a matrix in the output.
    InsertFieldEQ(builder, @"\b \bc\[ (\a \al \co3 \vs3 \hs3(1,0,0,0,1,0,0,0,1))");

    // 3 -  Displacement switch "\d", displacing text "B" 30 spaces to the right of "A", displaying the gap as an underline:
    InsertFieldEQ(builder, @"A \d \fo30 \li() B");

    // 4 -  Formula consisting of multiple fractions:
    InsertFieldEQ(builder, @"\f(d,dx)(u + v) = \f(du,dx) + \f(dv,dx)");

    // 5 -  Integral switch "\i", with a summation symbol:
    InsertFieldEQ(builder, @"\i \su(n=1,5,n)");

    // 6 -  List switch "\l":
    InsertFieldEQ(builder, @"\l(1,1,2,3,n,8,13)");

    // 7 -  Radical switch "\r", displaying a cubed root of x:
    InsertFieldEQ(builder, @"\r (3,x)");

    // 8 -  Subscript/superscript switch "/s", first as a superscript and then as a subscript:
    InsertFieldEQ(builder, @"\s \up8(Superscript) Text \s \do8(Subscript)");

    // 9 -  Box switch "\x", with lines at the top, bottom, left and right of the input:
    InsertFieldEQ(builder, @"\x \to \bo \le \ri(5)");

    // Some more complex combinations.
    InsertFieldEQ(builder, @"\a \ac \vs1 \co1(lim,n→∞) \b (\f(n,n2 + 12) + \f(n,n2 + 22) + ... + \f(n,n2 + n2))");
    InsertFieldEQ(builder, @"\i (,,  \b(\f(x,x2 + 3x + 2))) \s \up10(2)");
    InsertFieldEQ(builder, @"\i \in( tan x, \s \up2(sec x), \b(\r(3) )\s \up4(t) \s \up7(2)  dt)");

    doc.Save(ArtifactsDir + "Field.EQ.docx");
}

/// <summary>
/// Use a document builder to insert an EQ field, set its arguments and start a new paragraph.
/// </summary>
private static FieldEQ InsertFieldEQ(DocumentBuilder builder, string args)
{
    FieldEQ field = (FieldEQ)builder.InsertField(FieldType.FieldEquation, true);
    builder.MoveTo(field.Separator);
    builder.Write(args);
    builder.MoveTo(field.Start.ParentNode);

    builder.InsertParagraph();
    return field;
}
```

### See Also

* class [Field](../field/)
* namespace [Aspose.Words.Fields](../../aspose.words.fields/)
* assembly [Aspose.Words](../../)
