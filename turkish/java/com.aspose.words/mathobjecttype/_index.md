---
title: "MathObjectType"
linktitle: "MathObjectType"
second_title: "Aspose.Words Java için"
description: "Java'da bir Office Math nesnesinin türünü belirtir."
type: docs
weight: 459
url: /tr/java/com.aspose.words/mathobjecttype/
---

**Inheritance:**
java.lang.Object
```
public class MathObjectType
```

Bir Office Math nesnesinin tipini belirtir.

 **Examples:** 

Bir belgede her Office Math düğümünün düğüm yapısının nasıl yazdırılacağını gösterir.

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
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [ACCENT](#ACCENT) | Aksan işlevi, bir temel ve birleştirici diakritik işaretten oluşur. |
| [ARGUMENT](#ARGUMENT) | Argüman nesnesi. |
| [ARRAY](#ARRAY) | Dizi nesnesi, bir veya daha fazla denklem, ifade veya diğer matematiksel metin akışlarından oluşur ve satırdaki çevre metne göre bir birim olarak dikey olarak hizalanabilir. |
| [BAR](#BAR) | Bar işlevi, bir temel argüman ve üst çubuk ya da alt çubuktan oluşur. |
| [BORDER_BOX](#BORDER-BOX) | Border Box nesnesi, bir formül veya denklem gibi bir matematiksel metin örneği etrafına çizilen bir kenarlık içerir |
| [BOX](#BOX) | Box nesnesi, bir denklemin veya diğer bir matematiksel metin örneğinin bileşenlerini gruplamak için kullanılır. |
| [DEGREE](#DEGREE) | Matematiksel kökteki derece. |
| [DELIMITER](#DELIMITER) | Delimiter nesnesi, açılış ve kapanış sınırlayıcılarından (parantez, süslü parantez, köşeli parantez ve dikey çubuk gibi) ve içinde bulunan bir öğeden oluşur. |
| [DENOMINATOR](#DENOMINATOR) | Bir kesir nesnesinin paydası. |
| [FRACTION](#FRACTION) | Fraction nesnesi, bir pay ve bir paydadan oluşur ve bir kesir çubuğu ile ayrılır. |
| [FUNCTION](#FUNCTION) | Function-Apply nesnesi, bir fonksiyon adı ve üzerine uygulanacak bir argüman öğesinden oluşur. |
| [FUNCTION_NAME](#FUNCTION-NAME) | Fonksiyonun adı. |
| [GROUP_CHARACTER](#GROUP-CHARACTER) | Group-Character nesnesi, metnin üzerine veya altına çizilen bir karakterden oluşur ve genellikle öğeleri görsel olarak gruplama amacı taşır |
| [LIMIT](#LIMIT) | Alt sınır, [LOWER\_LIMIT](../../com.aspose.words/mathobjecttype/\#LOWER-LIMIT) nesnesinin ve üst sınır, [UPPER\_LIMIT](../../com.aspose.words/mathobjecttype/\#UPPER-LIMIT) işlevinin. |
| [LOWER_LIMIT](#LOWER-LIMIT) | Lower-Limit nesnesi, temel çizgi üzerindeki metin ve hemen altında daha küçük boyutta metinden oluşur. |
| [MATRIX](#MATRIX) | Matrix nesnesi, bir veya daha fazla satır ve bir veya daha fazla sütunda düzenlenmiş bir veya daha fazla öğeden oluşur. |
| [MATRIX_ROW](#MATRIX-ROW) | Matrisin tek satırı. |
| [NONE](#NONE) | Nesnenin türü belirtilmemiştir. |
| [NUMERATOR](#NUMERATOR) | Fraction nesnesinin payı. |
| [N_ARY](#N-ARY) | N-ary nesnesi, bir n-ary nesnesi, bir temel (veya operand) ve isteğe bağlı üst ve alt sınırları içerir. |
| [O_MATH](#O-MATH) | Matematiksel metin örneği. |
| [O_MATH_PARA](#O-MATH-PARA) | Görüntüleme modunda olan bir veya daha fazla [O\_MATH](../../com.aspose.words/mathobjecttype/\#O-MATH) öğesi içeren matematik paragrafı veya görüntüleme matematik bölgesi. |
| [PHANTOM](#PHANTOM) | Phantom nesnesi. |
| [PRE_SUB_SUPERSCRIPT](#PRE-SUB-SUPERSCRIPT) | Pre-Sub-Superscript nesnesi, bir temel öğe ve temel öğenin soluna yerleştirilen alt ve üst simge öğelerinden oluşur. |
| [RADICAL](#RADICAL) | Kök nesnesi, bir kök, bir temel öğe ve isteğe bağlı bir derece içerir. |
| [SUBSCRIPT](#SUBSCRIPT) | Alt simge nesnesi, bir temel öğe ve aşağıya ve sağa yerleştirilmiş küçültülmüş boyutlu bir alt simge içerir. |
| [SUBSCRIPT_PART](#SUBSCRIPT-PART) | Alt simge, alt simge kısmına sahip olabilen nesnedir. |
| [SUB_SUPERSCRIPT](#SUB-SUPERSCRIPT) | Alt-üst simge nesnesi, bir temel öğe, aşağıya ve sağa yerleştirilmiş küçültülmüş bir alt simge ve yukarıya ve sağa yerleştirilmiş küçültülmüş bir üst simge içerir. |
| [SUPERSCRIPT](#SUPERSCRIPT) | Üst simge nesnesi, bir temel öğe ve yukarıya ve sağa yerleştirilmiş küçültülmüş bir üst simge içerir. |
| [SUPERSCRIPT_PART](#SUPERSCRIPT-PART) | Üst simge nesnesinin üst simgesi. |
| [UPPER_LIMIT](#UPPER-LIMIT) | Üst Sınır nesnesi, temel çizgi üzerindeki metin ve hemen üstünde bulunan küçültülmüş metin içerir. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String mathObjectTypeName)](#fromName-java.lang.String) |  |
| [getName(int mathObjectType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int mathObjectType)](#toString-int) |  |
### ACCENT {#ACCENT}
```
public static int ACCENT
```


Aksan işlevi, bir temel ve birleştirici diakritik işaretten oluşur.

### ARGUMENT {#ARGUMENT}
```
public static int ARGUMENT
```


Argüman nesnesi. Office Math varlıklarını, diğer Office Math varlıklarına argüman olarak kullanıldıklarında kapsar.

### ARRAY {#ARRAY}
```
public static int ARRAY
```


Dizi nesnesi, bir veya daha fazla denklem, ifade veya diğer matematiksel metin akışlarından oluşur ve satırdaki çevre metne göre bir birim olarak dikey olarak hizalanabilir.

### BAR {#BAR}
```
public static int BAR
```


Bar işlevi, bir temel argüman ve üst çubuk ya da alt çubuktan oluşur.

### BORDER_BOX {#BORDER-BOX}
```
public static int BORDER_BOX
```


Border Box nesnesi, bir formül veya denklem gibi bir matematiksel metin örneği etrafına çizilen bir kenarlık içerir

### BOX {#BOX}
```
public static int BOX
```


Box nesnesi, bir denklemin veya diğer bir matematiksel metin örneğinin bileşenlerini gruplamak için kullanılır.

### DEGREE {#DEGREE}
```
public static int DEGREE
```


Matematiksel kökteki derece.

### DELIMITER {#DELIMITER}
```
public static int DELIMITER
```


Delimiter nesnesi, açılış ve kapanış sınırlayıcılarından (parantez, süslü parantez, köşeli parantez ve dikey çubuk gibi) ve içinde bulunan bir öğeden oluşur.

### DENOMINATOR {#DENOMINATOR}
```
public static int DENOMINATOR
```


Bir kesir nesnesinin paydası.

### FRACTION {#FRACTION}
```
public static int FRACTION
```


Fraction nesnesi, bir pay ve bir paydadan oluşur ve bir kesir çubuğu ile ayrılır.

### FUNCTION {#FUNCTION}
```
public static int FUNCTION
```


Function-Apply nesnesi, bir fonksiyon adı ve üzerine uygulanacak bir argüman öğesinden oluşur.

### FUNCTION_NAME {#FUNCTION-NAME}
```
public static int FUNCTION_NAME
```


Fonksiyonun adı. Örneğin, fonksiyon adları sin ve cos'tur.

### GROUP_CHARACTER {#GROUP-CHARACTER}
```
public static int GROUP_CHARACTER
```


Group-Character nesnesi, metnin üzerine veya altına çizilen bir karakterden oluşur ve genellikle öğeleri görsel olarak gruplama amacı taşır

### LIMIT {#LIMIT}
```
public static int LIMIT
```


Alt sınır, [LOWER\_LIMIT](../../com.aspose.words/mathobjecttype/\#LOWER-LIMIT) nesnesinin ve üst sınır, [UPPER\_LIMIT](../../com.aspose.words/mathobjecttype/\#UPPER-LIMIT) işlevinin.

### LOWER_LIMIT {#LOWER-LIMIT}
```
public static int LOWER_LIMIT
```


Lower-Limit nesnesi, temel çizgi üzerindeki metin ve hemen altında daha küçük boyutta metinden oluşur.

### MATRIX {#MATRIX}
```
public static int MATRIX
```


Matrix nesnesi, bir veya daha fazla satır ve bir veya daha fazla sütunda düzenlenmiş bir veya daha fazla öğeden oluşur.

### MATRIX_ROW {#MATRIX-ROW}
```
public static int MATRIX_ROW
```


Matrisin tek satırı.

### NONE {#NONE}
```
public static int NONE
```


Nesnenin türü belirtilmemiştir.

### NUMERATOR {#NUMERATOR}
```
public static int NUMERATOR
```


Fraction nesnesinin payı.

### N_ARY {#N-ARY}
```
public static int N_ARY
```


N-ary nesnesi, bir n-ary nesnesi, bir temel (veya operand) ve isteğe bağlı üst ve alt sınırları içerir.

### O_MATH {#O-MATH}
```
public static int O_MATH
```


Matematiksel metin örneği.

### O_MATH_PARA {#O-MATH-PARA}
```
public static int O_MATH_PARA
```


Görüntüleme modunda olan bir veya daha fazla [O\_MATH](../../com.aspose.words/mathobjecttype/\#O-MATH) öğesi içeren matematik paragrafı veya görüntüleme matematik bölgesi.

### PHANTOM {#PHANTOM}
```
public static int PHANTOM
```


Phantom nesnesi.

### PRE_SUB_SUPERSCRIPT {#PRE-SUB-SUPERSCRIPT}
```
public static int PRE_SUB_SUPERSCRIPT
```


Pre-Sub-Superscript nesnesi, bir temel öğe ve temel öğenin soluna yerleştirilen alt ve üst simge öğelerinden oluşur.

### RADICAL {#RADICAL}
```
public static int RADICAL
```


Kök nesnesi, bir kök, bir temel öğe ve isteğe bağlı bir derece içerir.

### SUBSCRIPT {#SUBSCRIPT}
```
public static int SUBSCRIPT
```


Alt simge nesnesi, bir temel öğe ve aşağıya ve sağa yerleştirilmiş küçültülmüş boyutlu bir alt simge içerir.

### SUBSCRIPT_PART {#SUBSCRIPT-PART}
```
public static int SUBSCRIPT_PART
```


Alt simge, alt simge kısmına sahip olabilen nesnedir.

### SUB_SUPERSCRIPT {#SUB-SUPERSCRIPT}
```
public static int SUB_SUPERSCRIPT
```


Alt-üst simge nesnesi, bir temel öğe, aşağıya ve sağa yerleştirilmiş küçültülmüş bir alt simge ve yukarıya ve sağa yerleştirilmiş küçültülmüş bir üst simge içerir.

### SUPERSCRIPT {#SUPERSCRIPT}
```
public static int SUPERSCRIPT
```


Üst simge nesnesi, bir temel öğe ve yukarıya ve sağa yerleştirilmiş küçültülmüş bir üst simge içerir.

### SUPERSCRIPT_PART {#SUPERSCRIPT-PART}
```
public static int SUPERSCRIPT_PART
```


Üst simge nesnesinin üst simgesi.

### UPPER_LIMIT {#UPPER-LIMIT}
```
public static int UPPER_LIMIT
```


Üst Sınır nesnesi, temel çizgi üzerindeki metin ve hemen üstünde bulunan küçültülmüş metin içerir.

### length {#length}
```
public static int length
```


### fromName(String mathObjectTypeName) {#fromName-java.lang.String}
```
public static int fromName(String mathObjectTypeName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| mathObjectTypeName | java.lang.String |  |

**Returns:**
int
### getName(int mathObjectType) {#getName-int}
```
public static String getName(int mathObjectType)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| mathObjectType | int |  |

**Returns:**
java.lang.String
