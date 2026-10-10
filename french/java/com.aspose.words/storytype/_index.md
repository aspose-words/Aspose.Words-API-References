---
title: "StoryType"
linktitle: "StoryType"
second_title: "Aspose.Words pour Java"
description: "Le texte d'un document Word est stocké dans des stories en Java."
type: docs
weight: 634
url: /fr/java/com.aspose.words/storytype/
---

**Inheritance:**
java.lang.Object
```
public class StoryType
```

Le texte d'un document Word est stocké dans des stories. [StoryType](../../com.aspose.words/storytype/) identifie une story.

 **Examples:** 

Montre comment supprimer toutes les formes d'un nœud.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Use a DocumentBuilder to insert a shape. This is an inline shape,
 // which has a parent Paragraph, which is a child node of the first section's Body.
 builder.insertShape(ShapeType.CUBE, 100.0, 100.0);

 Assert.assertEquals(doc.getChildNodes(NodeType.SHAPE, true).getCount(), 1);

 // We can delete all shapes from the child paragraphs of this Body.
 Assert.assertEquals(doc.getFirstSection().getBody().getStoryType(), StoryType.MAIN_TEXT);
 doc.getFirstSection().getBody().deleteShapes();

 Assert.assertEquals(doc.getChildNodes(NodeType.SHAPE, true).getCount(), 0);
 
```
## Champs

| Champ | Description |
| --- | --- |
| [COMMENTS](#COMMENTS) | Contient les commentaires du document (annotations), représentés par [Comment](../../com.aspose.words/comment/). |
| [ENDNOTES](#ENDNOTES) | Contient le texte des notes de fin, représenté par [Footnote](../../com.aspose.words/footnote/). |
| [ENDNOTE_CONTINUATION_NOTICE](#ENDNOTE-CONTINUATION-NOTICE) | Contient le texte du séparateur de l'avis de continuation de la note de fin. |
| [ENDNOTE_CONTINUATION_SEPARATOR](#ENDNOTE-CONTINUATION-SEPARATOR) | Contient le texte du séparateur de continuation de la note de fin. |
| [ENDNOTE_SEPARATOR](#ENDNOTE-SEPARATOR) | Contient le texte du séparateur de note de fin. |
| [EVEN_PAGES_FOOTER](#EVEN-PAGES-FOOTER) | Contient le texte du pied de page des pages paires, représenté par [HeaderFooter](../../com.aspose.words/headerfooter/). |
| [EVEN_PAGES_HEADER](#EVEN-PAGES-HEADER) | Contient le texte de l'en-tête des pages paires, représenté par [HeaderFooter](../../com.aspose.words/headerfooter/). |
| [FIRST_PAGE_FOOTER](#FIRST-PAGE-FOOTER) | Contient le texte du pied de page de la première page, représenté par [HeaderFooter](../../com.aspose.words/headerfooter/). |
| [FIRST_PAGE_HEADER](#FIRST-PAGE-HEADER) | Contient le texte de l'en-tête de la première page, représenté par [HeaderFooter](../../com.aspose.words/headerfooter/). |
| [FOOTNOTES](#FOOTNOTES) | Contient le texte de la note de bas de page, représenté par [Footnote](../../com.aspose.words/footnote/). |
| [FOOTNOTE_CONTINUATION_NOTICE](#FOOTNOTE-CONTINUATION-NOTICE) | Contient le texte du séparateur d'avis de continuation de note de bas de page. |
| [FOOTNOTE_CONTINUATION_SEPARATOR](#FOOTNOTE-CONTINUATION-SEPARATOR) | Contient le texte du séparateur de continuation de note de bas de page. |
| [FOOTNOTE_SEPARATOR](#FOOTNOTE-SEPARATOR) | Contient le texte du séparateur de note de bas de page. |
| [MAIN_TEXT](#MAIN-TEXT) | Contient le texte principal du document, représenté par [Body](../../com.aspose.words/body/). |
| [NONE](#NONE) | Valeur par défaut. |
| [PRIMARY_FOOTER](#PRIMARY-FOOTER) | Contient le texte du pied de page principal. |
| [PRIMARY_HEADER](#PRIMARY-HEADER) | Contient le texte de l'en-tête principal. |
| [TEXTBOX](#TEXTBOX) | Contient le texte de forme ou de zone de texte, représenté par [Shape](../../com.aspose.words/shape/). |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String storyTypeName)](#fromName-java.lang.String) |  |
| [getName(int storyType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int storyType)](#toString-int) |  |
### COMMENTS {#COMMENTS}
```
public static int COMMENTS
```


Contient les commentaires du document (annotations), représentés par [Comment](../../com.aspose.words/comment/).

### ENDNOTES {#ENDNOTES}
```
public static int ENDNOTES
```


Contient le texte des notes de fin, représenté par [Footnote](../../com.aspose.words/footnote/).

### ENDNOTE_CONTINUATION_NOTICE {#ENDNOTE-CONTINUATION-NOTICE}
```
public static int ENDNOTE_CONTINUATION_NOTICE
```


Contient le texte du séparateur de l'avis de continuation de la note de fin.

### ENDNOTE_CONTINUATION_SEPARATOR {#ENDNOTE-CONTINUATION-SEPARATOR}
```
public static int ENDNOTE_CONTINUATION_SEPARATOR
```


Contient le texte du séparateur de continuation de la note de fin.

### ENDNOTE_SEPARATOR {#ENDNOTE-SEPARATOR}
```
public static int ENDNOTE_SEPARATOR
```


Contient le texte du séparateur de note de fin.

### EVEN_PAGES_FOOTER {#EVEN-PAGES-FOOTER}
```
public static int EVEN_PAGES_FOOTER
```


Contient le texte du pied de page des pages paires, représenté par [HeaderFooter](../../com.aspose.words/headerfooter/).

### EVEN_PAGES_HEADER {#EVEN-PAGES-HEADER}
```
public static int EVEN_PAGES_HEADER
```


Contient le texte de l'en-tête des pages paires, représenté par [HeaderFooter](../../com.aspose.words/headerfooter/).

### FIRST_PAGE_FOOTER {#FIRST-PAGE-FOOTER}
```
public static int FIRST_PAGE_FOOTER
```


Contient le texte du pied de page de la première page, représenté par [HeaderFooter](../../com.aspose.words/headerfooter/).

### FIRST_PAGE_HEADER {#FIRST-PAGE-HEADER}
```
public static int FIRST_PAGE_HEADER
```


Contient le texte de l'en-tête de la première page, représenté par [HeaderFooter](../../com.aspose.words/headerfooter/).

### FOOTNOTES {#FOOTNOTES}
```
public static int FOOTNOTES
```


Contient le texte de la note de bas de page, représenté par [Footnote](../../com.aspose.words/footnote/).

### FOOTNOTE_CONTINUATION_NOTICE {#FOOTNOTE-CONTINUATION-NOTICE}
```
public static int FOOTNOTE_CONTINUATION_NOTICE
```


Contient le texte du séparateur d'avis de continuation de note de bas de page.

### FOOTNOTE_CONTINUATION_SEPARATOR {#FOOTNOTE-CONTINUATION-SEPARATOR}
```
public static int FOOTNOTE_CONTINUATION_SEPARATOR
```


Contient le texte du séparateur de continuation de note de bas de page.

### FOOTNOTE_SEPARATOR {#FOOTNOTE-SEPARATOR}
```
public static int FOOTNOTE_SEPARATOR
```


Contient le texte du séparateur de note de bas de page.

### MAIN_TEXT {#MAIN-TEXT}
```
public static int MAIN_TEXT
```


Contient le texte principal du document, représenté par [Body](../../com.aspose.words/body/).

### NONE {#NONE}
```
public static int NONE
```


Valeur par défaut. Il n'existe aucune histoire de ce type dans le document.

### PRIMARY_FOOTER {#PRIMARY-FOOTER}
```
public static int PRIMARY_FOOTER
```


Contient le texte du pied de page principal. Lorsque le pied de page diffère entre les pages impaires et paires, il contient le texte du pied de page des pages impaires. Représenté par [HeaderFooter](../../com.aspose.words/headerfooter/).

### PRIMARY_HEADER {#PRIMARY-HEADER}
```
public static int PRIMARY_HEADER
```


Contient le texte de l'en-tête principal. Lorsque l'en-tête diffère entre les pages impaires et paires, il contient le texte de l'en-tête des pages impaires. Représenté par [HeaderFooter](../../com.aspose.words/headerfooter/).

### TEXTBOX {#TEXTBOX}
```
public static int TEXTBOX
```


Contient le texte de forme ou de zone de texte, représenté par [Shape](../../com.aspose.words/shape/).

### length {#length}
```
public static int length
```


### fromName(String storyTypeName) {#fromName-java.lang.String}
```
public static int fromName(String storyTypeName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| storyTypeName | java.lang.String |  |

**Returns:**
int
### getName(int storyType) {#getName-int}
```
public static String getName(int storyType)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| storyType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int storyType) {#toString-int}
```
public static String toString(int storyType)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| storyType | int |  |

**Returns:**
java.lang.String
