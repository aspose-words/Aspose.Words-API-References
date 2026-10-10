---
title: "TypeObjetMath"
linktitle: "TypeObjetMath"
second_title: "Aspose.Words pour Java"
description: "Spécifie le type d'un objet Office Math en Java."
type: docs
weight: 459
url: /fr/java/com.aspose.words/mathobjecttype/
---

**Inheritance:**
java.lang.Object
```
public class MathObjectType
```

Spécifie le type d'un objet Office Math.

 **Examples:** 

Montre comment imprimer la structure des nœuds de chaque formule Office Math dans un document.

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
## Champs

| Champ | Description |
| --- | --- |
| [ACCENT](#ACCENT) | Fonction d'accent, composée d'une base et d'un signe diacritique combiné. |
| [ARGUMENT](#ARGUMENT) | Objet argument. |
| [ARRAY](#ARRAY) | Objet tableau, composé d'une ou plusieurs équations, expressions ou autres séquences de texte mathématique pouvant être justifiées verticalement en tant qu'unité par rapport au texte environnant sur la ligne. |
| [BAR](#BAR) | Fonction barre, composée d'un argument de base et d'une barre supérieure ou inférieure. |
| [BORDER_BOX](#BORDER-BOX) | Objet Boîte à bordure, composé d'une bordure dessinée autour d'une instance de texte mathématique (comme une formule ou une équation) |
| [BOX](#BOX) | Objet boîte, utilisé pour regrouper les composants d'une équation ou d'une autre instance de texte mathématique. |
| [DEGREE](#DEGREE) | Degré dans la racine mathématique. |
| [DELIMITER](#DELIMITER) | Objet délimiteur, composé de délimiteurs d'ouverture et de fermeture (tels que parenthèses, accolades, crochets et barres verticales), et d'un élément contenu à l'intérieur. |
| [DENOMINATOR](#DENOMINATOR) | Dénominateur d'un objet fraction. |
| [FRACTION](#FRACTION) | Objet fraction, composé d'un numérateur et d'un dénominateur séparés par une barre de fraction. |
| [FUNCTION](#FUNCTION) | Objet Fonction-Appliquer, qui consiste en un nom de fonction et un élément argument sur lequel il agit. |
| [FUNCTION_NAME](#FUNCTION-NAME) | Nom de la fonction. |
| [GROUP_CHARACTER](#GROUP-CHARACTER) | Objet Groupe-Caractère, composé d'un caractère dessiné au-dessus ou au-dessous du texte, souvent dans le but de regrouper visuellement les éléments. |
| [LIMIT](#LIMIT) | Limite inférieure de l'objet [LOWER\_LIMIT](../../com.aspose.words/mathobjecttype/\#LOWER-LIMIT) et limite supérieure de la fonction [UPPER\_LIMIT](../../com.aspose.words/mathobjecttype/\#UPPER-LIMIT). |
| [LOWER_LIMIT](#LOWER-LIMIT) | Objet Limite-inférieure, composé de texte sur la ligne de base et de texte de taille réduite immédiatement en dessous. |
| [MATRIX](#MATRIX) | Objet matrice, composé d'un ou plusieurs éléments disposés en une ou plusieurs lignes et une ou plusieurs colonnes. |
| [MATRIX_ROW](#MATRIX-ROW) | Ligne unique de la matrice. |
| [NONE](#NONE) | Le type d'objet n'est pas spécifié. |
| [NUMERATOR](#NUMERATOR) | Numérateur de l'objet Fraction. |
| [N_ARY](#N-ARY) | Objet n-aire, composé d'un objet n-aire, d'une base (ou opérande), et de limites supérieures et inférieures optionnelles. |
| [O_MATH](#O-MATH) | Instance de texte mathématique. |
| [O_MATH_PARA](#O-MATH-PARA) | Paragraphe mathématique, ou zone d'affichage mathématique, contenant un ou plusieurs éléments [O\_MATH](../../com.aspose.words/mathobjecttype/\#O-MATH) en mode affichage. |
| [PHANTOM](#PHANTOM) | Objet fantôme. |
| [PRE_SUB_SUPERSCRIPT](#PRE-SUB-SUPERSCRIPT) | Objet Pré-Sub-Surscript, qui consiste en un élément de base et un indice et un exposant placés à gauche de la base. |
| [RADICAL](#RADICAL) | Objet radical, composé d'un radical, d'un élément de base et d'un degré optionnel. |
| [SUBSCRIPT](#SUBSCRIPT) | Objet indice, qui se compose d'un élément de base et d'un script de taille réduite placé en dessous et à droite. |
| [SUBSCRIPT_PART](#SUBSCRIPT-PART) | Indice de l'objet qui peut avoir une partie indice. |
| [SUB_SUPERSCRIPT](#SUB-SUPERSCRIPT) | Objet sous-surscript, qui se compose d'un élément de base, d'un script de taille réduite placé en dessous et à droite, et d'un script de taille réduite placé au-dessus et à droite. |
| [SUPERSCRIPT](#SUPERSCRIPT) | Objet exposant, qui se compose d'un élément de base et d'un script de taille réduite placé au-dessus et à droite. |
| [SUPERSCRIPT_PART](#SUPERSCRIPT-PART) | Exposant de l'objet exposant. |
| [UPPER_LIMIT](#UPPER-LIMIT) | Objet limite supérieure, composé de texte sur la ligne de base et de texte de taille réduite immédiatement au-dessus. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String mathObjectTypeName)](#fromName-java.lang.String) |  |
| [getName(int mathObjectType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int mathObjectType)](#toString-int) |  |
### ACCENT {#ACCENT}
```
public static int ACCENT
```


Fonction d'accent, composée d'une base et d'un signe diacritique combiné.

### ARGUMENT {#ARGUMENT}
```
public static int ARGUMENT
```


Objet argument. Enveloppe les entités Office Math lorsqu'elles sont utilisées comme arguments d'autres entités Office Math.

### ARRAY {#ARRAY}
```
public static int ARRAY
```


Objet tableau, composé d'une ou plusieurs équations, expressions ou autres séquences de texte mathématique pouvant être justifiées verticalement en tant qu'unité par rapport au texte environnant sur la ligne.

### BAR {#BAR}
```
public static int BAR
```


Fonction barre, composée d'un argument de base et d'une barre supérieure ou inférieure.

### BORDER_BOX {#BORDER-BOX}
```
public static int BORDER_BOX
```


Objet Boîte à bordure, composé d'une bordure dessinée autour d'une instance de texte mathématique (comme une formule ou une équation)

### BOX {#BOX}
```
public static int BOX
```


Objet boîte, utilisé pour regrouper les composants d'une équation ou d'une autre instance de texte mathématique.

### DEGREE {#DEGREE}
```
public static int DEGREE
```


Degré dans la racine mathématique.

### DELIMITER {#DELIMITER}
```
public static int DELIMITER
```


Objet délimiteur, composé de délimiteurs d'ouverture et de fermeture (tels que parenthèses, accolades, crochets et barres verticales), et d'un élément contenu à l'intérieur.

### DENOMINATOR {#DENOMINATOR}
```
public static int DENOMINATOR
```


Dénominateur d'un objet fraction.

### FRACTION {#FRACTION}
```
public static int FRACTION
```


Objet fraction, composé d'un numérateur et d'un dénominateur séparés par une barre de fraction.

### FUNCTION {#FUNCTION}
```
public static int FUNCTION
```


Objet Fonction-Appliquer, qui consiste en un nom de fonction et un élément argument sur lequel il agit.

### FUNCTION_NAME {#FUNCTION-NAME}
```
public static int FUNCTION_NAME
```


Nom de la fonction. Par exemple, les noms de fonctions sont sin et cos.

### GROUP_CHARACTER {#GROUP-CHARACTER}
```
public static int GROUP_CHARACTER
```


Objet Groupe-Caractère, composé d'un caractère dessiné au-dessus ou au-dessous du texte, souvent dans le but de regrouper visuellement les éléments.

### LIMIT {#LIMIT}
```
public static int LIMIT
```


Limite inférieure de l'objet [LOWER\_LIMIT](../../com.aspose.words/mathobjecttype/\#LOWER-LIMIT) et limite supérieure de la fonction [UPPER\_LIMIT](../../com.aspose.words/mathobjecttype/\#UPPER-LIMIT).

### LOWER_LIMIT {#LOWER-LIMIT}
```
public static int LOWER_LIMIT
```


Objet Limite-inférieure, composé de texte sur la ligne de base et de texte de taille réduite immédiatement en dessous.

### MATRIX {#MATRIX}
```
public static int MATRIX
```


Objet matrice, composé d'un ou plusieurs éléments disposés en une ou plusieurs lignes et une ou plusieurs colonnes.

### MATRIX_ROW {#MATRIX-ROW}
```
public static int MATRIX_ROW
```


Ligne unique de la matrice.

### NONE {#NONE}
```
public static int NONE
```


Le type d'objet n'est pas spécifié.

### NUMERATOR {#NUMERATOR}
```
public static int NUMERATOR
```


Numérateur de l'objet Fraction.

### N_ARY {#N-ARY}
```
public static int N_ARY
```


Objet n-aire, composé d'un objet n-aire, d'une base (ou opérande), et de limites supérieures et inférieures optionnelles.

### O_MATH {#O-MATH}
```
public static int O_MATH
```


Instance de texte mathématique.

### O_MATH_PARA {#O-MATH-PARA}
```
public static int O_MATH_PARA
```


Paragraphe mathématique, ou zone d'affichage mathématique, contenant un ou plusieurs éléments [O\_MATH](../../com.aspose.words/mathobjecttype/\#O-MATH) en mode affichage.

### PHANTOM {#PHANTOM}
```
public static int PHANTOM
```


Objet fantôme.

### PRE_SUB_SUPERSCRIPT {#PRE-SUB-SUPERSCRIPT}
```
public static int PRE_SUB_SUPERSCRIPT
```


Objet Pré-Sub-Surscript, qui consiste en un élément de base et un indice et un exposant placés à gauche de la base.

### RADICAL {#RADICAL}
```
public static int RADICAL
```


Objet radical, composé d'un radical, d'un élément de base et d'un degré optionnel.

### SUBSCRIPT {#SUBSCRIPT}
```
public static int SUBSCRIPT
```


Objet indice, qui se compose d'un élément de base et d'un script de taille réduite placé en dessous et à droite.

### SUBSCRIPT_PART {#SUBSCRIPT-PART}
```
public static int SUBSCRIPT_PART
```


Indice de l'objet qui peut avoir une partie indice.

### SUB_SUPERSCRIPT {#SUB-SUPERSCRIPT}
```
public static int SUB_SUPERSCRIPT
```


Objet sous-surscript, qui se compose d'un élément de base, d'un script de taille réduite placé en dessous et à droite, et d'un script de taille réduite placé au-dessus et à droite.

### SUPERSCRIPT {#SUPERSCRIPT}
```
public static int SUPERSCRIPT
```


Objet exposant, qui se compose d'un élément de base et d'un script de taille réduite placé au-dessus et à droite.

### SUPERSCRIPT_PART {#SUPERSCRIPT-PART}
```
public static int SUPERSCRIPT_PART
```


Exposant de l'objet exposant.

### UPPER_LIMIT {#UPPER-LIMIT}
```
public static int UPPER_LIMIT
```


Objet limite supérieure, composé de texte sur la ligne de base et de texte de taille réduite immédiatement au-dessus.

### length {#length}
```
public static int length
```


### fromName(String mathObjectTypeName) {#fromName-java.lang.String}
```
public static int fromName(String mathObjectTypeName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| mathObjectTypeName | java.lang.String |  |

**Returns:**
int
### getName(int mathObjectType) {#getName-int}
```
public static String getName(int mathObjectType)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| mathObjectType | int |  |

**Returns:**
java.lang.String
