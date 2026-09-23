---
title: "MathObjectType"
linktitle: "MathObjectType"
second_title: "Aspose.Words per Java"
description: "Specifica il tipo di un oggetto Office Math in Java."
type: docs
weight: 459
url: /it/java/com.aspose.words/mathobjecttype/
---

**Inheritance:**
java.lang.Object
```
public class MathObjectType
```

Specifica il tipo di un oggetto Office Math.

 **Examples:** 

Mostra come stampare la struttura dei nodi di ogni nodo Office Math in un documento.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [ACCENT](#ACCENT) | Funzione accento, composta da una base e un segno diacritico combinante. |
| [ARGUMENT](#ARGUMENT) | Oggetto argomento. |
| [ARRAY](#ARRAY) | Oggetto array, composto da una o più equazioni, espressioni o altri segmenti di testo matematico che possono essere giustificati verticalmente come un'unità rispetto al testo circostante sulla linea. |
| [BAR](#BAR) | Funzione barra, composta da un argomento base e una barra superiore o inferiore. |
| [BORDER_BOX](#BORDER-BOX) | Oggetto Border Box, composto da un bordo disegnato attorno a un'istanza di testo matematico (come una formula o un'equazione). |
| [BOX](#BOX) | Oggetto Box, utilizzato per raggruppare componenti di un'equazione o altra istanza di testo matematico. |
| [DEGREE](#DEGREE) | Grado nel radicale matematico. |
| [DELIMITER](#DELIMITER) | Oggetto delimitatore, composto da delimitatori di apertura e chiusura (come parentesi tonde, graffe, quadre e barre verticali) e da un elemento contenuto al loro interno. |
| [DENOMINATOR](#DENOMINATOR) | Denominatore di un oggetto frazione. |
| [FRACTION](#FRACTION) | Oggetto frazione, composto da un numeratore e un denominatore separati da una barra di frazione. |
| [FUNCTION](#FUNCTION) | Oggetto Function-Apply, che consiste in un nome di funzione e un elemento argomento su cui agire. |
| [FUNCTION_NAME](#FUNCTION-NAME) | Nome della funzione. |
| [GROUP_CHARACTER](#GROUP-CHARACTER) | Oggetto Group-Character, composto da un carattere disegnato sopra o sotto il testo, spesso con lo scopo di raggruppare visivamente gli elementi. |
| [LIMIT](#LIMIT) | Limite inferiore dell'oggetto [LOWER\_LIMIT](../../com.aspose.words/mathobjecttype/\#LOWER-LIMIT) e limite superiore della funzione [UPPER\_LIMIT](../../com.aspose.words/mathobjecttype/\#UPPER-LIMIT). |
| [LOWER_LIMIT](#LOWER-LIMIT) | Oggetto Lower-Limit, composto da testo sulla linea di base e testo di dimensione ridotta immediatamente al di sotto. |
| [MATRIX](#MATRIX) | Oggetto matrice, composto da uno o più elementi disposti in una o più righe e una o più colonne. |
| [MATRIX_ROW](#MATRIX-ROW) | Riga singola della matrice. |
| [NONE](#NONE) | Il tipo di oggetto non è specificato. |
| [NUMERATOR](#NUMERATOR) | Numeratore dell'oggetto Frazione. |
| [N_ARY](#N-ARY) | Oggetto N-ario, composto da un oggetto n-ario, una base (o operando) e limiti superiori e inferiori opzionali. |
| [O_MATH](#O-MATH) | Istanza di testo matematico. |
| [O_MATH_PARA](#O-MATH-PARA) | Paragrafo matematico, o zona di visualizzazione matematica, che contiene uno o più elementi [O\_MATH](../../com.aspose.words/mathobjecttype/\#O-MATH) in modalità display. |
| [PHANTOM](#PHANTOM) | Oggetto fantasma. |
| [PRE_SUB_SUPERSCRIPT](#PRE-SUB-SUPERSCRIPT) | Oggetto Pre-Sub-Superscript, che consiste in un elemento base e un pedice e apice posizionati a sinistra della base. |
| [RADICAL](#RADICAL) | Oggetto radicale, composto da un radicale, un elemento base e un grado opzionale. |
| [SUBSCRIPT](#SUBSCRIPT) | Oggetto pedice, che consiste in un elemento base e uno script di dimensioni ridotte posizionato sotto e a destra. |
| [SUBSCRIPT_PART](#SUBSCRIPT-PART) | Pedice dell'oggetto che può avere una parte pedice. |
| [SUB_SUPERSCRIPT](#SUB-SUPERSCRIPT) | Oggetto sub-superscript, che consiste in un elemento base, uno script di dimensioni ridotte posizionato sotto e a destra, e uno script di dimensioni ridotte posizionato sopra e a destra. |
| [SUPERSCRIPT](#SUPERSCRIPT) | Oggetto apice, che consiste in un elemento base e uno script di dimensioni ridotte posizionato sopra e a destra. |
| [SUPERSCRIPT_PART](#SUPERSCRIPT-PART) | Apice dell'oggetto apice. |
| [UPPER_LIMIT](#UPPER-LIMIT) | Oggetto limite superiore, composto da testo sulla linea di base e testo di dimensioni ridotte immediatamente sopra di esso. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String mathObjectTypeName)](#fromName-java.lang.String) |  |
| [getName(int mathObjectType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int mathObjectType)](#toString-int) |  |
### ACCENT {#ACCENT}
```
public static int ACCENT
```


Funzione accento, composta da una base e un segno diacritico combinante.

### ARGUMENT {#ARGUMENT}
```
public static int ARGUMENT
```


Oggetto argomento. Racchiude le entità Office Math quando vengono utilizzate come argomenti per altre entità Office Math.

### ARRAY {#ARRAY}
```
public static int ARRAY
```


Oggetto array, composto da una o più equazioni, espressioni o altri segmenti di testo matematico che possono essere giustificati verticalmente come un'unità rispetto al testo circostante sulla linea.

### BAR {#BAR}
```
public static int BAR
```


Funzione barra, composta da un argomento base e una barra superiore o inferiore.

### BORDER_BOX {#BORDER-BOX}
```
public static int BORDER_BOX
```


Oggetto Border Box, composto da un bordo disegnato attorno a un'istanza di testo matematico (come una formula o un'equazione).

### BOX {#BOX}
```
public static int BOX
```


Oggetto Box, utilizzato per raggruppare componenti di un'equazione o altra istanza di testo matematico.

### DEGREE {#DEGREE}
```
public static int DEGREE
```


Grado nel radicale matematico.

### DELIMITER {#DELIMITER}
```
public static int DELIMITER
```


Oggetto delimitatore, composto da delimitatori di apertura e chiusura (come parentesi tonde, graffe, quadre e barre verticali) e da un elemento contenuto al loro interno.

### DENOMINATOR {#DENOMINATOR}
```
public static int DENOMINATOR
```


Denominatore di un oggetto frazione.

### FRACTION {#FRACTION}
```
public static int FRACTION
```


Oggetto frazione, composto da un numeratore e un denominatore separati da una barra di frazione.

### FUNCTION {#FUNCTION}
```
public static int FUNCTION
```


Oggetto Function-Apply, che consiste in un nome di funzione e un elemento argomento su cui agire.

### FUNCTION_NAME {#FUNCTION-NAME}
```
public static int FUNCTION_NAME
```


Nome della funzione. Per esempio, i nomi delle funzioni sono sin e cos.

### GROUP_CHARACTER {#GROUP-CHARACTER}
```
public static int GROUP_CHARACTER
```


Oggetto Group-Character, composto da un carattere disegnato sopra o sotto il testo, spesso con lo scopo di raggruppare visivamente gli elementi.

### LIMIT {#LIMIT}
```
public static int LIMIT
```


Limite inferiore dell'oggetto [LOWER\_LIMIT](../../com.aspose.words/mathobjecttype/\#LOWER-LIMIT) e limite superiore della funzione [UPPER\_LIMIT](../../com.aspose.words/mathobjecttype/\#UPPER-LIMIT).

### LOWER_LIMIT {#LOWER-LIMIT}
```
public static int LOWER_LIMIT
```


Oggetto Lower-Limit, composto da testo sulla linea di base e testo di dimensione ridotta immediatamente al di sotto.

### MATRIX {#MATRIX}
```
public static int MATRIX
```


Oggetto matrice, composto da uno o più elementi disposti in una o più righe e una o più colonne.

### MATRIX_ROW {#MATRIX-ROW}
```
public static int MATRIX_ROW
```


Riga singola della matrice.

### NONE {#NONE}
```
public static int NONE
```


Il tipo di oggetto non è specificato.

### NUMERATOR {#NUMERATOR}
```
public static int NUMERATOR
```


Numeratore dell'oggetto Frazione.

### N_ARY {#N-ARY}
```
public static int N_ARY
```


Oggetto N-ario, composto da un oggetto n-ario, una base (o operando) e limiti superiori e inferiori opzionali.

### O_MATH {#O-MATH}
```
public static int O_MATH
```


Istanza di testo matematico.

### O_MATH_PARA {#O-MATH-PARA}
```
public static int O_MATH_PARA
```


Paragrafo matematico, o zona di visualizzazione matematica, che contiene uno o più elementi [O\_MATH](../../com.aspose.words/mathobjecttype/\#O-MATH) in modalità display.

### PHANTOM {#PHANTOM}
```
public static int PHANTOM
```


Oggetto fantasma.

### PRE_SUB_SUPERSCRIPT {#PRE-SUB-SUPERSCRIPT}
```
public static int PRE_SUB_SUPERSCRIPT
```


Oggetto Pre-Sub-Superscript, che consiste in un elemento base e un pedice e apice posizionati a sinistra della base.

### RADICAL {#RADICAL}
```
public static int RADICAL
```


Oggetto radicale, composto da un radicale, un elemento base e un grado opzionale.

### SUBSCRIPT {#SUBSCRIPT}
```
public static int SUBSCRIPT
```


Oggetto pedice, che consiste in un elemento base e uno script di dimensioni ridotte posizionato sotto e a destra.

### SUBSCRIPT_PART {#SUBSCRIPT-PART}
```
public static int SUBSCRIPT_PART
```


Pedice dell'oggetto che può avere una parte pedice.

### SUB_SUPERSCRIPT {#SUB-SUPERSCRIPT}
```
public static int SUB_SUPERSCRIPT
```


Oggetto sub-superscript, che consiste in un elemento base, uno script di dimensioni ridotte posizionato sotto e a destra, e uno script di dimensioni ridotte posizionato sopra e a destra.

### SUPERSCRIPT {#SUPERSCRIPT}
```
public static int SUPERSCRIPT
```


Oggetto apice, che consiste in un elemento base e uno script di dimensioni ridotte posizionato sopra e a destra.

### SUPERSCRIPT_PART {#SUPERSCRIPT-PART}
```
public static int SUPERSCRIPT_PART
```


Apice dell'oggetto apice.

### UPPER_LIMIT {#UPPER-LIMIT}
```
public static int UPPER_LIMIT
```


Oggetto limite superiore, composto da testo sulla linea di base e testo di dimensioni ridotte immediatamente sopra di esso.

### length {#length}
```
public static int length
```


### fromName(String mathObjectTypeName) {#fromName-java.lang.String}
```
public static int fromName(String mathObjectTypeName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| mathObjectTypeName | java.lang.String |  |

**Returns:**
int
### getName(int mathObjectType) {#getName-int}
```
public static String getName(int mathObjectType)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| mathObjectType | int |  |

**Returns:**
java.lang.String
