---
title: MathObjectType
linktitle: MathObjectType
second_title: Aspose.Words for Java
description: Specifies type of an Office Math object in Java.
type: docs
weight: 444
url: /java/com.aspose.words/mathobjecttype/
---

**Inheritance:**
java.lang.Object
```
public class MathObjectType
```

Specifies type of an Office Math object.

 **Examples:** 

Shows how to print the node structure of every office math node in a document.

```

 public void officeMathToText() throws Exception {
     Document doc = new Document(getMyDir() + "DocumentVisitor-compatible features.docx");
     OfficeMathStructurePrinter visitor = new OfficeMathStructurePrinter();

     // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
     // and then traverses all the node's children in a depth-first manner.
     // The visitor can read and modify each visited node.
     doc.accept(visitor);

     System.out.println(visitor.getText());
 }

 /// 
 /// Traverses a node's non-binary tree of child nodes.
 /// Creates a map in the form of a string of all encountered OfficeMath nodes and their children.
 /// 
 public static class OfficeMathStructurePrinter extends DocumentVisitor {
     public OfficeMathStructurePrinter() {
         mBuilder = new StringBuilder();
         mVisitorIsInsideOfficeMath = false;
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// 
     public int visitRun(final Run run) {
         if (mVisitorIsInsideOfficeMath) {
             indentAndAppendLine("[Run] \"" + run.getText() + "\"");
         }

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when an OfficeMath node is encountered in the document.
     /// 
     public int visitOfficeMathStart(final OfficeMath officeMath) {
         indentAndAppendLine("[OfficeMath start] Math object type: " + officeMath.getMathObjectType());
         mDocTraversalDepth++;
         mVisitorIsInsideOfficeMath = true;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of an OfficeMath node have been visited.
     /// 
     public int visitOfficeMathEnd(final OfficeMath officeMath) {
         mDocTraversalDepth--;
         indentAndAppendLine("[OfficeMath end]");
         mVisitorIsInsideOfficeMath = false;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Append a line to the StringBuilder and indent it depending on how deep the visitor is into the document tree.
     /// 
     /// 
     private void indentAndAppendLine(final String text) {
         for (int i = 0; i < mDocTraversalDepth; i++) {
             mBuilder.append("|  ");
         }

         mBuilder.append(text + "\r\n");
     }

     private boolean mVisitorIsInsideOfficeMath;
     private int mDocTraversalDepth;
     private final StringBuilder mBuilder;
 }
 
```
## Fields

| Field | Description |
| --- | --- |
| [ACCENT](#ACCENT) | Accent function, consisting of a base and a combining diacritical mark. |
| [ARGUMENT](#ARGUMENT) | Argument object. |
| [ARRAY](#ARRAY) | Array object, consisting of one or more equations, expressions, or other mathematical text runs that can be vertically justified as a unit with respect to surrounding text on the line. |
| [BAR](#BAR) | Bar function, consisting of a base argument and an overbar or underbar. |
| [BORDER_BOX](#BORDER-BOX) | Border Box object, consisting of a border drawn around an instance of mathematical text (such as a formula or equation) |
| [BOX](#BOX) | Box object, which is used to group components of an equation or other instance of mathematical text. |
| [DEGREE](#DEGREE) | Degree in the mathematical radical. |
| [DELIMITER](#DELIMITER) | Delimiter object, consisting of opening and closing delimiters (such as parentheses, braces, brackets, and vertical bars), and an element contained inside. |
| [DENOMINATOR](#DENOMINATOR) | Denominator of a fraction object. |
| [FRACTION](#FRACTION) | Fraction object, consisting of a numerator and denominator separated by a fraction bar. |
| [FUNCTION](#FUNCTION) | Function-Apply object, which consists of a function name and an argument element acted upon. |
| [FUNCTION_NAME](#FUNCTION-NAME) | Name of the function. |
| [GROUP_CHARACTER](#GROUP-CHARACTER) | Group-Character object, consisting of a character drawn above or below text, often with the purpose of visually grouping items |
| [LIMIT](#LIMIT) | Lower limit of the [LOWER\_LIMIT](../../com.aspose.words/mathobjecttype/\#LOWER-LIMIT) object and the upper limit of the [UPPER\_LIMIT](../../com.aspose.words/mathobjecttype/\#UPPER-LIMIT) function. |
| [LOWER_LIMIT](#LOWER-LIMIT) | Lower-Limit object, consisting of text on the baseline and reduced-size text immediately below it. |
| [MATRIX](#MATRIX) | Matrix object, consisting of one or more elements laid out in one or more rows and one or more columns. |
| [MATRIX_ROW](#MATRIX-ROW) | Single row of the matrix. |
| [NUMERATOR](#NUMERATOR) | Numerator of the Fraction object. |
| [N_ARY](#N-ARY) | N-ary object, consisting of an n-ary object, a base (or operand), and optional upper and lower limits. |
| [O_MATH](#O-MATH) | Instance of mathematical text. |
| [O_MATH_PARA](#O-MATH-PARA) | Math paragraph, or display math zone, that contains one or more [O\_MATH](../../com.aspose.words/mathobjecttype/\#O-MATH) elements that are in display mode. |
| [PHANTOM](#PHANTOM) | Phantom object. |
| [PRE_SUB_SUPERSCRIPT](#PRE-SUB-SUPERSCRIPT) | Pre-Sub-Superscript object, which consists of a base element and a subscript and superscript placed to the left of the base. |
| [RADICAL](#RADICAL) | Radical object, consisting of a radical, a base element, and an optional degree . |
| [SUBSCRIPT](#SUBSCRIPT) | Subscript object, which consists of a base element and a reduced-size script placed below and to the right. |
| [SUBSCRIPT_PART](#SUBSCRIPT-PART) | Subscript of the object that can have subscript part. |
| [SUB_SUPERSCRIPT](#SUB-SUPERSCRIPT) | Sub-superscript object, which consists of a base element, a reduced-size script placed below and to the right, and a reduced-size script placed above and to the right. |
| [SUPERCRIPT](#SUPERCRIPT) | Superscript object, which consists of a base element and a reduced-size script placed above and to the right. |
| [SUPERSCRIPT_PART](#SUPERSCRIPT-PART) | Superscript of the superscript object. |
| [UPPER_LIMIT](#UPPER-LIMIT) | Upper-Limit object, consisting of text on the baseline and reduced-size text immediately above it. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String mathObjectTypeName)](#fromName-java.lang.String) |  |
| [getName(int mathObjectType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int mathObjectType)](#toString-int) |  |
### ACCENT {#ACCENT}
```
public static int ACCENT
```


Accent function, consisting of a base and a combining diacritical mark.

### ARGUMENT {#ARGUMENT}
```
public static int ARGUMENT
```


Argument object. Encloses Office Math entities when they are used as arguments to other Office Math entities.

### ARRAY {#ARRAY}
```
public static int ARRAY
```


Array object, consisting of one or more equations, expressions, or other mathematical text runs that can be vertically justified as a unit with respect to surrounding text on the line.

### BAR {#BAR}
```
public static int BAR
```


Bar function, consisting of a base argument and an overbar or underbar.

### BORDER_BOX {#BORDER-BOX}
```
public static int BORDER_BOX
```


Border Box object, consisting of a border drawn around an instance of mathematical text (such as a formula or equation)

### BOX {#BOX}
```
public static int BOX
```


Box object, which is used to group components of an equation or other instance of mathematical text.

### DEGREE {#DEGREE}
```
public static int DEGREE
```


Degree in the mathematical radical.

### DELIMITER {#DELIMITER}
```
public static int DELIMITER
```


Delimiter object, consisting of opening and closing delimiters (such as parentheses, braces, brackets, and vertical bars), and an element contained inside.

### DENOMINATOR {#DENOMINATOR}
```
public static int DENOMINATOR
```


Denominator of a fraction object.

### FRACTION {#FRACTION}
```
public static int FRACTION
```


Fraction object, consisting of a numerator and denominator separated by a fraction bar.

### FUNCTION {#FUNCTION}
```
public static int FUNCTION
```


Function-Apply object, which consists of a function name and an argument element acted upon.

### FUNCTION_NAME {#FUNCTION-NAME}
```
public static int FUNCTION_NAME
```


Name of the function. For example, function names are sin and cos.

### GROUP_CHARACTER {#GROUP-CHARACTER}
```
public static int GROUP_CHARACTER
```


Group-Character object, consisting of a character drawn above or below text, often with the purpose of visually grouping items

### LIMIT {#LIMIT}
```
public static int LIMIT
```


Lower limit of the [LOWER\_LIMIT](../../com.aspose.words/mathobjecttype/\#LOWER-LIMIT) object and the upper limit of the [UPPER\_LIMIT](../../com.aspose.words/mathobjecttype/\#UPPER-LIMIT) function.

### LOWER_LIMIT {#LOWER-LIMIT}
```
public static int LOWER_LIMIT
```


Lower-Limit object, consisting of text on the baseline and reduced-size text immediately below it.

### MATRIX {#MATRIX}
```
public static int MATRIX
```


Matrix object, consisting of one or more elements laid out in one or more rows and one or more columns.

### MATRIX_ROW {#MATRIX-ROW}
```
public static int MATRIX_ROW
```


Single row of the matrix.

### NUMERATOR {#NUMERATOR}
```
public static int NUMERATOR
```


Numerator of the Fraction object.

### N_ARY {#N-ARY}
```
public static int N_ARY
```


N-ary object, consisting of an n-ary object, a base (or operand), and optional upper and lower limits.

### O_MATH {#O-MATH}
```
public static int O_MATH
```


Instance of mathematical text.

### O_MATH_PARA {#O-MATH-PARA}
```
public static int O_MATH_PARA
```


Math paragraph, or display math zone, that contains one or more [O\_MATH](../../com.aspose.words/mathobjecttype/\#O-MATH) elements that are in display mode.

### PHANTOM {#PHANTOM}
```
public static int PHANTOM
```


Phantom object.

### PRE_SUB_SUPERSCRIPT {#PRE-SUB-SUPERSCRIPT}
```
public static int PRE_SUB_SUPERSCRIPT
```


Pre-Sub-Superscript object, which consists of a base element and a subscript and superscript placed to the left of the base.

### RADICAL {#RADICAL}
```
public static int RADICAL
```


Radical object, consisting of a radical, a base element, and an optional degree .

### SUBSCRIPT {#SUBSCRIPT}
```
public static int SUBSCRIPT
```


Subscript object, which consists of a base element and a reduced-size script placed below and to the right.

### SUBSCRIPT_PART {#SUBSCRIPT-PART}
```
public static int SUBSCRIPT_PART
```


Subscript of the object that can have subscript part.

### SUB_SUPERSCRIPT {#SUB-SUPERSCRIPT}
```
public static int SUB_SUPERSCRIPT
```


Sub-superscript object, which consists of a base element, a reduced-size script placed below and to the right, and a reduced-size script placed above and to the right.

### SUPERCRIPT {#SUPERCRIPT}
```
public static int SUPERCRIPT
```


Superscript object, which consists of a base element and a reduced-size script placed above and to the right.

### SUPERSCRIPT_PART {#SUPERSCRIPT-PART}
```
public static int SUPERSCRIPT_PART
```


Superscript of the superscript object.

### UPPER_LIMIT {#UPPER-LIMIT}
```
public static int UPPER_LIMIT
```


Upper-Limit object, consisting of text on the baseline and reduced-size text immediately above it.

### length {#length}
```
public static int length
```


### fromName(String mathObjectTypeName) {#fromName-java.lang.String}
```
public static int fromName(String mathObjectTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| mathObjectTypeName | java.lang.String |  |

**Returns:**
int
### getName(int mathObjectType) {#getName-int}
```
public static String getName(int mathObjectType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| mathObjectType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int mathObjectType) {#toString-int}
```
public static String toString(int mathObjectType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| mathObjectType | int |  |

**Returns:**
java.lang.String
