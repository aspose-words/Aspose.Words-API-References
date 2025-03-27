---
title: MathObjectType enumeration
linktitle: MathObjectType enumeration
articleTitle: MathObjectType enumeration
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Math.MathObjectType enumeration. Specifies type of an Office Math object."
type: docs
weight: 10
url: /nodejs-net/Aspose.Words.Math/mathobjecttype/
---

## MathObjectType enumeration

Specifies type of an Office Math object.


### Members

| Name | Description |
| --- | --- |
| OMath | Instance of mathematical text. |
| OMathPara | Math paragraph, or display math zone, that contains one or more [MathObjectType.OMath](./#OMath) elements that are in display mode. |
| Accent | Accent function, consisting of a base and a combining diacritical mark. |
| Bar | Bar function, consisting of a base argument and an overbar or underbar. |
| BorderBox | Border Box object, consisting of a border drawn around an instance of mathematical text (such as a formula or equation) |
| Box | Box object, which is used to group components of an equation or other instance of mathematical text. |
| Delimiter | Delimiter object, consisting of opening and closing delimiters (such as parentheses,  braces, brackets, and vertical bars), and an element contained inside. |
| Degree | Degree in the mathematical radical. |
| Argument | Argument object. Encloses Office Math entities when they are used as arguments to other Office Math entities. |
| Array | Array object, consisting of one or more equations, expressions, or other mathematical text runs  that can be vertically justified as a unit with respect to surrounding text on the line. |
| Fraction | Fraction object, consisting of a numerator and denominator separated by a fraction bar. |
| Denominator | Denominator of a fraction object. |
| Numerator | Numerator of the Fraction object. |
| Function | Function-Apply object, which consists of a function name and an argument element acted upon. |
| FunctionName | Name of the function. For example, function names are sin and cos. |
| GroupCharacter | Group-Character object, consisting of a character drawn above or below text, often  with the purpose of visually grouping items |
| Limit | Lower limit of the [MathObjectType.LowerLimit](./#LowerLimit) object and  the upper limit of the [MathObjectType.UpperLimit](./#UpperLimit) function. |
| LowerLimit | Lower-Limit object, consisting of text on the baseline and reduced-size text immediately below it. |
| UpperLimit | Upper-Limit object, consisting of text on the baseline and reduced-size text immediately above it. |
| Matrix | Matrix object, consisting of one or more elements laid out in one or more rows and one or more columns. |
| MatrixRow | Single row of the matrix. |
| NAry | N-ary object, consisting of an n-ary object, a base (or operand), and optional upper and lower limits. |
| Phantom | Phantom object. |
| Radical | Radical object, consisting of a radical, a base element, and an optional degree . |
| SubscriptPart | Subscript of the object that can have subscript part. |
| SuperscriptPart | Superscript of the superscript object. |
| PreSubSuperscript | Pre-Sub-Superscript object, which consists of a base element and a subscript and superscript placed to the left of the base. |
| Subscript | Subscript object, which consists of a base element and a reduced-size script placed below and to the right. |
| SubSuperscript | Sub-superscript object, which consists of a base element, a reduced-size script placed below and to the right, and a reduced-size script placed above and to the right. |
| Supercript | Superscript object, which consists of a base element and a reduced-size script placed above and to the right. |

### Examples

Shows how to print the node structure of every office math node in a document.

```js
test('OfficeMathToText', () => {
  let doc = new aw.Document(base.myDir + "DocumentVisitor-compatible features.docx");
  let visitor = new OfficeMathStructurePrinter();

  // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
  // and then traverses all the node's children in a depth-first manner.
  // The visitor can read and modify each visited node.
  doc.accept(visitor);

  console.log(visitor.getText());
});


  /// <summary>
  /// Traverses a node's non-binary tree of child nodes.
  /// Creates a map in the form of a string of all encountered OfficeMath nodes and their children.
  /// </summary>
public class OfficeMathStructurePrinter : DocumentVisitor
{
  public OfficeMathStructurePrinter()
  {
    mBuilder = new StringBuilder();
    mVisitorIsInsideOfficeMath = false;
  }

    /// <summary>
    /// Gets the plain text of the document that was accumulated by the visitor.
    /// </summary>
  public string GetText()
  {
    return mBuilder.toString();
  }

    /// <summary>
    /// Called when a Run node is encountered in the document.
    /// </summary>
  public override VisitorAction VisitRun(Run run)
  {
    if (mVisitorIsInsideOfficeMath) IndentAndAppendLine("[Run] \"" + run.getText() + "\"");

    return aw.VisitorAction.Continue;
  }

    /// <summary>
    /// Called when an OfficeMath node is encountered in the document.
    /// </summary>
  public override VisitorAction VisitOfficeMathStart(OfficeMath officeMath)
  {
    IndentAndAppendLine("[OfficeMath start] Math object type: " + officeMath.mathObjectType);
    mDocTraversalDepth++;
    mVisitorIsInsideOfficeMath = true;

    return aw.VisitorAction.Continue;
  }

    /// <summary>
    /// Called after all the child nodes of an OfficeMath node have been visited.
    /// </summary>
  public override VisitorAction VisitOfficeMathEnd(OfficeMath officeMath)
  {
    mDocTraversalDepth--;
    IndentAndAppendLine("[OfficeMath end]");
    mVisitorIsInsideOfficeMath = false;

    return aw.VisitorAction.Continue;
  }

    /// <summary>
    /// Append a line to the StringBuilder and indent it depending on how deep the visitor is into the document tree.
    /// </summary>
    /// <param name="text"></param>
  private void IndentAndAppendLine(string text)
  {
    for (let i = 0; i < mDocTraversalDepth; i++) mBuilder.append("|  ");

    mBuilder.AppendLine(text);
  }

  private bool mVisitorIsInsideOfficeMath;
  private int mDocTraversalDepth;
  private readonly StringBuilder mBuilder;
}
```

### See Also

* module [Aspose.Words.Math](../)

