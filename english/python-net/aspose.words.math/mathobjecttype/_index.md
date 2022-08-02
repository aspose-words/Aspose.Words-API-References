---
title: MathObjectType enumeration
second_title: Aspose.Words for Python via .NET API Reference
description: "Specifies type of an Office Math object."
type: docs
weight: 10
url: /python-net/aspose.words.math/mathobjecttype/
---

## MathObjectType enumeration

Specifies type of an Office Math object.


### Members

| Name | Description |
| --- | --- |
| O_MATH | Instance of mathematical text. |
| O_MATH_PARA | Math paragraph, or display math zone, that contains one or more [MathObjectType.O_MATH](./#O_MATH) elements that are in display mode. |
| ACCENT | Accent function, consisting of a base and a combining diacritical mark. |
| BAR | Bar function, consisting of a base argument and an overbar or underbar. |
| BORDER_BOX | Border Box object, consisting of a border drawn around an instance of mathematical text (such as a formula or equation) |
| BOX | Box object, which is used to group components of an equation or other instance of mathematical text. |
| DELIMITER | Delimiter object, consisting of opening and closing delimiters (such as parentheses,  braces, brackets, and vertical bars), and an element contained inside. |
| DEGREE | Degree in the mathematical radical. |
| ARGUMENT | Argument object. Encloses Office Math entities when they are used as arguments to other Office Math entities. |
| ARRAY | Array object, consisting of one or more equations, expressions, or other mathematical text runs  that can be vertically justified as a unit with respect to surrounding text on the line. |
| FRACTION | Fraction object, consisting of a numerator and denominator separated by a fraction bar. |
| DENOMINATOR | Denominator of a fraction object. |
| NUMERATOR | Numerator of the Fraction object. |
| FUNCTION | Function-Apply object, which consists of a function name and an argument element acted upon. |
| FUNCTION_NAME | Name of the function. For example, function names are sin and cos. |
| GROUP_CHARACTER | Group-Character object, consisting of a character drawn above or below text, often  with the purpose of visually grouping items |
| LIMIT | Lower limit of the [MathObjectType.LOWER_LIMIT](./#LOWER_LIMIT) object and  the upper limit of the [MathObjectType.UPPER_LIMIT](./#UPPER_LIMIT) function. |
| LOWER_LIMIT | Lower-Limit object, consisting of text on the baseline and reduced-size text immediately below it. |
| UPPER_LIMIT | Upper-Limit object, consisting of text on the baseline and reduced-size text immediately above it. |
| MATRIX | Matrix object, consisting of one or more elements laid out in one or more rows and one or more columns. |
| MATRIX_ROW | Single row of the matrix. |
| N_ARY | N-ary object, consisting of an n-ary object, a base (or operand), and optional upper and lower limits. |
| PHANTOM | Phantom object. |
| RADICAL | Radical object, consisting of a radical, a base element, and an optional degree . |
| SUBSCRIPT_PART | Subscript of the object that can have subscript part. |
| SUPERSCRIPT_PART | Superscript of the superscript object. |
| PRE_SUB_SUPERSCRIPT | Pre-Sub-Superscript object, which consists of a base element and a subscript and superscript placed to the left of the base. |
| SUBSCRIPT | Subscript object, which consists of a base element and a reduced-size script placed below and to the right. |
| SUB_SUPERSCRIPT | Sub-superscript object, which consists of a base element, a reduced-size script placed below and to the right, and a reduced-size script placed above and to the right. |
| SUPERCRIPT | Superscript object, which consists of a base element and a reduced-size script placed above and to the right. |

### Examples

Shows how to print the node structure of every office math node in a document.

```python
def test_office_math_to_text(self):

    doc = aw.Document(MY_DIR + "DocumentVisitor-compatible features.docx")
    visitor = ExDocumentVisitor.OfficeMathStructurePrinter()

    # When we get a composite node to accept a document visitor, the visitor visits the accepting node,
    # and then traverses all the node's children in a depth-first manner.
    # The visitor can read and modify each visited node.
    doc.accept(visitor)

    print(visitor.get_text())

class OfficeMathStructurePrinter(aw.DocumentVisitor):
    """Traverses a node's non-binary tree of child nodes.
    Creates a map in the form of a string of all encountered OfficeMath nodes and their children."""

    def __init__(self):

        aw.DocumentVisitor.__init__(self)

        self.builder = io.StringIO()
        self.visitor_is_inside_office_math = False
        self.doc_traversal_depth = 0

    def get_text(self) -> str:
        """Gets the plain text of the document that was accumulated by the visitor."""

        return self.builder.getvalue()

    def visit_run(self, run: aw.Run) -> aw.VisitorAction:
        """Called when a Run node is encountered in the document."""

        if self.visitor_is_inside_office_math:
            self._indent_and_append_line("[Run] \"" + run.get_text() + "\"")

        return aw.VisitorAction.CONTINUE

    def visit_office_math_start(self, office_math: aw.OfficeMath) -> aw.VisitorAction:
        """Called when an OfficeMath node is encountered in the document."""

        self._indent_and_append_line("[OfficeMath start] Math object type: " + office_math.math_object_type)
        self.doc_traversal_depth += 1
        self.visitor_is_inside_office_math = True

        return aw.VisitorAction.CONTINUE

    def visit_office_math_end(self, office_math: aw.OfficeMath) -> aw.VisitorAction:
        """Called after all the child nodes of an OfficeMath node have been visited."""

        self.doc_traversal_depth -= 1
        self._indent_and_append_line("[OfficeMath end]")
        self.visitor_is_inside_office_math = False

        return aw.VisitorAction.CONTINUE

    def _indent_and_append_line(self, text: str):
        """Append a line to the StringBuilder and indent it depending on how deep the visitor is into the document tree."""

        for i in range(self.doc_traversal_depth):
            self.builder.write("|  ")

        self.builder.write(text + "\n")
```

### See Also

* module [aspose.words.math](../)

