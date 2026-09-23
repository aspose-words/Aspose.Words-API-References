---
title: "MathObjectType"
linktitle: "MathObjectType"
second_title: "Aspose.Words для Java"
description: "Указывает тип объекта Office Math в Java."
type: docs
weight: 459
url: /ru/java/com.aspose.words/mathobjecttype/
---

**Inheritance:**
java.lang.Object
```
public class MathObjectType
```

Указывает тип объекта Office Math.

 **Examples:** 

Показывает, как вывести структуру узлов каждого узла Office Math в документе.

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
## Поля

| Поле | Описание |
| --- | --- |
| [ACCENT](#ACCENT) | Функция акцента, состоящая из основы и комбинируемого диакритического знака. |
| [ARGUMENT](#ARGUMENT) | Объект аргумента. |
| [ARRAY](#ARRAY) | Объект массива, состоящий из одного или нескольких уравнений, выражений или других фрагментов математического текста, которые могут быть вертикально выровнены как единое целое относительно окружающего текста в строке. |
| [BAR](#BAR) | Функция черты, состоящая из базового аргумента и надчерты или подчерты. |
| [BORDER_BOX](#BORDER-BOX) | Объект рамки (Border Box), состоящий из границы, нарисованной вокруг экземпляра математического текста (например, формулы или уравнения). |
| [BOX](#BOX) | Объект коробки, используемый для группировки компонентов уравнения или другого экземпляра математического текста. |
| [DEGREE](#DEGREE) | Степень в математическом радикале. |
| [DELIMITER](#DELIMITER) | Объект разделителя, состоящий из открывающих и закрывающих разделителей (например, скобок, фигурных скобок, квадратных скобок и вертикальных черт) и содержащегося внутри элемента. |
| [DENOMINATOR](#DENOMINATOR) | Знаменатель объекта дроби. |
| [FRACTION](#FRACTION) | Объект дроби, состоящий из числителя и знаменателя, разделённых чертой дроби. |
| [FUNCTION](#FUNCTION) | Объект применения функции (Function-Apply), который состоит из имени функции и аргументного элемента, к которому применяется действие. |
| [FUNCTION_NAME](#FUNCTION-NAME) | Имя функции. |
| [GROUP_CHARACTER](#GROUP-CHARACTER) | Объект группирующего символа (Group-Character), состоящий из символа, размещённого над или под текстом, часто с целью визуального объединения элементов. |
| [LIMIT](#LIMIT) | Нижний предел объекта [LOWER\\_LIMIT](../../com.aspose.words/mathobjecttype/\\#LOWER-LIMIT) и верхний предел функции [UPPER\\_LIMIT](../../com.aspose.words/mathobjecttype/\\#UPPER-LIMIT). |
| [LOWER_LIMIT](#LOWER-LIMIT) | Объект нижнего предела (Lower-Limit), состоящий из текста на базовой линии и уменьшенного текста непосредственно под ним. |
| [MATRIX](#MATRIX) | Объект матрицы, состоящий из одного или нескольких элементов, расположенных в одной или нескольких строках и одной или нескольких колонках. |
| [MATRIX_ROW](#MATRIX-ROW) | Одна строка матрицы. |
| [NONE](#NONE) | Тип объекта не указан. |
| [NUMERATOR](#NUMERATOR) | Числитель объекта дроби. |
| [N_ARY](#N-ARY) | Объект n-арный, состоящий из n-арного объекта, базы (или операнда) и необязательных верхних и нижних пределов. |
| [O_MATH](#O-MATH) | Экземпляр математического текста. |
| [O_MATH_PARA](#O-MATH-PARA) | Математический абзац или зона отображения математики, содержащая один или несколько элементов [O\\_MATH](../../com.aspose.words/mathobjecttype/\\#O-MATH) в режиме отображения. |
| [PHANTOM](#PHANTOM) | Фантомный объект. |
| [PRE_SUB_SUPERSCRIPT](#PRE-SUB-SUPERSCRIPT) | Объект предварительного под- и надстрочного (Pre-Sub-Superscript), который состоит из базового элемента и подстрочного и надстрочного индексов, размещённых слева от базы. |
| [RADICAL](#RADICAL) | Радикальный объект, состоящий из радикала, базового элемента и необязательной степени. |
| [SUBSCRIPT](#SUBSCRIPT) | Объект нижнего индекса, который состоит из базового элемента и уменьшенного скрипта, размещённого ниже и справа. |
| [SUBSCRIPT_PART](#SUBSCRIPT-PART) | Нижний индекс объекта, который может иметь часть в виде нижнего индекса. |
| [SUB_SUPERSCRIPT](#SUB-SUPERSCRIPT) | Объект под-надстрочного индекса, который состоит из базового элемента, уменьшенного скрипта, размещённого ниже и справа, и уменьшенного скрипта, размещённого выше и справа. |
| [SUPERSCRIPT](#SUPERSCRIPT) | Объект верхнего индекса, который состоит из базового элемента и уменьшенного скрипта, размещённого выше и справа. |
| [SUPERSCRIPT_PART](#SUPERSCRIPT-PART) | Верхний индекс объекта верхнего индекса. |
| [UPPER_LIMIT](#UPPER-LIMIT) | Объект верхнего предела, состоящий из текста на базовой линии и уменьшенного текста непосредственно над ним. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String mathObjectTypeName)](#fromName-java.lang.String) |  |
| [getName(int mathObjectType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int mathObjectType)](#toString-int) |  |
### ACCENT {#ACCENT}
```
public static int ACCENT
```


Функция акцента, состоящая из основы и комбинируемого диакритического знака.

### ARGUMENT {#ARGUMENT}
```
public static int ARGUMENT
```


Объект аргумента. Охватывает сущности Office Math, когда они используются в качестве аргументов для других сущностей Office Math.

### ARRAY {#ARRAY}
```
public static int ARRAY
```


Объект массива, состоящий из одного или нескольких уравнений, выражений или других фрагментов математического текста, которые могут быть вертикально выровнены как единое целое относительно окружающего текста в строке.

### BAR {#BAR}
```
public static int BAR
```


Функция черты, состоящая из базового аргумента и надчерты или подчерты.

### BORDER_BOX {#BORDER-BOX}
```
public static int BORDER_BOX
```


Объект рамки (Border Box), состоящий из границы, нарисованной вокруг экземпляра математического текста (например, формулы или уравнения).

### BOX {#BOX}
```
public static int BOX
```


Объект коробки, используемый для группировки компонентов уравнения или другого экземпляра математического текста.

### DEGREE {#DEGREE}
```
public static int DEGREE
```


Степень в математическом радикале.

### DELIMITER {#DELIMITER}
```
public static int DELIMITER
```


Объект разделителя, состоящий из открывающих и закрывающих разделителей (например, скобок, фигурных скобок, квадратных скобок и вертикальных черт) и содержащегося внутри элемента.

### DENOMINATOR {#DENOMINATOR}
```
public static int DENOMINATOR
```


Знаменатель объекта дроби.

### FRACTION {#FRACTION}
```
public static int FRACTION
```


Объект дроби, состоящий из числителя и знаменателя, разделённых чертой дроби.

### FUNCTION {#FUNCTION}
```
public static int FUNCTION
```


Объект применения функции (Function-Apply), который состоит из имени функции и аргументного элемента, к которому применяется действие.

### FUNCTION_NAME {#FUNCTION-NAME}
```
public static int FUNCTION_NAME
```


Имя функции. Например, имена функций — sin и cos.

### GROUP_CHARACTER {#GROUP-CHARACTER}
```
public static int GROUP_CHARACTER
```


Объект группирующего символа (Group-Character), состоящий из символа, размещённого над или под текстом, часто с целью визуального объединения элементов.

### LIMIT {#LIMIT}
```
public static int LIMIT
```


Нижний предел объекта [LOWER\\_LIMIT](../../com.aspose.words/mathobjecttype/\\#LOWER-LIMIT) и верхний предел функции [UPPER\\_LIMIT](../../com.aspose.words/mathobjecttype/\\#UPPER-LIMIT).

### LOWER_LIMIT {#LOWER-LIMIT}
```
public static int LOWER_LIMIT
```


Объект нижнего предела (Lower-Limit), состоящий из текста на базовой линии и уменьшенного текста непосредственно под ним.

### MATRIX {#MATRIX}
```
public static int MATRIX
```


Объект матрицы, состоящий из одного или нескольких элементов, расположенных в одной или нескольких строках и одной или нескольких колонках.

### MATRIX_ROW {#MATRIX-ROW}
```
public static int MATRIX_ROW
```


Одна строка матрицы.

### NONE {#NONE}
```
public static int NONE
```


Тип объекта не указан.

### NUMERATOR {#NUMERATOR}
```
public static int NUMERATOR
```


Числитель объекта дроби.

### N_ARY {#N-ARY}
```
public static int N_ARY
```


Объект n-арный, состоящий из n-арного объекта, базы (или операнда) и необязательных верхних и нижних пределов.

### O_MATH {#O-MATH}
```
public static int O_MATH
```


Экземпляр математического текста.

### O_MATH_PARA {#O-MATH-PARA}
```
public static int O_MATH_PARA
```


Математический абзац или зона отображения математики, содержащая один или несколько элементов [O\\_MATH](../../com.aspose.words/mathobjecttype/\\#O-MATH) в режиме отображения.

### PHANTOM {#PHANTOM}
```
public static int PHANTOM
```


Фантомный объект.

### PRE_SUB_SUPERSCRIPT {#PRE-SUB-SUPERSCRIPT}
```
public static int PRE_SUB_SUPERSCRIPT
```


Объект предварительного под- и надстрочного (Pre-Sub-Superscript), который состоит из базового элемента и подстрочного и надстрочного индексов, размещённых слева от базы.

### RADICAL {#RADICAL}
```
public static int RADICAL
```


Радикальный объект, состоящий из радикала, базового элемента и необязательной степени.

### SUBSCRIPT {#SUBSCRIPT}
```
public static int SUBSCRIPT
```


Объект нижнего индекса, который состоит из базового элемента и уменьшенного скрипта, размещённого ниже и справа.

### SUBSCRIPT_PART {#SUBSCRIPT-PART}
```
public static int SUBSCRIPT_PART
```


Нижний индекс объекта, который может иметь часть в виде нижнего индекса.

### SUB_SUPERSCRIPT {#SUB-SUPERSCRIPT}
```
public static int SUB_SUPERSCRIPT
```


Объект под-надстрочного индекса, который состоит из базового элемента, уменьшенного скрипта, размещённого ниже и справа, и уменьшенного скрипта, размещённого выше и справа.

### SUPERSCRIPT {#SUPERSCRIPT}
```
public static int SUPERSCRIPT
```


Объект верхнего индекса, который состоит из базового элемента и уменьшенного скрипта, размещённого выше и справа.

### SUPERSCRIPT_PART {#SUPERSCRIPT-PART}
```
public static int SUPERSCRIPT_PART
```


Верхний индекс объекта верхнего индекса.

### UPPER_LIMIT {#UPPER-LIMIT}
```
public static int UPPER_LIMIT
```


Объект верхнего предела, состоящий из текста на базовой линии и уменьшенного текста непосредственно над ним.

### length {#length}
```
public static int length
```


### fromName(String mathObjectTypeName) {#fromName-java.lang.String}
```
public static int fromName(String mathObjectTypeName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| mathObjectTypeName | java.lang.String |  |

**Returns:**
int
### getName(int mathObjectType) {#getName-int}
```
public static String getName(int mathObjectType)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
| --- | --- | --- |
| mathObjectType | int |  |

**Returns:**
java.lang.String
