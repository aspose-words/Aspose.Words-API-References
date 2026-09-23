---
title: "MathObjectType"
linktitle: "MathObjectType"
second_title: "Aspose.Words für Java"
description: "Gibt den Typ eines Office‑Math‑Objekts in Java an."
type: docs
weight: 459
url: /de/java/com.aspose.words/mathobjecttype/
---

**Inheritance:**
java.lang.Object
```
public class MathObjectType
```

Gibt den Typ eines Office Math-Objekts an.

 **Examples:** 

Zeigt, wie die Knotenstruktur jedes Office-Math-Knotens in einem Dokument ausgegeben wird.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [ACCENT](#ACCENT) | Akzentfunktion, bestehend aus einer Basis und einem kombinierenden diakritischen Zeichen. |
| [ARGUMENT](#ARGUMENT) | Argumentobjekt. |
| [ARRAY](#ARRAY) | Array-Objekt, bestehend aus einer oder mehreren Gleichungen, Ausdrücken oder anderen mathematischen Textabschnitten, die vertikal als Einheit in Bezug auf den umgebenden Text in der Zeile ausgerichtet werden können. |
| [BAR](#BAR) | Balkenfunktion, bestehend aus einem Basisargument und einem Überstrich oder Unterstrich. |
| [BORDER_BOX](#BORDER-BOX) | Border-Box-Objekt, bestehend aus einem Rahmen, der um eine Instanz mathematischen Textes (wie einer Formel oder Gleichung) gezeichnet wird. |
| [BOX](#BOX) | Box-Objekt, das verwendet wird, um Komponenten einer Gleichung oder einer anderen Instanz mathematischen Textes zu gruppieren. |
| [DEGREE](#DEGREE) | Grad im mathematischen Radikal. |
| [DELIMITER](#DELIMITER) | Delimiter-Objekt, bestehend aus öffnenden und schließenden Begrenzungszeichen (wie Klammern, geschweiften Klammern, eckigen Klammern und senkrechten Strichen) und einem darin enthaltenen Element. |
| [DENOMINATOR](#DENOMINATOR) | Nenner eines Bruchobjekts. |
| [FRACTION](#FRACTION) | Bruchobjekt, bestehend aus einem Zähler und einem Nenner, getrennt durch einen Bruchstrich. |
| [FUNCTION](#FUNCTION) | Function-Apply-Objekt, das aus einem Funktionsnamen und einem darauf angewendeten Argumentelement besteht. |
| [FUNCTION_NAME](#FUNCTION-NAME) | Name der Funktion. |
| [GROUP_CHARACTER](#GROUP-CHARACTER) | Group-Character-Objekt, bestehend aus einem Zeichen, das über oder unter dem Text gezeichnet wird, oft mit dem Zweck, Elemente visuell zu gruppieren. |
| [LIMIT](#LIMIT) | Untere Grenze des [LOWER\_LIMIT](../../com.aspose.words/mathobjecttype/\#LOWER-LIMIT) Objekts und die obere Grenze der [UPPER\_LIMIT](../../com.aspose.words/mathobjecttype/\#UPPER-LIMIT) Funktion. |
| [LOWER_LIMIT](#LOWER-LIMIT) | Lower-Limit-Objekt, bestehend aus Text auf der Grundlinie und verkleinertem Text unmittelbar darunter. |
| [MATRIX](#MATRIX) | Matrix-Objekt, bestehend aus einem oder mehreren Elementen, die in ein oder mehreren Zeilen und ein oder mehreren Spalten angeordnet sind. |
| [MATRIX_ROW](#MATRIX-ROW) | Einzelne Zeile der Matrix. |
| [NONE](#NONE) | Objekttyp ist nicht angegeben. |
| [NUMERATOR](#NUMERATOR) | Zähler des Fraction-Objekts. |
| [N_ARY](#N-ARY) | N-ary-Objekt, bestehend aus einem n-ary-Objekt, einer Basis (oder Operanden) und optionalen oberen und unteren Grenzen. |
| [O_MATH](#O-MATH) | Instanz mathematischen Textes. |
| [O_MATH_PARA](#O-MATH-PARA) | Mathematikabsatz oder Anzeigemathzone, die ein oder mehrere [O\_MATH](../../com.aspose.words/mathobjecttype/\#O-MATH) Elemente enthält, die im Anzeigemodus sind. |
| [PHANTOM](#PHANTOM) | Phantom-Objekt. |
| [PRE_SUB_SUPERSCRIPT](#PRE-SUB-SUPERSCRIPT) | Pre-Sub-Superscript-Objekt, das aus einem Basiselement sowie einem tief- und hochgestellten Index besteht, die links vom Basiselement platziert sind. |
| [RADICAL](#RADICAL) | Radikal-Objekt, bestehend aus einem Radikal, einem Basiselement und einem optionalen Grad. |
| [SUBSCRIPT](#SUBSCRIPT) | Subskript-Objekt, das aus einem Basiselement und einem verkleinerten Skript besteht, das unten rechts platziert ist. |
| [SUBSCRIPT_PART](#SUBSCRIPT-PART) | Subskript des Objekts, das einen Subskript-Teil haben kann. |
| [SUB_SUPERSCRIPT](#SUB-SUPERSCRIPT) | Sub‑Superskript-Objekt, das aus einem Basiselement, einem verkleinerten Skript unten rechts und einem verkleinerten Skript oben rechts besteht. |
| [SUPERSCRIPT](#SUPERSCRIPT) | Superskript-Objekt, das aus einem Basiselement und einem verkleinerten Skript oben rechts besteht. |
| [SUPERSCRIPT_PART](#SUPERSCRIPT-PART) | Superskript des Superskript-Objekts. |
| [UPPER_LIMIT](#UPPER-LIMIT) | Obergrenzen‑Objekt, das aus Text auf der Grundlinie und verkleinertem Text unmittelbar darüber besteht. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String mathObjectTypeName)](#fromName-java.lang.String) |  |
| [getName(int mathObjectType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int mathObjectType)](#toString-int) |  |
### ACCENT {#ACCENT}
```
public static int ACCENT
```


Akzentfunktion, bestehend aus einer Basis und einem kombinierenden diakritischen Zeichen.

### ARGUMENT {#ARGUMENT}
```
public static int ARGUMENT
```


Argument‑Objekt. Umschließt Office‑Math‑Entitäten, wenn sie als Argumente für andere Office‑Math‑Entitäten verwendet werden.

### ARRAY {#ARRAY}
```
public static int ARRAY
```


Array-Objekt, bestehend aus einer oder mehreren Gleichungen, Ausdrücken oder anderen mathematischen Textabschnitten, die vertikal als Einheit in Bezug auf den umgebenden Text in der Zeile ausgerichtet werden können.

### BAR {#BAR}
```
public static int BAR
```


Balkenfunktion, bestehend aus einem Basisargument und einem Überstrich oder Unterstrich.

### BORDER_BOX {#BORDER-BOX}
```
public static int BORDER_BOX
```


Border-Box-Objekt, bestehend aus einem Rahmen, der um eine Instanz mathematischen Textes (wie einer Formel oder Gleichung) gezeichnet wird.

### BOX {#BOX}
```
public static int BOX
```


Box-Objekt, das verwendet wird, um Komponenten einer Gleichung oder einer anderen Instanz mathematischen Textes zu gruppieren.

### DEGREE {#DEGREE}
```
public static int DEGREE
```


Grad im mathematischen Radikal.

### DELIMITER {#DELIMITER}
```
public static int DELIMITER
```


Delimiter-Objekt, bestehend aus öffnenden und schließenden Begrenzungszeichen (wie Klammern, geschweiften Klammern, eckigen Klammern und senkrechten Strichen) und einem darin enthaltenen Element.

### DENOMINATOR {#DENOMINATOR}
```
public static int DENOMINATOR
```


Nenner eines Bruchobjekts.

### FRACTION {#FRACTION}
```
public static int FRACTION
```


Bruchobjekt, bestehend aus einem Zähler und einem Nenner, getrennt durch einen Bruchstrich.

### FUNCTION {#FUNCTION}
```
public static int FUNCTION
```


Function-Apply-Objekt, das aus einem Funktionsnamen und einem darauf angewendeten Argumentelement besteht.

### FUNCTION_NAME {#FUNCTION-NAME}
```
public static int FUNCTION_NAME
```


Name der Funktion. Zum Beispiel sind Funktionsnamen sin und cos.

### GROUP_CHARACTER {#GROUP-CHARACTER}
```
public static int GROUP_CHARACTER
```


Group-Character-Objekt, bestehend aus einem Zeichen, das über oder unter dem Text gezeichnet wird, oft mit dem Zweck, Elemente visuell zu gruppieren.

### LIMIT {#LIMIT}
```
public static int LIMIT
```


Untere Grenze des [LOWER\_LIMIT](../../com.aspose.words/mathobjecttype/\#LOWER-LIMIT) Objekts und die obere Grenze der [UPPER\_LIMIT](../../com.aspose.words/mathobjecttype/\#UPPER-LIMIT) Funktion.

### LOWER_LIMIT {#LOWER-LIMIT}
```
public static int LOWER_LIMIT
```


Lower-Limit-Objekt, bestehend aus Text auf der Grundlinie und verkleinertem Text unmittelbar darunter.

### MATRIX {#MATRIX}
```
public static int MATRIX
```


Matrix-Objekt, bestehend aus einem oder mehreren Elementen, die in ein oder mehreren Zeilen und ein oder mehreren Spalten angeordnet sind.

### MATRIX_ROW {#MATRIX-ROW}
```
public static int MATRIX_ROW
```


Einzelne Zeile der Matrix.

### NONE {#NONE}
```
public static int NONE
```


Objekttyp ist nicht angegeben.

### NUMERATOR {#NUMERATOR}
```
public static int NUMERATOR
```


Zähler des Fraction-Objekts.

### N_ARY {#N-ARY}
```
public static int N_ARY
```


N-ary-Objekt, bestehend aus einem n-ary-Objekt, einer Basis (oder Operanden) und optionalen oberen und unteren Grenzen.

### O_MATH {#O-MATH}
```
public static int O_MATH
```


Instanz mathematischen Textes.

### O_MATH_PARA {#O-MATH-PARA}
```
public static int O_MATH_PARA
```


Mathematikabsatz oder Anzeigemathzone, die ein oder mehrere [O\_MATH](../../com.aspose.words/mathobjecttype/\#O-MATH) Elemente enthält, die im Anzeigemodus sind.

### PHANTOM {#PHANTOM}
```
public static int PHANTOM
```


Phantom-Objekt.

### PRE_SUB_SUPERSCRIPT {#PRE-SUB-SUPERSCRIPT}
```
public static int PRE_SUB_SUPERSCRIPT
```


Pre-Sub-Superscript-Objekt, das aus einem Basiselement sowie einem tief- und hochgestellten Index besteht, die links vom Basiselement platziert sind.

### RADICAL {#RADICAL}
```
public static int RADICAL
```


Radikal-Objekt, bestehend aus einem Radikal, einem Basiselement und einem optionalen Grad.

### SUBSCRIPT {#SUBSCRIPT}
```
public static int SUBSCRIPT
```


Subskript-Objekt, das aus einem Basiselement und einem verkleinerten Skript besteht, das unten rechts platziert ist.

### SUBSCRIPT_PART {#SUBSCRIPT-PART}
```
public static int SUBSCRIPT_PART
```


Subskript des Objekts, das einen Subskript-Teil haben kann.

### SUB_SUPERSCRIPT {#SUB-SUPERSCRIPT}
```
public static int SUB_SUPERSCRIPT
```


Sub‑Superskript-Objekt, das aus einem Basiselement, einem verkleinerten Skript unten rechts und einem verkleinerten Skript oben rechts besteht.

### SUPERSCRIPT {#SUPERSCRIPT}
```
public static int SUPERSCRIPT
```


Superskript-Objekt, das aus einem Basiselement und einem verkleinerten Skript oben rechts besteht.

### SUPERSCRIPT_PART {#SUPERSCRIPT-PART}
```
public static int SUPERSCRIPT_PART
```


Superskript des Superskript-Objekts.

### UPPER_LIMIT {#UPPER-LIMIT}
```
public static int UPPER_LIMIT
```


Obergrenzen‑Objekt, das aus Text auf der Grundlinie und verkleinertem Text unmittelbar darüber besteht.

### length {#length}
```
public static int length
```


### fromName(String mathObjectTypeName) {#fromName-java.lang.String}
```
public static int fromName(String mathObjectTypeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| mathObjectTypeName | java.lang.String |  |

**Returns:**
int
### getName(int mathObjectType) {#getName-int}
```
public static String getName(int mathObjectType)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| mathObjectType | int |  |

**Returns:**
java.lang.String
