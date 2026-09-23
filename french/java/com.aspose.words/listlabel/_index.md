---
title: "ListLabel"
linktitle: "ListLabel"
second_title: "Aspose.Words pour Java"
description: "Définit les propriétés spécifiques à une étiquette de liste en Java."
type: docs
weight: 428
url: /fr/java/com.aspose.words/listlabel/
---

**Inheritance:**
java.lang.Object
```
public class ListLabel
```

Définit les propriétés spécifiques à une étiquette de liste.

Pour en savoir plus, consultez l'article de documentation [ Working with Lists ][Working with Lists].

 **Examples:** 

Montre comment extraire les étiquettes de liste de tous les paragraphes qui sont des éléments de liste.

```
{@code
 Document doc = new Document(getMyDir() + "Rendering.docx");
 doc.updateListLabels();
 int listParaCount = 1;

 for (Paragraph paragraph : (Iterable) doc.getChildNodes(NodeType.PARAGRAPH, true)) {
     // Find if we have the paragraph list. In our document, our list uses plain Arabic numbers,
     // which start at three and ends at six.
     if (paragraph.getListFormat().isListItem()) {
         System.out.println(MessageFormat.format("List item paragraph #{0}", listParaCount));

         // This is the text we get when getting when we output this node to text format.
         // This text output will omit list labels. Trim any paragraph formatting characters.
         String paragraphText = paragraph.toString(SaveFormat.TEXT).trim();
         System.out.println("Exported Text: " + paragraphText);

         ListLabel label = paragraph.getListLabel();

         // This gets the position of the paragraph in the current level of the list. If we have a list with multiple levels,
         // this will tell us what position it is on that level.
         System.out.println("\tNumerical Id: {label.LabelValue}");

         // Combine them together to include the list label with the text in the output.
         System.out.println("\tList label combined with text: {label.LabelString} {paragraphText}");
     }
 }
```


[Working with Lists]: https://docs.aspose.com/words/java/working-with-lists/
## Méthodes

| Méthode | Description |
| --- | --- |
| [clearRunAttrs()](#clearRunAttrs) |  |
| [fetchInheritedRunAttr(int key)](#fetchInheritedRunAttr-int) |  |
| [getDirectRunAttr(int key)](#getDirectRunAttr-int) |  |
| [getDirectRunAttr(int key, int revisionsView)](#getDirectRunAttr-int-int) |  |
| [getFont()](#getFont) | Obtient la police de l'étiquette de liste. |
| [getLabelString()](#getLabelString) | Obtient une représentation sous forme de chaîne du libellé de la liste. |
| [getLabelValue()](#getLabelValue) | Obtient une valeur numérique pour ce libellé. |
| [removeRunAttr(int key)](#removeRunAttr-int) |  |
| [setRunAttr(int key, Object value)](#setRunAttr-int-java.lang.Object) |  |
### clearRunAttrs() {#clearRunAttrs}
```
public void clearRunAttrs()
```




### fetchInheritedRunAttr(int key) {#fetchInheritedRunAttr-int}
```
public Object fetchInheritedRunAttr(int key)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDirectRunAttr(int key) {#getDirectRunAttr-int}
```
public Object getDirectRunAttr(int key)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDirectRunAttr(int key, int revisionsView) {#getDirectRunAttr-int-int}
```
public Object getDirectRunAttr(int key, int revisionsView)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| key | int |  |
| revisionsView | int |  |

**Returns:**
java.lang.Object
### getFont() {#getFont}
```
public Font getFont()
```


Obtient la police de l'étiquette de liste.

**Returns:**
[Font](../../com.aspose.words/font/) - The list label font.
### getLabelString() {#getLabelString}
```
public String getLabelString()
```


Obtient une représentation sous forme de chaîne du libellé de la liste.

 **Examples:** 

Montre comment extraire les étiquettes de liste de tous les paragraphes qui sont des éléments de liste.

```
{@code
 Document doc = new Document(getMyDir() + "Rendering.docx");
 doc.updateListLabels();
 int listParaCount = 1;

 for (Paragraph paragraph : (Iterable) doc.getChildNodes(NodeType.PARAGRAPH, true)) {
     // Find if we have the paragraph list. In our document, our list uses plain Arabic numbers,
     // which start at three and ends at six.
     if (paragraph.getListFormat().isListItem()) {
         System.out.println(MessageFormat.format("List item paragraph #{0}", listParaCount));

         // This is the text we get when getting when we output this node to text format.
         // This text output will omit list labels. Trim any paragraph formatting characters.
         String paragraphText = paragraph.toString(SaveFormat.TEXT).trim();
         System.out.println("Exported Text: " + paragraphText);

         ListLabel label = paragraph.getListLabel();

         // This gets the position of the paragraph in the current level of the list. If we have a list with multiple levels,
         // this will tell us what position it is on that level.
         System.out.println("\tNumerical Id: {label.LabelValue}");

         // Combine them together to include the list label with the text in the output.
         System.out.println("\tList label combined with text: {label.LabelString} {paragraphText}");
     }
 }
```

**Returns:**
java.lang.String - Une représentation sous forme de chaîne du libellé de la liste.
### getLabelValue() {#getLabelValue}
```
public int getLabelValue()
```


Obtient une valeur numérique pour ce libellé.

 **Remarks:** 

Utilisez la méthode [Document.updateListLabels()](../../com.aspose.words/document/\#updateListLabels) pour mettre à jour la valeur de cette propriété.

 **Examples:** 

Montre comment extraire les étiquettes de liste de tous les paragraphes qui sont des éléments de liste.

```
{@code
 Document doc = new Document(getMyDir() + "Rendering.docx");
 doc.updateListLabels();
 int listParaCount = 1;

 for (Paragraph paragraph : (Iterable) doc.getChildNodes(NodeType.PARAGRAPH, true)) {
     // Find if we have the paragraph list. In our document, our list uses plain Arabic numbers,
     // which start at three and ends at six.
     if (paragraph.getListFormat().isListItem()) {
         System.out.println(MessageFormat.format("List item paragraph #{0}", listParaCount));

         // This is the text we get when getting when we output this node to text format.
         // This text output will omit list labels. Trim any paragraph formatting characters.
         String paragraphText = paragraph.toString(SaveFormat.TEXT).trim();
         System.out.println("Exported Text: " + paragraphText);

         ListLabel label = paragraph.getListLabel();

         // This gets the position of the paragraph in the current level of the list. If we have a list with multiple levels,
         // this will tell us what position it is on that level.
         System.out.println("\tNumerical Id: {label.LabelValue}");

         // Combine them together to include the list label with the text in the output.
         System.out.println("\tList label combined with text: {label.LabelString} {paragraphText}");
     }
 }
```

**Returns:**
int - Une valeur numérique pour ce libellé.
### removeRunAttr(int key) {#removeRunAttr-int}
```
public void removeRunAttr(int key)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| key | int |  |

### setRunAttr(int key, Object value) {#setRunAttr-int-java.lang.Object}
```
public void setRunAttr(int key, Object value)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| key | int |  |
| valeur | java.lang.Object |  |

