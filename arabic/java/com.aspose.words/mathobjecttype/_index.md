---
title: "MathObjectType"
linktitle: "MathObjectType"
second_title: "Aspose.Words لـ Java"
description: "يحدد نوع كائن Office Math في Java."
type: docs
weight: 459
url: /ar/java/com.aspose.words/mathobjecttype/
---

**Inheritance:**
java.lang.Object
```
public class MathObjectType
```

يحدد نوع كائن Office Math.

 **Examples:** 

يعرض كيفية طباعة بنية العقد لكل عقدة رياضية مكتبية في المستند.

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
## الحقول

| حقل | الوصف |
| --- | --- |
| [ACCENT](#ACCENT) | دالة التشكيل، تتكون من قاعدة وعلامة تشكيلية مركبة. |
| [ARGUMENT](#ARGUMENT) | كائن الحجة. |
| [ARRAY](#ARRAY) | كائن المصفوفة، يتكون من معادلة أو أكثر أو تعبيرات أو مقاطع نصية رياضية أخرى يمكن محاذاتها عموديًا كوحدة واحدة بالنسبة للنص المحيط على السطر. |
| [BAR](#BAR) | دالة الشريط، تتكون من حجة قاعدة وشريط فوقي أو سفلي. |
| [BORDER_BOX](#BORDER-BOX) | كائن صندوق الحدود، يتكون من حد يُرسم حول مثال للنص الرياضي (مثل صيغة أو معادلة). |
| [BOX](#BOX) | كائن الصندوق، يُستخدم لتجميع مكونات معادلة أو مثال آخر للنص الرياضي. |
| [DEGREE](#DEGREE) | درجة في الجذر الرياضي. |
| [DELIMITER](#DELIMITER) | كائن الفاصل، يتكون من فواصل افتتاحية وإغلاقية (مثل الأقواس المستديرة، الأقواس المعقوفة، الأقواس المربعة، والشرطات العمودية)، وعنصر موجود بداخلها. |
| [DENOMINATOR](#DENOMINATOR) | مقام كائن الكسر. |
| [FRACTION](#FRACTION) | كائن الكسر، يتكون من بسط ومقام مفصولين بشريط الكسر. |
| [FUNCTION](#FUNCTION) | كائن تطبيق الدالة، يتكون من اسم الدالة وعنصر حجة يُطبّق عليه. |
| [FUNCTION_NAME](#FUNCTION-NAME) | اسم الدالة. |
| [GROUP_CHARACTER](#GROUP-CHARACTER) | كائن تجميع-الحرف، يتكون من حرف يُرسم فوق أو تحت النص، غالبًا بهدف تجميع العناصر بصريًا. |
| [LIMIT](#LIMIT) | الحد الأدنى لكائن [LOWER\_LIMIT](../../com.aspose.words/mathobjecttype/\#LOWER-LIMIT) والحد الأعلى لدالة [UPPER\_LIMIT](../../com.aspose.words/mathobjecttype/\#UPPER-LIMIT). |
| [LOWER_LIMIT](#LOWER-LIMIT) | كائن الحد الأدنى، يتكون من نص على خط القاعدة ونص بحجم أصغر مباشرةً أسفله. |
| [MATRIX](#MATRIX) | كائن المصفوفة، يتكون من عنصر أو أكثر مُرتّب في صف واحد أو أكثر وعمود واحد أو أكثر. |
| [MATRIX_ROW](#MATRIX-ROW) | صف واحد من المصفوفة. |
| [NONE](#NONE) | نوع الكائن غير محدد. |
| [NUMERATOR](#NUMERATOR) | بسط كائن الكسر. |
| [N_ARY](#N-ARY) | كائن n-ary، يتكون من كائن n-ary، قاعدة (أو معامل)، وحدود علوية وسفلية اختيارية. |
| [O_MATH](#O-MATH) | مثال للنص الرياضي. |
| [O_MATH_PARA](#O-MATH-PARA) | فقرة رياضية، أو منطقة عرض رياضية، تحتوي على عنصر أو أكثر من [O\_MATH](../../com.aspose.words/mathobjecttype/\#O-MATH) في وضع العرض. |
| [PHANTOM](#PHANTOM) | كائن شبح. |
| [PRE_SUB_SUPERSCRIPT](#PRE-SUB-SUPERSCRIPT) | كائن ما قبل-تحتي-عليا، يتكون من عنصر قاعدة وتحتي وعليا موضوعة إلى يسار القاعدة. |
| [RADICAL](#RADICAL) | كائن جذري، يتكون من جذري وعنصر أساسي ودرجة اختيارية. |
| [SUBSCRIPT](#SUBSCRIPT) | كائن نص سفلي، يتكون من عنصر أساسي ونص بحجم مصغر موضع أسفل اليمين. |
| [SUBSCRIPT_PART](#SUBSCRIPT-PART) | نص سفلي للكائن يمكن أن يحتوي على جزء سفلي. |
| [SUB_SUPERSCRIPT](#SUB-SUPERSCRIPT) | كائن نص سفلي-علوي، يتكون من عنصر أساسي ونص بحجم مصغر موضع أسفل اليمين، ونص بحجم مصغر موضع أعلى اليمين. |
| [SUPERSCRIPT](#SUPERSCRIPT) | كائن نص علوي، يتكون من عنصر أساسي ونص بحجم مصغر موضع أعلى اليمين. |
| [SUPERSCRIPT_PART](#SUPERSCRIPT-PART) | نص علوي لكائن النص العلوي. |
| [UPPER_LIMIT](#UPPER-LIMIT) | كائن حد أعلى، يتكون من نص على الخط الأساسي ونص بحجم مصغر مباشرةً فوقه. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String mathObjectTypeName)](#fromName-java.lang.String) |  |
| [getName(int mathObjectType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int mathObjectType)](#toString-int) |  |
### ACCENT {#ACCENT}
```
public static int ACCENT
```


دالة التشكيل، تتكون من قاعدة وعلامة تشكيلية مركبة.

### ARGUMENT {#ARGUMENT}
```
public static int ARGUMENT
```


كائن حجة. يحيط بكيانات Office Math عندما تُستخدم كحجج لكيانات Office Math أخرى.

### ARRAY {#ARRAY}
```
public static int ARRAY
```


كائن المصفوفة، يتكون من معادلة أو أكثر أو تعبيرات أو مقاطع نصية رياضية أخرى يمكن محاذاتها عموديًا كوحدة واحدة بالنسبة للنص المحيط على السطر.

### BAR {#BAR}
```
public static int BAR
```


دالة الشريط، تتكون من حجة قاعدة وشريط فوقي أو سفلي.

### BORDER_BOX {#BORDER-BOX}
```
public static int BORDER_BOX
```


كائن صندوق الحدود، يتكون من حد يُرسم حول مثال للنص الرياضي (مثل صيغة أو معادلة).

### BOX {#BOX}
```
public static int BOX
```


كائن الصندوق، يُستخدم لتجميع مكونات معادلة أو مثال آخر للنص الرياضي.

### DEGREE {#DEGREE}
```
public static int DEGREE
```


درجة في الجذر الرياضي.

### DELIMITER {#DELIMITER}
```
public static int DELIMITER
```


كائن الفاصل، يتكون من فواصل افتتاحية وإغلاقية (مثل الأقواس المستديرة، الأقواس المعقوفة، الأقواس المربعة، والشرطات العمودية)، وعنصر موجود بداخلها.

### DENOMINATOR {#DENOMINATOR}
```
public static int DENOMINATOR
```


مقام كائن الكسر.

### FRACTION {#FRACTION}
```
public static int FRACTION
```


كائن الكسر، يتكون من بسط ومقام مفصولين بشريط الكسر.

### FUNCTION {#FUNCTION}
```
public static int FUNCTION
```


كائن تطبيق الدالة، يتكون من اسم الدالة وعنصر حجة يُطبّق عليه.

### FUNCTION_NAME {#FUNCTION-NAME}
```
public static int FUNCTION_NAME
```


اسم الدالة. على سبيل المثال، أسماء الدوال هي sin و cos.

### GROUP_CHARACTER {#GROUP-CHARACTER}
```
public static int GROUP_CHARACTER
```


كائن تجميع-الحرف، يتكون من حرف يُرسم فوق أو تحت النص، غالبًا بهدف تجميع العناصر بصريًا.

### LIMIT {#LIMIT}
```
public static int LIMIT
```


الحد الأدنى لكائن [LOWER\_LIMIT](../../com.aspose.words/mathobjecttype/\#LOWER-LIMIT) والحد الأعلى لدالة [UPPER\_LIMIT](../../com.aspose.words/mathobjecttype/\#UPPER-LIMIT).

### LOWER_LIMIT {#LOWER-LIMIT}
```
public static int LOWER_LIMIT
```


كائن الحد الأدنى، يتكون من نص على خط القاعدة ونص بحجم أصغر مباشرةً أسفله.

### MATRIX {#MATRIX}
```
public static int MATRIX
```


كائن المصفوفة، يتكون من عنصر أو أكثر مُرتّب في صف واحد أو أكثر وعمود واحد أو أكثر.

### MATRIX_ROW {#MATRIX-ROW}
```
public static int MATRIX_ROW
```


صف واحد من المصفوفة.

### NONE {#NONE}
```
public static int NONE
```


نوع الكائن غير محدد.

### NUMERATOR {#NUMERATOR}
```
public static int NUMERATOR
```


بسط كائن الكسر.

### N_ARY {#N-ARY}
```
public static int N_ARY
```


كائن n-ary، يتكون من كائن n-ary، قاعدة (أو معامل)، وحدود علوية وسفلية اختيارية.

### O_MATH {#O-MATH}
```
public static int O_MATH
```


مثال للنص الرياضي.

### O_MATH_PARA {#O-MATH-PARA}
```
public static int O_MATH_PARA
```


فقرة رياضية، أو منطقة عرض رياضية، تحتوي على عنصر أو أكثر من [O\_MATH](../../com.aspose.words/mathobjecttype/\#O-MATH) في وضع العرض.

### PHANTOM {#PHANTOM}
```
public static int PHANTOM
```


كائن شبح.

### PRE_SUB_SUPERSCRIPT {#PRE-SUB-SUPERSCRIPT}
```
public static int PRE_SUB_SUPERSCRIPT
```


كائن ما قبل-تحتي-عليا، يتكون من عنصر قاعدة وتحتي وعليا موضوعة إلى يسار القاعدة.

### RADICAL {#RADICAL}
```
public static int RADICAL
```


كائن جذري، يتكون من جذري وعنصر أساسي ودرجة اختيارية.

### SUBSCRIPT {#SUBSCRIPT}
```
public static int SUBSCRIPT
```


كائن نص سفلي، يتكون من عنصر أساسي ونص بحجم مصغر موضع أسفل اليمين.

### SUBSCRIPT_PART {#SUBSCRIPT-PART}
```
public static int SUBSCRIPT_PART
```


نص سفلي للكائن يمكن أن يحتوي على جزء سفلي.

### SUB_SUPERSCRIPT {#SUB-SUPERSCRIPT}
```
public static int SUB_SUPERSCRIPT
```


كائن نص سفلي-علوي، يتكون من عنصر أساسي ونص بحجم مصغر موضع أسفل اليمين، ونص بحجم مصغر موضع أعلى اليمين.

### SUPERSCRIPT {#SUPERSCRIPT}
```
public static int SUPERSCRIPT
```


كائن نص علوي، يتكون من عنصر أساسي ونص بحجم مصغر موضع أعلى اليمين.

### SUPERSCRIPT_PART {#SUPERSCRIPT-PART}
```
public static int SUPERSCRIPT_PART
```


نص علوي لكائن النص العلوي.

### UPPER_LIMIT {#UPPER-LIMIT}
```
public static int UPPER_LIMIT
```


كائن حد أعلى، يتكون من نص على الخط الأساسي ونص بحجم مصغر مباشرةً فوقه.

### length {#length}
```
public static int length
```


### fromName(String mathObjectTypeName) {#fromName-java.lang.String}
```
public static int fromName(String mathObjectTypeName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| mathObjectTypeName | java.lang.String |  |

**Returns:**
int
### getName(int mathObjectType) {#getName-int}
```
public static String getName(int mathObjectType)
```




**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| mathObjectType | int |  |

**Returns:**
java.lang.String
