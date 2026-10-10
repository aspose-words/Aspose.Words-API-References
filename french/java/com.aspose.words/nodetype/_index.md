---
title: "NodeType"
linktitle: "NodeType"
second_title: "Aspose.Words pour Java"
description: "Spécifie le type d'un nœud de document Word en Java."
type: docs
weight: 483
url: /fr/java/com.aspose.words/nodetype/
---

**Inheritance:**
java.lang.Object
```
public class NodeType
```

Spécifie le type d'un nœud de document Word.

 **Examples:** 

Montre comment parcourir la collection de nœuds enfants d'un nœud composite.

```

 Document doc = new Document();

 // Add two runs and one shape as child nodes to the first paragraph of this document.
 Paragraph paragraph = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 0, true);
 paragraph.appendChild(new Run(doc, "Hello world! "));

 Shape shape = new Shape(doc, ShapeType.RECTANGLE);
 shape.setWidth(200.0);
 shape.setHeight(200.0);
 // Note that the 'CustomNodeId' is not saved to an output file and exists only during the node lifetime.
 shape.setCustomNodeId(100);
 shape.setWrapType(WrapType.INLINE);
 paragraph.appendChild(shape);

 paragraph.appendChild(new Run(doc, "Hello again!"));

 // Iterate through the paragraph's collection of immediate children,
 // and print any runs or shapes that we find within.
 NodeCollection children = paragraph.getChildNodes(NodeType.ANY, false);

 Assert.assertEquals(3, paragraph.getChildNodes(NodeType.ANY, false).getCount());

 for (Node child : (Iterable) children)
     switch (child.getNodeType()) {
         case NodeType.RUN:
             System.out.println("Run contents:");
             System.out.println(MessageFormat.format("\t\"{0}\"", child.getText().trim()));
             break;
         case NodeType.SHAPE:
             Shape childShape = (Shape)child;
             System.out.println("Shape:");
             System.out.println(MessageFormat.format("\t{0}, {1}x{2}", childShape.getShapeType(), childShape.getWidth(), childShape.getHeight()));
             break;
     }
 
```
## Champs

| Champ | Description |
| --- | --- |
| [ANY](#ANY) | Indique tous les types de nœuds. |
| [BODY](#BODY) | Un objet [Body](../../com.aspose.words/body/) qui contient le texte principal d'une section (histoire de texte principal). |
| [BOOKMARK_END](#BOOKMARK-END) | Une fin de marqueur de signet. |
| [BOOKMARK_START](#BOOKMARK-START) | Un début de marqueur de signet. |
| [BUILDING_BLOCK](#BUILDING-BLOCK) | Un bloc de construction dans un document de glossaire (par ex. |
| [CELL](#CELL) | Une cellule d'une ligne de tableau. |
| [COMMENT](#COMMENT) | Un commentaire dans un document Word. |
| [COMMENT_RANGE_END](#COMMENT-RANGE-END) | Un nœud marqueur qui représente la fin d'une plage commentée. |
| [COMMENT_RANGE_START](#COMMENT-RANGE-START) | Un nœud marqueur qui représente le début d'une plage commentée. |
| [DOCUMENT](#DOCUMENT) | Un objet [Document](../../com.aspose.words/document/) qui, en tant que racine de l'arbre du document, donne accès à l'ensemble du document Word. |
| [EDITABLE_RANGE_END](#EDITABLE-RANGE-END) | Une fin d'une plage modifiable. |
| [EDITABLE_RANGE_START](#EDITABLE-RANGE-START) | Un début d'une plage modifiable. |
| [FIELD_END](#FIELD-END) | Un caractère spécial qui désigne la fin d'un champ Word. |
| [FIELD_SEPARATOR](#FIELD-SEPARATOR) | Un caractère spécial qui sépare le code du champ du résultat du champ. |
| [FIELD_START](#FIELD-START) | Un caractère spécial qui désigne le début d'un champ Word. |
| [FOOTNOTE](#FOOTNOTE) | Une note de bas de page ou une note de fin dans un document Word. |
| [FORM_FIELD](#FORM-FIELD) | Un champ de formulaire. |
| [GLOSSARY_DOCUMENT](#GLOSSARY-DOCUMENT) | Un document de glossaire dans le document principal. |
| [GROUP_SHAPE](#GROUP-SHAPE) | Un groupe de formes, d'images, d'objets OLE ou d'autres formes groupées. |
| [HEADER_FOOTER](#HEADER-FOOTER) | Un objet [HeaderFooter](../../com.aspose.words/headerfooter/) qui contient le texte d'un en-tête ou d'un pied de page particulier à l'intérieur d'une section. |
| [MOVE_FROM_RANGE_END](#MOVE-FROM-RANGE-END) | Une fin d'une plage MoveFrom. |
| [MOVE_FROM_RANGE_START](#MOVE-FROM-RANGE-START) | Un début d'une plage MoveFrom. |
| [MOVE_TO_RANGE_END](#MOVE-TO-RANGE-END) | Une fin d'une plage MoveTo. |
| [MOVE_TO_RANGE_START](#MOVE-TO-RANGE-START) | Un début d'une plage MoveTo. |
| [NULL](#NULL) | Réservé à un usage interne par Aspose.Words. |
| [OFFICE_MATH](#OFFICE-MATH) | Un objet Office Math. |
| [PARAGRAPH](#PARAGRAPH) | Un paragraphe de texte. |
| [ROW](#ROW) | Une ligne d'un tableau. |
| [RUN](#RUN) | Une séquence de texte. |
| [SECTION](#SECTION) | Un objet [Section](../../com.aspose.words/section/) qui correspond à une section dans un document Word. |
| [SHAPE](#SHAPE) | Un objet de dessin, tel qu'une forme OfficeArt, une image ou un objet OLE. |
| [SMART_TAG](#SMART-TAG) | Une balise intelligente autour d'une ou plusieurs structures en ligne (runs, images, champs, etc.) dans un paragraphe. |
| [SPECIAL_CHAR](#SPECIAL-CHAR) | Un caractère spécial qui ne fait pas partie des types de caractères spéciaux plus spécifiques. |
| [STRUCTURED_DOCUMENT_TAG](#STRUCTURED-DOCUMENT-TAG) | Permet de définir des informations spécifiques au client et leurs moyens de présentation. |
| [STRUCTURED_DOCUMENT_TAG_RANGE_END](#STRUCTURED-DOCUMENT-TAG-RANGE-END) | Une fin de balise de document structuré **ranged** qui accepte du contenu multi-sections. |
| [STRUCTURED_DOCUMENT_TAG_RANGE_START](#STRUCTURED-DOCUMENT-TAG-RANGE-START) | Un début de balise de document structuré **ranged** qui accepte du contenu multi-sections. |
| [SUB_DOCUMENT](#SUB-DOCUMENT) | Un nœud de sous-document qui est un lien vers un autre document. |
| [SYSTEM](#SYSTEM) | Réservé à un usage interne par Aspose.Words. |
| [TABLE](#TABLE) | Un objet [Table](../../com.aspose.words/table/) qui représente un tableau dans un document Word. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String nodeTypeName)](#fromName-java.lang.String) |  |
| [getName(int nodeType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int nodeType)](#toString-int) |  |
### ANY {#ANY}
```
public static int ANY
```


Indique tous les types de nœuds. Permet de sélectionner tous les enfants.

### BODY {#BODY}
```
public static int BODY
```


Un objet [Body](../../com.aspose.words/body/) qui contient le texte principal d'une section (histoire de texte principal).

Un nœud [Body](../../com.aspose.words/body/) peut contenir des nœuds [Paragraph](../../com.aspose.words/paragraph/) et [Table](../../com.aspose.words/table/).

### BOOKMARK_END {#BOOKMARK-END}
```
public static int BOOKMARK_END
```


Une fin de marqueur de signet.

### BOOKMARK_START {#BOOKMARK-START}
```
public static int BOOKMARK_START
```


Un début de marqueur de signet.

### BUILDING_BLOCK {#BUILDING-BLOCK}
```
public static int BUILDING_BLOCK
```


Un élément de construction dans un document de glossaire (par ex. entrée de document de glossaire).

### CELL {#CELL}
```
public static int CELL
```


Une cellule d'une ligne de tableau.

Un nœud [Cell](../../com.aspose.words/cell/) peut contenir des nœuds [Paragraph](../../com.aspose.words/paragraph/) et [Table](../../com.aspose.words/table/).

### COMMENT {#COMMENT}
```
public static int COMMENT
```


Un commentaire dans un document Word.

Un nœud [Comment](../../com.aspose.words/comment/) peut contenir des nœuds [Paragraph](../../com.aspose.words/paragraph/) et [Table](../../com.aspose.words/table/).

### COMMENT_RANGE_END {#COMMENT-RANGE-END}
```
public static int COMMENT_RANGE_END
```


Un nœud marqueur qui représente la fin d'une plage commentée.

### COMMENT_RANGE_START {#COMMENT-RANGE-START}
```
public static int COMMENT_RANGE_START
```


Un nœud marqueur qui représente le début d'une plage commentée.

### DOCUMENT {#DOCUMENT}
```
public static int DOCUMENT
```


Un objet [Document](../../com.aspose.words/document/) qui, en tant que racine de l'arbre du document, donne accès à l'ensemble du document Word.

Un nœud [Document](../../com.aspose.words/document/) peut contenir des nœuds [Section](../../com.aspose.words/section/).

### EDITABLE_RANGE_END {#EDITABLE-RANGE-END}
```
public static int EDITABLE_RANGE_END
```


Une fin d'une plage modifiable.

### EDITABLE_RANGE_START {#EDITABLE-RANGE-START}
```
public static int EDITABLE_RANGE_START
```


Un début d'une plage modifiable.

### FIELD_END {#FIELD-END}
```
public static int FIELD_END
```


Un caractère spécial qui désigne la fin d'un champ Word.

### FIELD_SEPARATOR {#FIELD-SEPARATOR}
```
public static int FIELD_SEPARATOR
```


Un caractère spécial qui sépare le code du champ du résultat du champ.

### FIELD_START {#FIELD-START}
```
public static int FIELD_START
```


Un caractère spécial qui désigne le début d'un champ Word.

### FOOTNOTE {#FOOTNOTE}
```
public static int FOOTNOTE
```


Une note de bas de page ou une note de fin dans un document Word.

Un nœud [Footnote](../../com.aspose.words/footnote/) peut contenir des nœuds [Paragraph](../../com.aspose.words/paragraph/) et [Table](../../com.aspose.words/table/).

### FORM_FIELD {#FORM-FIELD}
```
public static int FORM_FIELD
```


Un champ de formulaire.

### GLOSSARY_DOCUMENT {#GLOSSARY-DOCUMENT}
```
public static int GLOSSARY_DOCUMENT
```


Un document de glossaire dans le document principal.

### GROUP_SHAPE {#GROUP-SHAPE}
```
public static int GROUP_SHAPE
```


Un groupe de formes, d'images, d'objets OLE ou d'autres formes groupées.

Un nœud [GroupShape](../../com.aspose.words/groupshape/) peut contenir d'autres nœuds [Shape](../../com.aspose.words/shape/) et [GroupShape](../../com.aspose.words/groupshape/).

### HEADER_FOOTER {#HEADER-FOOTER}
```
public static int HEADER_FOOTER
```


Un objet [HeaderFooter](../../com.aspose.words/headerfooter/) qui contient le texte d'un en-tête ou d'un pied de page particulier à l'intérieur d'une section.

Un nœud [HeaderFooter](../../com.aspose.words/headerfooter/) peut contenir des nœuds [Paragraph](../../com.aspose.words/paragraph/) et [Table](../../com.aspose.words/table/).

### MOVE_FROM_RANGE_END {#MOVE-FROM-RANGE-END}
```
public static int MOVE_FROM_RANGE_END
```


Une fin d'une plage MoveFrom.

### MOVE_FROM_RANGE_START {#MOVE-FROM-RANGE-START}
```
public static int MOVE_FROM_RANGE_START
```


Un début d'une plage MoveFrom.

### MOVE_TO_RANGE_END {#MOVE-TO-RANGE-END}
```
public static int MOVE_TO_RANGE_END
```


Une fin d'une plage MoveTo.

### MOVE_TO_RANGE_START {#MOVE-TO-RANGE-START}
```
public static int MOVE_TO_RANGE_START
```


Un début d'une plage MoveTo.

### NULL {#NULL}
```
public static int NULL
```


Réservé à un usage interne par Aspose.Words.

### OFFICE_MATH {#OFFICE-MATH}
```
public static int OFFICE_MATH
```


Un objet Office Math. Peut être une équation, une fonction, une matrice ou l'un des autres objets mathématiques. Peut être une collection d'objets mathématiques et peut également contenir des objets non mathématiques tels que des séquences de texte.

### PARAGRAPH {#PARAGRAPH}
```
public static int PARAGRAPH
```


Un paragraphe de texte.

Un nœud [Paragraph](../../com.aspose.words/paragraph/) est un conteneur pour les éléments de niveau en ligne [Run](../../com.aspose.words/run/), [FieldStart](../../com.aspose.words/fieldstart/), [FieldSeparator](../../com.aspose.words/fieldseparator/), [FieldEnd](../../com.aspose.words/fieldend/), [FormField](../../com.aspose.words/formfield/), [Shape](../../com.aspose.words/shape/), [GroupShape](../../com.aspose.words/groupshape/), [Footnote](../../com.aspose.words/footnote/), [Comment](../../com.aspose.words/comment/), [SpecialChar](../../com.aspose.words/specialchar/), ainsi que [BookmarkStart](../../com.aspose.words/bookmarkstart/) et [BookmarkEnd](../../com.aspose.words/bookmarkend/).

### ROW {#ROW}
```
public static int ROW
```


Une ligne d'un tableau.

Un nœud [Row](../../com.aspose.words/row/) peut contenir des nœuds [Cell](../../com.aspose.words/cell/).

### RUN {#RUN}
```
public static int RUN
```


Une séquence de texte.

### SECTION {#SECTION}
```
public static int SECTION
```


Un objet [Section](../../com.aspose.words/section/) qui correspond à une section dans un document Word.

Un nœud [Section](../../com.aspose.words/section/) peut contenir des nœuds [Body](../../com.aspose.words/body/) et [HeaderFooter](../../com.aspose.words/headerfooter/).

### SHAPE {#SHAPE}
```
public static int SHAPE
```


Un objet de dessin, tel qu'une forme OfficeArt, une image ou un objet OLE.

Un nœud [Shape](../../com.aspose.words/shape/) peut contenir des nœuds [Paragraph](../../com.aspose.words/paragraph/) et [Table](../../com.aspose.words/table/).

### SMART_TAG {#SMART-TAG}
```
public static int SMART_TAG
```


Une balise intelligente autour d'une ou plusieurs structures en ligne (runs, images, champs, etc.) dans un paragraphe.

### SPECIAL_CHAR {#SPECIAL-CHAR}
```
public static int SPECIAL_CHAR
```


Un caractère spécial qui ne fait pas partie des types de caractères spéciaux plus spécifiques.

### STRUCTURED_DOCUMENT_TAG {#STRUCTURED-DOCUMENT-TAG}
```
public static int STRUCTURED_DOCUMENT_TAG
```


Permet de définir des informations spécifiques au client et leurs moyens de présentation.

### STRUCTURED_DOCUMENT_TAG_RANGE_END {#STRUCTURED-DOCUMENT-TAG-RANGE-END}
```
public static int STRUCTURED_DOCUMENT_TAG_RANGE_END
```


Une fin de balise de document structuré **ranged** qui accepte du contenu multi-sections.

### STRUCTURED_DOCUMENT_TAG_RANGE_START {#STRUCTURED-DOCUMENT-TAG-RANGE-START}
```
public static int STRUCTURED_DOCUMENT_TAG_RANGE_START
```


Un début de balise de document structuré **ranged** qui accepte du contenu multi-sections.

### SUB_DOCUMENT {#SUB-DOCUMENT}
```
public static int SUB_DOCUMENT
```


Un nœud de sous-document qui est un lien vers un autre document.

### SYSTEM {#SYSTEM}
```
public static int SYSTEM
```


Réservé à un usage interne par Aspose.Words.

### TABLE {#TABLE}
```
public static int TABLE
```


Un objet [Table](../../com.aspose.words/table/) qui représente un tableau dans un document Word.

Un nœud [Table](../../com.aspose.words/table/) peut contenir des nœuds [Row](../../com.aspose.words/row/).

### length {#length}
```
public static int length
```


### fromName(String nodeTypeName) {#fromName-java.lang.String}
```
public static int fromName(String nodeTypeName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| nodeTypeName | java.lang.String |  |

**Returns:**
int
### getName(int nodeType) {#getName-int}
```
public static String getName(int nodeType)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| nodeType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int nodeType) {#toString-int}
```
public static String toString(int nodeType)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| nodeType | int |  |

**Returns:**
java.lang.String
